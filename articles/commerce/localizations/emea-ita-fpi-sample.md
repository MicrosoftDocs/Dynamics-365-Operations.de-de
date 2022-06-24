---
title: Beispiel für die Einbindung eines Belegdruckers für Italien
description: In diesem Artikel erhalten Sie einen Überblick über das steuerliche Integrationsbeispiel für Italien in Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2018-11-1
ms.openlocfilehash: 2aa1851fe5fe447ba2dd4640be9881b37e54216e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909389"
---
# <a name="fiscal-printer-integration-sample-for-italy"></a>Beispiel für die Einbindung eines Belegdruckers für Italien

[!include[banner](../includes/banner.md)]

In diesem Artikel erhalten Sie einen Überblick über das steuerliche Integrationsbeispiel für Italien in Microsoft Dynamics 365 Commerce.

Die Commerce-Funktionalität für Italien umfasst eine Beispielintegration des Point of Sale (POS) mit einem Fiskaldrucker. Die Probe erweitert die [Steuerliche Integrationsfunktion](fiscal-integration-for-retail-channel.md) damit es mit [Epson FP-90III-Serie](https://www.epson.it/products/sd/pos-printer/epson-fp-90iii-series) Drucker von Epson funktioniert und es ermöglicht die Kommunikation mit einem Steuerdrucker im Webserver-Modus über den EpsonFPMate-Webservice unter Verwendung der Fiscal ePOS-Print API. Das Beispiel unterstützt nur den Registratore Telematico (RT)-Modus. Das Beispiel wird in der Form eines Quellcodes bereitgestellt und ist Teil des Retail Software Development Kit (SDK).

Microsoft gibt keine Hardware, Software oder Dokumentation von Epson frei. Für Informationen darüber, wie Sie den Fiskaldrucker erhalten und betreiben, wenden Sie sich an [Epson Italia SpA](https://www.epson.it).

## <a name="scenarios"></a>Szenarien

Die folgenden Szenarien werden im Beispiel für die Integration des Steuerregistrierungsservice für Italien abgedeckt:

- Verkaufsszenarien:

    - Druck eines Kassenbons für Cash-and-Carry-Verkäufe und Retouren.
    - Erfassen Sie eine Antwort vom Fiskaldrucker und speichern Sie sie in der Channel-Datenbank.
    - Steuern:

        - Zuordnung zu den Steuercodes (Abteilungen) des Fiskaldruckers.
        - Übertragen Sie zugeordnete Steuerdaten an den Fiskaldrucker.
        - Drucken Sie Steuern auf eine Steuerquittung.

    - Zahlungen:

        - Zuordnung zu den Zahlungsarten des Fiskaldruckers.
        - Drucken Sie Zahlungen auf einem Fiskalbeleg.
        - Änderungsinformationen drucken.

    - Positionsrabattbetrag drucken.
    - Geschenkkarten:

        - Schließen Sie eine ausgegebene/aufgeladene Zeile einer Geschenkkarte aus einem Kassenbon für einen Verkauf aus.
        - Drucken Sie eine Zahlung, die eine Geschenkkarte als reguläre Zahlungsmethode verwendet.

    - Drucken Sie Fiskalquittungen für Vorgänge bei Kundenbestellungen:

        - Für die Einzahlung einer Kundenbestellung wird kein Steuerbeleg gedruckt.
        - Drucken Sie einen Steuerbeleg für Carryout-Positionen eines hybriden Kundenauftrags.
        - Drucken Sie einen Kassenbon für den Vorgang der Abholung eines Kundenauftrags.
        - Drucken Sie eine Quittung für eine Rücklieferung.

    - Drucken Sie einen Strichcode für die Quittungsnummer auf einer Steuerquittung.
    - Drucken Sie die [ Kundeninformation](emea-ita-customer-information.md) die für eine Verkaufstransaktion auf einem Steuerbeleg angegeben ist. Ein Beispiel für diese Informationen ist der Lotteriecode des Kunden. 

- Tagesendabschlüsse (Fiskalische X- und Fiskalische Z-Berichte).
- Fehlerbehebung, wie beispielsweise die folgenden Optionen:

    - Versuchen Sie die Fiskalregistrierung erneut, wenn ein erneuter Versuch möglich ist, z. B. wenn der Fiskaldrucker nicht angeschlossen ist, nicht bereit ist oder nicht reagiert, der Drucker kein Papier hat oder ein Papierstau vorliegt.
    - Verschieben Sie die Steuererfassung.
    - Überspringen Sie Steuererfassung, oder markieren Sie die Buchung als erfasst, und schließen Sie Infocodes ein, um den Grund für den Fehler und zusätzliche Informationen zu erfassen.
    - Prüfen Sie die Verfügbarkeit des Fiskaldruckers, bevor eine neue Verkaufstransaktion eröffnet oder eine Verkaufstransaktion abgeschlossen wird.

### <a name="gift-cards"></a>Geschenkkarten

Das Fiskaldrucker-Integrationsbeispiel implementiert die folgenden Regeln, die sich auf Geschenkkarten beziehen:

- Schließen Sie Verkaufszeilen, die mit den Vorgängen *Geschenkkarte ausgeben* und *Zu Geschenkkarte hinzufügen* verbunden sind, vom Fiskalbon aus.
- Drucken Sie keinen Kassenbon, wenn er nur aus Geschenkkartenzeilen besteht.
- Ziehen Sie den Gesamtbetrag der Geschenkkarten, die in einer Transaktion ausgegeben oder aufgeladen werden, von den Zahlungszeilen des Steuerbelegs ab.
- Speichern Sie berechnete Zahlungsregulierungspositionen in der Kanaldatenbank mit einem Verweis auf eine entsprechende Steuerbuchung.
- Zahlung per Geschenkkarte wird als eine normale Zahlung betrachtet.

### <a name="customer-deposits-and-customer-order-deposits"></a>Debitoreneinzahlungen und Debitorenauftragseinzahlungen

Das Beispiel der Fiskaldrucker-Integration implementiert die folgenden Regeln, die sich auf Kundeneinlagen und Kundenauftragseinlagen beziehen:

- Drucken Sie keine Quittung, wenn es sich bei einer Transaktion um eine Kundeneinzahlung handelt.
- Drucken Sie keinen Kassenbon, wenn eine Transaktion nur eine Einzahlung auf eine Kundenbestellung oder eine Rückerstattung einer Kundenbestellung enthält.
- Drucken Sie den Betrag der zuvor geleisteten Anzahlung auf einem Fiskalbeleg für einen Vorgang zur Abholung eines Kundenauftrags.
- Ziehen Sie den Debitorenauftragseinzahlungsbetrag von den Zahlungspositionen ab, wenn ein hybrider Kundenauftrag erstellt wird.
- Speichern Sie berechnete Zahlungsregulierungspositionen in der Kanaldatenbank mit einem Verweis auf eine Steuerbuchung für einen hybriden Debitorenauftrag.

### <a name="limitations-of-the-sample"></a>Einschränkungen des Beispiels

- Der Fiskaldrucker unterstützt nur Szenarien, bei denen die Mehrwertsteuer im Preis enthalten ist. Daher muss die Option **Preis in Mehrwertsteuer enthalten** auf **Ja** sowohl für Geschäfte als auch Debitoren festgelegt werden.
- Tagesberichte (Fiskal X und Fiskal Z) werden in dem Format gedruckt, das in die Firmware des Fiskaldruckers eingebettet ist.
- Der Fiskaldrucker unterstützt keine gemischten Transaktionen. Die Option **Verkäufe und Retouren auf einem Bon nicht mischen** sollte in den Profilen der POS-Funktionalität auf **Ja** festgelegt werden.
- Das Beispiel unterstützt nur die Integration mit einem Fiskaldrucker, der im Registratore Telematico (RT))-Modus arbeitet.

## <a name="set-up-fiscal-integration-for-italy"></a>Steuerintegration für Italien einrichten

Die Beispiele für diese Druckerintegration für Italien basiert auf der [steuerlichen Integrationsfunktionalität](fiscal-integration-for-retail-channel.md) und ist Teil der Retail SDK. Die Probe befindet sich im Ordner **src\\Fiscallntegration\\EpsonFP90IIISample** des [Dynamics 365 Commerce Lösungen](https://github.com/microsoft/Dynamics365Commerce.Solutions/) Repository (zum Beispiel [die Stichprobe in Release/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/EpsonFP90IIISample)). Das Beispiel [besteht](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) aus einem Anbieter von fiskalischen Belegen, der eine Erweiterung der Commerce Runtime (CRT) ist, und einem fiskalischen Konnektor, der eine Erweiterung der Commerce Hardware Station ist. Weitere Informationen über die Verwendung des Retail SDK finden Sie unter [Retail SDK Architektur](../dev-itpro/retail-sdk/retail-sdk-overview.md) und [Einrichten einer Build-Pipeline für das Independent-Packaging SDK](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Aufgrund der Einschränkungen des [neuen unabhängigen Verpackungs- und Erweiterungsmodells](../dev-itpro/build-pipeline.md) kann es derzeit nicht für dieses Beispiel der steuerlichen Integration verwendet werden. Sie müssen die vorherige Version des Retail SDK auf einer virtuellen Maschine (VM) für Entwickler in Microsoft Dynamics Lifecycle Services (LCS) verwenden. Weitere Informationen unter [Bereitstellungsrichtlinien für den Steuerdrucker-Integrationsbeispiel für Italien (Legacy)](emea-ita-fpi-sample-sdk.md).
>
> Die Unterstützung des neuen unabhängigen Paketierungs- und Erweiterungsmodells für steuerliche Integrationsmuster ist für spätere Versionen geplant.

Schließen Sie die Schritte zur Einrichtung der Fiskalintegration ab, die unter [Einrichten der Fiskalintegration für Commerce-Kanäle](setting-up-fiscal-integration-for-retail-channel.md) festgelegt sind.

1. [Richten Sie einen Steuererfassungsprozesses ein](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Notieren Sie sich auch die Einstellungen für den Prozess der steuerlichen Registrierung, die [spezifisch für dieses Beispiel der Steuerdrucker-Integration sind](#set-up-the-registration-process).
1. [Steuertexte für Rabatte einrichten](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-texts-for-discounts).
1. [Legen Sie Einstellungen zur Fehlerbehandlung fest](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Fiskalische X/Z-Berichte vom POS festlegen](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-xz-reports-from-the-pos).
1. [Aktivieren Sie manuelle Ausführung der verschobenen steuerlichen Erfassung](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Einrichten der Funktionalität für die Verwaltung von Kundeninformationen in POS](emea-ita-customer-information.md#setup).
1. [Kanal-Komponenten konfigurieren](#configure-channel-components).

### <a name="set-up-the-registration-process"></a>Den Erfassungsprozess einrichten

Um den Registrierungsprozess zu aktivieren, folgen Sie diesen Schritten, um die Commerce-Zentrale festzulegen. Weitere Informationen finden Sie unter [Einrichten der Fiskalintegration für Commerce-Kanäle](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

1. Laden Sie die Konfigurationsdateien für den Fiskalbeleg-Anbieter und den Fiskal-Konnektor herunter:

    1. Öffnen Sie das [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions/) Repository.
    1. Wählen Sie eine korrekte Version des Release Branches entsprechend Ihrer SDK-/Anwendungsversion (zum Beispiel **[Release/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**).
    1. Öffnen Sie **src \> FiscalIntegration \> EpsonFP90IIISample**.
    1. Laden Sie die Konfigurationsdatei des Fiskaldokumentanbieters herunter unter **CommerceRuntime \> DocumentProvider.EpsonFP90IIISample \> Konfiguration \> DocumentProviderEpsonFP90IIISample.xml** (beispielsweise [die Datei für den Release/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/EpsonFP90IIISample/CommerceRuntime/DocumentProvider.EpsonFP90IIISample/Configuration/DocumentProviderEpsonFP90IIISample.xml)).
    1. Laden Sie die Konnektor-Konfigurationsdatei des Fiskaldokumentanbieters herunter **HardwareStation \> EpsonFP90IIIFiscalDeviceSample \> Konfiguration\> ConnectorEpsonFP90IIISample.xml** (Beispielsweise [die Datei für Release/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/EpsonFP90IIISample/HardwareStation/EpsonFP90IIIFiscalDeviceSample/Configuration/ConnectorEpsonFP90IIISample.xml).

    > [!WARNING]
    > Aufgrund der Einschränkungen des [neuen unabhängigen Verpackungs- und Erweiterungsmodells](../dev-itpro/build-pipeline.md) kann es derzeit nicht für dieses Beispiel der steuerlichen Integration verwendet werden. Sie müssen die Vorgängerversion des Retail SDK auf einer Entwickler-VM in LCS verwenden. Die Konfigurationsdateien für dieses Beispiel zur Fiskalintegration befinden sich in den folgenden Ordnern des Retail SDK auf einer Entwickler-VM in LCS:
    >
    > - **Steuerdokument-Konfigurationsdatei-Anbieter:** RetailSdk\\SampleExtensions\\CommerceRuntime\\Extension.DocumentProvider.EpsonFP90IIISample\\Configuration\\DocumentProviderEpsonFP90IIISample.xml
    > - **Steuerkonnektor-Konfigurationsdatei** RetailSdk\\SampleExtensions\\HardwareStation\\Extension.EpsonFP90IIIFiscalDeviceSample\\Configuration\\ConnectorEpsonFP90IIISample.xml
    > 
    > Die Unterstützung des neuen unabhängigen Paketierungs- und Erweiterungsmodells für steuerliche Integrationsmuster ist für spätere Versionen geplant.

1. Gehen Sie zu **Einzelhandel und Handel \> Zentralverwaltungseinrichtung \> Parameter \> Gemeinsame Commerce-Parameter**. Auf der Registerkarte **Allgemein** legen Sie die Option **Steuerintegration aktivieren** auf **Ja** fest.
1. Gehen Sie zu **Handel und Commerce \> Channel-Einrichtung \> Fiskalische Integration \> Fiskalische Belege**, und laden Sie die Konfigurationsdatei des Fiskalischen Belegs, die Sie zuvor heruntergeladen haben.
1. Gehen Sie zu **Retail und Commerce \> Channel Einrichtung \> Fiskalische Integration \> Fiskalische Konnektoren**, und laden Sie die Konfigurationsdatei für den Fiskalischen Konnektor, die Sie zuvor heruntergeladen haben.
1. Wechseln Sie zu **Einzelhandel und Handel \> Kanaleinrichtung \> Steuerintegration \> Konnektorfunktionsprofile**. Erstellen Sie ein neues funktionales Profil für den Konnektor. Wählen Sie den Beleg-Anbieter und den Konnektor, den Sie zuvor geladen haben. Aktualisieren Sie die [Einstellungen für die Datenzuordnung](#default-data-mapping) nach Bedarf.
1. Wechseln Sie zu **Einzelhandel und Handel \> Kanaleinrichtung \> Steuerintegration \> Technische Profile des Connectors**. Erstellen Sie ein neues technisches Profil für den Konnektor und wählen Sie den Fiskalkonnektor, den Sie zuvor erstellt haben. Aktualisieren Sie die [Konnektor-Einstellungen](#fiscal-connector-settings) nach Bedarf.
6. Wechseln Sie zu **Einzelhandel und Handel \> Kanaleinrichtung \> Steuerintegration \> Steuerkonnektorgruppen**. Erstellen Sie eine neue Steuerkonnektorgruppen für das funktionale Konnektorfunktionsprofil, das Sie vorher erstellt haben.
7. Wechseln Sie zu **Einzelhandel und Handel \> Kanaleinrichtung \> Steuerintegration \> Steuererfassungsprozesse**. Erstellen Sie einen neuen Fiskalregistrierungsprozess und einen Fiskalregistrierungsprozessschritt und wählen Sie die Fiskalkonnektorgruppe, die Sie zuvor erstellt haben.
8. Gehen Sie zu **Einzelhandel und Handel \> Kanaleinrichtung \> POS-Einrichtung \> POS-Profile \> Funktionsprofile**. Wählen Sie ein Funktionsprofil aus, das mit dem Einzelhandelsgeschäft verbunden ist, wo der Erfassungsprozess aktiviert werden soll. Im Inforegister **Steuererfassungsprozess** aktivieren Sie den Steuererfassungsprozess, den Sie vorher erstellt haben.
9. Wechseln Sie zu **Einzelhandel und Handel \> Kanaleinrichtung \> POS-Einrichtung \> POS-Profile \> Hardwareprofile**. Wählen Sie ein Hardwareprofil aus, das mit der Hardware station verknüpft ist, mit der der Belegdrucker verbunden wird. Im Inforegister **Peripheriegeräte für die Steuerverwaltung** aktivieren Sie das technische Konnektorprofil, das Sie vorher erstellt haben.
10. Öffnen Sie den Vertriebsplan (**Retail and Commerce \> Retail and Commerce IT \> Vertriebsplan**), und wählen Sie Jobs **1070** und **1090** aus, um Daten zur Kanaldatenbank zu übertragen.

#### <a name="default-data-mapping"></a>Standarddatenzuordnung

Die folgende Standarddatenzuordnung ist in der Steuerbeleganbieter-Konfiguration enthalten, die als Teil des Steuerintegrationsbeispiels bereitgestellt wird:

- **Zuordnung der Ausschreibungsarten** – Die Zuordnung von Zahlungsmethoden, die für den Store konfiguriert sind, zu Zahlungsarten, die der Fiskaldrucker unterstützt. Das folgende Beispiel zeigt die standardmäßige Zuordnung.

    ```JSON
    {"PaymentMethods": [
        {"StorePaymentMethod":"1", "PrinterPaymentType":"0", "PrinterPaymentIndex":"00"},
        {"StorePaymentMethod":"3", "PrinterPaymentType":"2", "PrinterPaymentIndex":"00"},
        {"StorePaymentMethod":"4", "PrinterPaymentType":"2", "PrinterPaymentIndex":"01"},
        {"StorePaymentMethod":"6", "PrinterPaymentType":"0", "PrinterPaymentIndex":"01"},
        {"StorePaymentMethod":"8", "PrinterPaymentType":"6", "PrinterPaymentIndex":"01"}
        ],
        "DepositPaymentMethod": {"PrinterPaymentType":"2", "PrinterPaymentIndex":"00"}}
    ```

    Hier ist eine Erläuterung der Attribute dieser Zuordnung:

    - **StorePaymentMethod** ist eine Zahlungsmethode, die für den Store unter **Einzelhandel und Gewerbe \> Kanaleinrichtung \> Zahlungsarten \> Zahlungsarten** eingerichtet ist.
    - **PrinterPaymentType** und **PrinterPaymentIndex** sind die entsprechende Zahlungsart und der Index, die in der Epson Fiskaldruckerdokumentation definiert sind.
    - **DepositPaymentMethod** wird verwendet, um die Zahlungsart und den Index eines Druckers für den Teil des Abholbetrags der Kundenbestellung anzugeben, der mit der Anzahlung der Kundenbestellung verrechnet wird.

    Die folgende Tabelle zeigt, wie Musterzuordnung von Zahlarten den Storezahlarten entspricht, die in den Standard-Demodaten konfiguriert sind.

    | Zahlungsweise | Name der Zahlungsmethode |
    |----------------|---------------------|
    | 1              | Bargeld                |
    | 3              | Karte                |
    | 4              | Debitorenkonto    |
    | 6              | Währung            |
    | 8              | Geschenkkarte           |

    Sie müssen die Beispielzuordnung entsprechend den in Ihrer Anwendung konfigurierten Zahlungsformen ändern.

- **Barcodetyp für Belegnummer** – Der Strichcodetyp, der verwendet wird, um eine Belegnummer auf einem Steuerbeleg anzuzeigen. Der Standardwert ist **CODE128**.
- **Steuerdaten im Belegkopf drucken** – Wenn dieser Parameter aktiviert ist, werden die Geschäftsinformationen auf dem Kassenbon gedruckt. Zu diesen Informationen gehören der Name, die Adresse und die Steueridentifikationsnummer des Geschäfts sowie der Name des Kassierers.
- **Zuordnung der Finanzdruckerabteilung** – Die Zuordnung der Abteilungen der Fiskaldruckerei zu Mehrwertsteuersätzen, Mehrwertsteuerbefreiten und Produktarten. Das folgende Beispiel zeigt die standardmäßige Zuordnung.

    ```JSON
    {"Departments": [
        {"VATRate":"2200", "VATExemptNature":"", "ProductType":"0", "DepartmentNumber":"01"},
        {"VATRate":"2200", "VATExemptNature":"", "ProductType":"1", "DepartmentNumber":"02"},
        {"VATRate":"1000", "VATExemptNature":"", "ProductType":"0", "DepartmentNumber":"03"},
        {"VATRate":"1000", "VATExemptNature":"", "ProductType":"1", "DepartmentNumber":"04"},
        {"VATRate":"0500", "VATExemptNature":"", "ProductType":"0", "DepartmentNumber":"05"},
        {"VATRate":"0500", "VATExemptNature":"", "ProductType":"1", "DepartmentNumber":"06"},
        {"VATRate":"0400", "VATExemptNature":"", "ProductType":"0", "DepartmentNumber":"07"},
        {"VATRate":"0400", "VATExemptNature":"", "ProductType":"1", "DepartmentNumber":"08"},
        {"VATRate":"0000", "VATExemptNature":"", "ProductType":"0", "DepartmentNumber":"09"},
        {"VATRate":"0000", "VATExemptNature":"", "ProductType":"1", "DepartmentNumber":"10"},
        {"VATRate":"0000", "VATExemptNature":"NS", "ProductType":"0", "DepartmentNumber":"99"}]}
    ```

    Hier ist eine Erläuterung der Attribute dieser Zuordnung:

    - **VATRate** ist ein unterstützter Mehrwertsteuersatz, der als Mehrwertsteuercode konfiguriert ist. Der Wert in der Zuordnung hat zwei Dezimalstellen, aber kein Dezimaltrennzeichen. Beispielsweise **2200** repräsentiert 22 Prozent und **1000** macht 10 Prozent aus.
    - **VATExemptNature** gilt nur in Fällen, in denen der Mehrwertsteuersatz 0 (null) beträgt, einschließlich der Fälle, in denen keine Steuer anfällt. Zurzeit wird **VATExemptNature** nur für Geschenkkarten unterstützt, und der Wert in der Zuordnung sollte dem Wert der **VATExemptNatureForGiftCard** -Eigenschaft in der XML-Konfigurationsdatei entsprechen.
    - **ProductType** ist die Art des Produkts, Ein Wert von **0** steht für Waren und ein Wert von **1** steht für Services.
    - **DepartmentNumber** ist die Nummer der Abteilung, die im Drucker konfiguriert ist und den vorherigen drei Attributen entspricht.

    Sie müssen die Musterzuordnung entsprechend den in Ihrer Anwendung konfigurierten Mehrwertsteuersätzen und den entsprechenden Abteilungen, die in Ihrem Fiskaldrucker konfiguriert sind, ändern.

- **Mehrwertsteuerbefreiter Charakter für Geschenkkarte** – Die Mehrwertsteuerbefreiung, die angewendet werden sollte, wenn eine Geschenkkarte ausgestellt oder aufgefüllt wird. Der Wert sollte einem Eintrag in der Zuordnung der Finanzdruckerabteilung entsprechen. Der Standardwert ist **NS**.
- **Kostenlose Artikel aktivieren** – Wenn dieser Parameter eingeschaltet ist, wird der *omaggio* Spezialrabattanpassungstyp für Artikel mit 100-Prozent-Rabatt aktiviert.
- **Infocode für Rücksendeursprung** – Der Infocode, der verwendet wird, um die Herkunft einer Retourentransaktion zu erfassen, wenn kein Originalkaufbeleg vorgelegt wird. Dieser Parameter wird zusammen mit dem **Infocode für ursprüngliches Verkaufsdatum** und **Ursprüngliche Zuordnung zurückgeben** Parameter zum Generieren einer korrekten Meldung im Fiskalbeleg über die Herkunft einer Retourentransaktion verwendet, wenn keine ursprüngliche Verkaufstransaktion vorhanden ist. 

    Dieser Infocode sollte so konfiguriert sein, dass der Benutzer eine der möglichen Retourenquellen in Ihren Filialen auswählen oder eingeben kann. Sie kann beispielsweise als Liste von Subcodes konfiguriert werden (wie **Retoure von der Website** oder **Retoure vom Kiosk**). Der **Retour-Ursprungszuordnung** Parameter wird dann verwendet, um den Wert des Infocodes in einen Befehl für den Fiskaldrucker zu übersetzen.

    Der Info-Code, der ausgewählt ist für **Infocode für Rücksendeursprung** sollte als obligatorischer Infocode konfiguriert werden, der einmal pro Verkaufsvorgang ausgelöst wird. Es sollte als zugewiesenen **Produkt zurückgeben** Info-Code im POS-Funktionsprofil zugewiesen werden, damit er ausgelöst wird, wenn der Vorgangn **Produkt zurückgeben** ausgeführt wird.

    Für diese Zuordnung ist kein Standardwert angegeben. Sie müssen einen Infocode auswählen, der in Ihrer Anwendung konfiguriert ist.

- **Infocode für Original-Verkaufsdatum** – Der Infocode, der verwendet wird, um das Original-Verkaufsdatum einer Retourentransaktion zu erfassen, wenn kein Originalkaufbeleg vorgelegt wird. Dieser Parameter wird zusammen mit dem **Infocode für ursprüngliche Retoure** und **Ursprüngliche Zuordnung der Retoure** Parameter zum Generieren einer korrekten Meldung im Fiskalbeleg über die Herkunft einer Retourentransaktion verwendet, wenn keine ursprüngliche Verkaufstransaktion vorhanden ist.

    Der Infocode sollte so konfiguriert sein, dass das **Eingabetyp** Feld auf **Datum** festgelegt ist. Es sollte als obligatorischer Infocode konfiguriert werden, der einmal pro Verkaufsvorgang ausgelöst wird. Es sollte auch als **Verknüpfter Info-Code** für den Info-Code zugewiesen werden, der für die **Infocode für Rücksendeursprung** Parameter zugewiesen ist, sodass die beiden Infocodes nacheinander abgesendet werden.

    Für diese Zuordnung ist kein Standardwert angegeben. Sie müssen einen Infocode auswählen, der in Ihrer Anwendung konfiguriert ist.

- **Mapping für Rücksendeursprung** – Mapping für Rücksendeursprung wird verwendet, um die Herkunft einer Retourentransaktion zu erfassen, wenn kein Originalkaufbeleg vorgelegt wird. Dieser Parameter wird zusammen mit dem **Infocode für Rücksendeursprung** und **Infocode für ursprüngliches Verkaufsatum** Parameter zum Generieren einer korrekten Meldung im Fiskalbeleg über die Herkunft einer Retourentransaktion verwendet, wenn keine ursprüngliche Verkaufstransaktion vorhanden ist. Das folgende Beispiel zeigt die standardmäßige Zuordnung.

    ```JSON
    {"ReturnOrigins": [
        {"ReturnOrigin":"1", "PrinterReturnOrigin":"POS"},
        {"ReturnOrigin":"2", "PrinterReturnOrigin":"ND"}
        ],
        "PrinterReturnOriginWithoutFiscalData":"POS"}
    ```

    Hier ist eine Erläuterung der Attribute dieser Zuordnung:

    - **ReturnOrigin** ist einer der möglichen Retourenquellen in Ihren Filialen. Der Wert sollte einem Wert vom **Infocode für Rücksendeursprung** Parameter entsprechen.
    - **PrinterReturnOrigin** ist einer der Rückgabeursprünge, die der Fiskaldrucker akzeptiert (**POS**, **VR**, oder **ND**).
    - **PrinterReturnOriginWithoutFiscalData** ist der Rückgabeursprung, den der Fiskaldrucker akzeptiert und der einer Rückgabetransaktion entspricht, die mit einer ursprünglichen Verkaufstransaktion verknüpft ist, die keine verknüpften Fiskaldaten enthält, da sie nicht über einen Fiskaldrucker registriert wurde. In diesem Fall wird das ursprüngliche Verkaufsdatum als das Datum des ursprünglichen Verkaufsvorgangs identifiziert.

Die folgenden Standarddatenzuordnungen sind veraltet und werden nur aus Gründen der Abwärtskompatibilität beibehalten:

- Mehrwertsteuer-(MwSt.)-Codezuordnung
- Zahlungsart für Einzahlungen

#### <a name="fiscal-connector-settings"></a>Konnektor-Einstellungen für Steuern

Die folgenden Einstellungen sind in der Konfiguration des Fiskalkonnektors enthalten, die als Teil des Beispiels für die Fiskalintegration bereitgestellt wird:

- **Endpunktadresse** – Die URL des Druckers.
- **Datum- und Uhrzeitsynchronisation** – Ein Wert, der angibt, ob Datum und Uhrzeit des Druckers mit der angeschlossenen Hardwarestation synchronisiert werden müssen.

### <a name="configure-channel-components"></a>Kanal-Komponenten konfigurieren

> [!WARNING]
> Aufgrund der Einschränkungen des [neuen unabhängigen Verpackungs- und Erweiterungsmodells](../dev-itpro/build-pipeline.md) kann es derzeit nicht für dieses Beispiel der steuerlichen Integration verwendet werden. Sie müssen die Vorgängerversion des Retail SDK auf einer Entwickler-VM in LCS verwenden. Weitere Informationen unter [Bereitstellungsrichtlinien für den Steuerdrucker-Integrationsbeispiel für Italien (Legacy)](emea-ita-fpi-sample-sdk.md).
>
> Die Unterstützung des neuen unabhängigen Paketierungs- und Erweiterungsmodells für steuerliche Integrationsmuster ist für spätere Versionen geplant.

#### <a name="set-up-the-development-environment"></a>Die Umgebung für die Entwicklung festlegen

Um eine Entwicklungsumgebung zum Testen und Erweitern des Beispiels festzulegen, gehen Sie wie folgt vor.

1. Klonen oder laden Sie das [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions) Repository herunter. Wählen Sie eine korrekte Version des Release Branch entsprechend Ihrer SDK-/Anwendungsversion. Weitere Informationen finden Sie unter [Herunterladen von Retail SDK Beispielen und Referenzpaketen von GitHub und NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Öffnen Sie die Lösung zur Integration von Fiskaldruckern unter **Dynamics365Commerce.Lösungen\\FiscalIntegration\\EpsonFP90IIIBeispiel\\EpsonFP90IIISample.sln**, und bauen Sie sie auf.
1. Installieren von CRT Erweiterungen:

    1. Suchen Sie das Installationsprogramm für die Erweiterung CRT:

        - **Commerce Scale Unit:** Im **EpsonFP90IIISample\\ScaleUnit\\ScaleUnit.EpsonFP90III.Installer\\bin\\Debug\\net461** Ordner finden Sie das **ScaleUnit.EpsonFP90III.Installer** Installationsprogramm.
        - **Lokal CRT im Modern POS:** Im **EpsonFP90IIISample\\ModernPOS\\ModernPOS.EpsonFP90III.Installer\\bin\\Debug\\net461** Ordner finden Sie das **ModernPOS.EpsonFP90III.Installer** Installationsprogramm.

    1. Starten Sie das Installationsprogramm für die CRT-Erweiterung über die Befehlszeile:

        - **Commerce Scale Unit:**

            ```Console
            ScaleUnit.EpsonFP90III.Installer.exe install --verbosity 0
            ```

        - **Lokal CRT auf Modern POS:**

            ```Console
            ModernPOS.EpsonFP90III.Installer.exe install --verbosity 0
            ```

1. Installieren Sie die Hardware Station Extensions:

    1. Im **EpsonFP90IIISample\\HardwareStation\\HardwareStation.EpsonFP90III.Installer\\bin\\Debug\\net461** Ordner finden Sie das **HardwareStation.EpsonFP90III.Installer** Installationsprogramm.
    1. Starten Sie das Installationsprogramm für die Erweiterung über die Befehlszeile:

        ```Console
        HardwareStation.EpsonFP90III.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>Produktionsumgebung

Legen Sie die Schritte unter [Einrichten einer Build-Pipeline für ein Fiskalintegrationsbeispiel](fiscal-integration-sample-build-pipeline.md) fest, um die Cloud Scale-Unit und die Self-Service bereitstellbaren Pakete für das Fiskalintegrationsbeispiel zu erzeugen und freizugeben. Die **EpsonFP90III Build-pipeline.yml** Vorlagen-YAML-Datei finden Sie im **Pipeline\\YAML_Files** Ordner des [Dynamics 365 Commerce Lösungen](https://github.com/microsoft/Dynamics365Commerce.Solutions) Repository.

## <a name="design-of-extensions"></a>Entwurf von Erweiterungen

Die Beispiele für diese Druckerintegration für Italien basiert auf der [steuerlichen Integrationsfunktionalität](fiscal-integration-for-retail-channel.md) und ist Teil der Retail SDK. Die Probe befindet sich im Ordner **src\\Fiscallntegration\\EpsonFP90IIISample** des [Dynamics 365 Commerce Lösungen](https://github.com/microsoft/Dynamics365Commerce.Solutions/) Repository (zum Beispiel [die Stichprobe in Release/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/EpsonFP90IIISample)). Das Beispiel [besteht](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) aus einem Anbieter von fiskalischen Belegen, der eine Erweiterung von CRT ist, und einem fiskalischen Konnektor, der eine Erweiterung von Commerce Hardware Station ist. Weitere Informationen über die Verwendung des Retail SDK finden Sie unter [Retail SDK Architektur](../dev-itpro/retail-sdk/retail-sdk-overview.md) und [Einrichten einer Build-Pipeline für das Independent-Packaging SDK](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Aufgrund der Einschränkungen des [neuen unabhängigen Verpackungs- und Erweiterungsmodells](../dev-itpro/build-pipeline.md) kann es derzeit nicht für dieses Beispiel der steuerlichen Integration verwendet werden. Sie müssen die Vorgängerversion des Retail SDK auf einer Entwickler-VM in LCS verwenden. Weitere Informationen unter [Bereitstellungsrichtlinien für den Steuerdrucker-Integrationsbeispiel für Italien (Legacy)](emea-ita-fpi-sample-sdk.md). Die Unterstützung des neuen unabhängigen Paketierungs- und Erweiterungsmodells für steuerliche Integrationsmuster ist für spätere Versionen geplant.

### <a name="commerce-runtime-extension-design"></a>Commerce-Laufzeiterweiterungsentwurf

Der Zweck der Erweiterung ist es, dass ein Steuerdokumentanbieter druckerspezifische Dokumente erzeugt und Antworten aus dem Steuerdrucker handhabt.

#### <a name="request-handler"></a>Anforderungshandler

Der **DocumentProviderEpsonFP90III** Anforderungshandler ist der Einstiegspunkt für die Anforderung zum Generieren von Dokumenten vom Steuerdrucker.

Der Handler wird von der Oberfläche **INamedRequestHandler** geerbt. Die Methode **HandlerName** ist für die Rückgabe des Namens des Handlers zuständig. Der Handlername sollte mit dem Name des Konnektordokumentanbieters übereinstimmen, der in der Commerce Zentralverwaltung angegeben ist.

Der Konnektor unterstützt die folgenden Anforderungen:

- **GetFiscalDocumentDocumentProviderRequest** – Diese Anforderung enthält Informationen darüber, welches Dokument generiert werden soll. Sie gibt ein druckerspezifisches Dokument zurück, dass im Steuerdrucker erfasst werden soll.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Diese Anforderung gibt die Liste der Ereignisse zurück, die Sie abonnieren können. Derzeit werden die folgenden Ereignisse unterstützt: Verkauf, X-Bericht drucken und Z-Bericht drucken.

#### <a name="configuration"></a>Variante

Die Konfigurationsdatei für den Anbieter von Steuerdokumenten befindet sich im **src\\FiscalIntegration\\EpsonFP90IIISample\\CommerceRuntime\\DocumentProvider.EpsonFP90IIISample\\Configuration\\DocumentProviderEpsonFP90IIISample.xml** im [Dynamics 365 Commerce Lösungen](https://github.com/microsoft/Dynamics365Commerce.Solutions/) Repository. Der Zweck der Datei ist es, Einstellungen zu aktivieren, damit der Dokumentanbieter von der Commerce Zentralverwaltung aus konfiguriert werden kann. Das Dateiformat wird mit den Anforderungen für die Steuerintegrationskonfiguration ausgerichtet.

### <a name="hardware-station-extension-design"></a>Hardware station-Erweiterungsentwurf

Der Zweck der Erweiterung, die ein Steuerkonnektor ist, ist die Kommunikation mit dem Steuerdrucker. Diese Erweiterung verwendet das HTTP-Protokoll, um Dokumente, die die CRT-Erweiterung generiert, zum Steuerdrucker zu übermitteln. Sie handhabt auch die Antworten, die vom Steuerdrucker empfangen werden.

#### <a name="request-handler"></a>Anforderungshandler

Der Anforderungshandler **EpsonFP90IIISample** ist der Einstiegspunkt für die Handhabung der Anforderung an das Steuererfassungsgerät.

Der Handler wird von der Oberfläche **INamedRequestHandler** geerbt. Die Methode **HandlerName** ist für die Rückgabe des Namens des Handlers zuständig. Der Handlername sollte mit dem Name des Steuerkonnektors übereinstimmen, der in der Commerce Zentralverwaltung angegeben ist.

Der Konnektor unterstützt die folgenden Anforderungen:

- **SubmitDocumentFiscalDeviceRequest** – Diese Anforderung sendet Dokumente an den Drucker und gibt eine Antwort vom Steuerdrucker zurück.
- **IsReadyFiscalDeviceRequest** – Diese Anforderung wird für eine Integritätsprüfung des Steuererfassungsgeräts verwendet.
- **InitializeFiscalDeviceRequest** – Diese Anforderung wird für Initialisierung des Druckers verwendet.

#### <a name="configuration"></a>Variante

Die Konfigurationsdatei für den Anbieter von Steuerkonnektoren befindet sich unter **src\\FiscalIntegration\\EpsonFP90IIISample\\HardwareStation\\EpsonFP90IIIFiscalDeviceSample\\Configuration\\ConnectorEpsonFP90IIISample.xml** im [Dynamics 365 Commerce Lösungen](https://github.com/microsoft/Dynamics365Commerce.Solutions/) Repository. Der Zweck dieser Datei ist es, Einstellungen zu aktivieren, damit der Konnektor von der Commerce Zentralverwaltung aus konfiguriert werden kann. Das Dateiformat wird mit den Anforderungen für die Steuerintegrationskonfiguration ausgerichtet.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
