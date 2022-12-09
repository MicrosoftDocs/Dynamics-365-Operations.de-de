---
title: Übersicht über den Dynamics 365 Payment Connector für Adyen
description: Dieser Artikel bietet einen Überblick über Microsoft Dynamics 365 Payment Connector für Adyen.
author: rassadi
ms.date: 11/16/2022
ms.topic: overview
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2019-01-01
ms.openlocfilehash: 58d88e023b73ce19331bd6f54644a62d8f6f35af
ms.sourcegitcommit: 3aa3dedc3123cb079614762e2718841c2f7d7d35
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/30/2022
ms.locfileid: "9812085"
---
# <a name="dynamics-365-payment-connector-for-adyen-overview"></a>Übersicht über den Dynamics 365 Payment Connector für Adyen

[!include [banner](../includes/banner.md)]

Dieser Artikel gibt einen Überblick über den Microsoft Dynamics 365 Payment Connector für Adyen und enthält eine umfassende Liste der unterstützten Features und Funktionen. Verwandte Artikel behandeln die Anmeldung bei Adyen, die Konfiguration des Connectors, häufig gestellte Fragen und Anleitungen zur Fehlerbehebung bei einigen häufigen Problemen.

## <a name="key-terms"></a>Schlüsselbegriffe

| Zeitdauer | Description |
|---|---|
| Connector für Zahlungen | Eine Erweiterung, die die Kommunikation zwischen Microsoft Dynamics 365 Commerce (und dazugehörigen Komponenten) und einem Zahlungsservice. Der Connector, der in diesem Artikel beschrieben wird, wurde durch das Standardzahlungs-Software-Development-Kit (SDK) implementiert. |
| Karte vorhanden | Bezieht sich auf Zahlungstransaktionen, in denen eine physischen Karte vorgelegt und auf einem Zahlungsterminal-Connector die Dynamics 365 Verkaufsstelle verwendet wird. |
| Karte nicht vorhanden | Bezieht sich auf Zahlungstransaktionen, bei denen keine physische Karte vorgelegt wird, wie z. B. E-Commerce- oder Callcenter-Szenarien. In diesem Szenario werden die den Zahlungen zugeordneten Informationen manuell auf eine E-Commerce-Website, in einen Callcenter-Flow oder in der Verkaufsstelle oder dem Zahlungsterminal eingegeben. |

## <a name="supported-features-functionality-versions-and-terminals"></a>Unterstützte Features, Funktionen, Versionen und Terminals

Der sofort einsatzbereite Dynamics 365 Payment Connector für Adyen verwendet das Standardzahlungs-SDK. Daher verfügt er über keine speziellen Funktionen, die nicht auch anderen Zahlungs-Connectoren zur Verfügung stehen.

### <a name="supported-versions"></a>Unterstützten Versionen

#### <a name="microsoft-dynamics-365-supported-versions"></a>Unterstützte Microsoft Dynamics 365 Versionen
Der sofort einsatzbereite Dynamics 365 Payment Connector für Adyen von Erstanbietern wird ab der Microsoft Dynamics 365 Finance-Version 8.1.3 (Januar 2019) und ab der Microsoft Dynamics 365 Retail Version 8.1.3 unterstützt. Drittanbieter können jedoch weiterhin andere Zahlungs-Connectors für Adyen für frühere Versionen von Microsoft Dynamics 365 entwickeln.

#### <a name="supported-adyen-firmware-versions"></a>Unterstützte Adyen-Firmwareversionen

Die folgende Liste beschreibt die minimalen und maximalen Adyen-Firmwareversionen, die für jede Version des Microsoft Dynamics 365 Retail POS unterstützt werden.

---

# <a name="10025"></a>[10.0.25](#tab/10-0-25)
### <a name="dynamics-365-retail-pos-version-10025"></a>Dynamics 365 Retail POS-Version 10.0.25
| Mindestversion der Adyen-Firmware | Höchstversion der Adyen-Firmware |
| --- | --- |
| adyen_v1_71p16 | adyen_v1_73p6 |

# <a name="10026"></a>[10.0.26](#tab/10-0-26)
### <a name="dynamics-365-retail-pos-version-10026"></a>Dynamics 365 Retail POS-Version 10.0.26
| Mindestversion der Adyen-Firmware | Höchstversion der Adyen-Firmware |
| --- | --- |
| adyen_v1_73p6 | adyen_v1_75p13 |

# <a name="10027"></a>[10.0.27](#tab/10-0-27)
### <a name="dynamics-365-retail-pos-version-10027"></a>Dynamics 365 Retail POS-Version 10.0.27
| Mindestversion der Adyen-Firmware | Höchstversion der Adyen-Firmware |
| --- | --- |
| adyen_v1_73p6 | adyen_v1_75p13 |

# <a name="10028"></a>[10.0.28](#tab/10-0-28)
### <a name="dynamics-365-retail-pos-version-10028"></a>Dynamics 365 Retail POS-Version 10.0.28
| Mindestversion der Adyen-Firmware | Höchstversion der Adyen-Firmware |
| --- | --- |
| adyen_v1_73p6 | adyen_v1_75p22 |

# <a name="10029"></a>[10.0.29](#tab/10-0-29)
### <a name="dynamics-365-retail-pos-version-10029"></a>Dynamics 365 Retail POS-Version 10.0.29
| Mindestversion der Adyen-Firmware | Höchstversion der Adyen-Firmware |
| --- | --- |
| adyen_v1_71p16 | adyen_v1_78p6 |

# <a name="10030"></a>[10.0.30](#tab/10-0-30)
### <a name="dynamics-365-retail-pos-version-10030"></a>Dynamics 365 Retail POS-Version 10.0.30
| Mindestversion der Adyen-Firmware | Höchstversion der Adyen-Firmware |
| --- | --- |
| adyen_v1_71p16 | adyen_v1_78p6 |

---

> [!NOTE]
> Adyen kann kleinere Versionsaktualisierungen veröffentlichen, nachdem Microsoft die Hauptversion getestet hat. Solange eine Hauptversion unterstützt wird, ist es in Ordnung, Nebenversionsaktualisierungen innerhalb derselben Hauptversion zu haben. Diese Aktualisierungen sind normalerweise sehr zielgerichtete Korrekturen und erfüllen nicht die Messlatte für einen vollständigen erneuten Test, solange dieselbe Hauptfirmwareversion zuvor getestet wurde. Updates sollten die in der Dokumentation aufgeführte maximale Adyen-Firmwareversion nicht überschreiten. 
>
> Für die Migration von einer Adyen-Firmwareversion von vor Version 53 auf Version 53 ist POS KB **4577957** für monatliche Updates von Commerce, Versionen 10.0.11 bis 10.0.14, erforderlich. Wenn eine dieser Versionen verwendet wird und den Hotfix nicht enthält, sind nach der Aktualisierung des Zahlungsterminals nur Zahlungen über NFC möglich. Das Anwenden des Hotfixes auf den POS behebt dieses Problem. Wenn die POS-Version älter als Version 10.0.11 ist, reichen Sie eine Supportanfrage ein und geben Sie an, dass eine Korrektur für KB **4577957** für ein außer Betrieb befindliches MPOS erforderlich ist.
> 
> Für die Adyen-Firmware-Versionen 59p7 bis 62p9 fordert der Vorgang **Geschenkkarte auszahlen** zweimal die Eingabe der PIN in Szenarien, in denen die Geschenkkarte manuell eingegeben wird. Dieses Problem wird nicht reproduziert, wenn die Geschenkkarte durch das Lesegerät gezogen wird. Adyen untersucht dies. 

### <a name="supported-payment-terminals"></a>Unterstützte Zahlungsterminals
Der Dynamics 365 Payment Connector für Adyen nutzt die geräteunabhängige [Adyen-Zahlungsterminal-API](https://www.adyen.com/blog/introducing-the-terminal-api). Es unterstützt alle Zahlungsterminals, die diese Anwendungsprogrammierschnittstelle (API) unterstützt. Eine vollständige Liste der unterstützten Zahlungsterminals finden Sie auf der Seite [Adyen POS Terminals](https://www.adyen.com/pos-payments/terminals).

Das folgende Video beschreibt die Fähigkeiten des Adyen Castles SE1 Android Zahlungsterminals.


> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE5bKeM]

### <a name="supported-payment-instruments"></a>Unterstützte Zahlungsmittel

#### <a name="supported-debit-and-credit-cards"></a>Unterstützte Debit- und Kreditkarten

| Marke | Variante | Karte vorhanden | e-Geschäftsverkehr | Callcenter |
|---|---|:-:|:-:|:-:|
| MasterCard | Gutschrift | ✔ | ✔ | ✔ |
| MasterCard | Belastung | ✔ | ✔ | ✔ |
| MasterCard | Alpha-Bank-Bonus | ✔ | ✔ | ✔ |
| MasterCard | Apple Pay | ✔ |  |  |
| MasterCard | Samsung Pay | ✔ |  |  |
| MasterCard | Maestro | ✔ | ✔ | ✔ |
| MasterCard | Maestro Samsung Pay | ✔ |  |  |
| MasterCard | Maestro Vereinigtes Königreich | ✔ | ✔ | ✔ |
| VISA | Gutschrift | ✔ | ✔ | ✔ |
| VISA | Belastung | ✔ | ✔ | ✔ |
| VISA | Alpha-Bank-Bonus | ✔ | ✔ | ✔ |
| VISA | Android Pay | ✔ |  |  |
| VISA | Apple Pay | ✔ |  |  |
| VISA | Samsung Pay | ✔ |  |  |
| VISA | VISA Checkout | ✔ | ✔ | ✔ |
| VISA | VISA Dankort | ✔ | ✔ | ✔ |
| VISA | VISA Hipotecario | ✔ | ✔ | ✔ |
| VISA | VISA-Aravia-Karte | ✔ | ✔ | ✔ |
| AMEX | Gutschrift | ✔ | ✔ | ✔ |
| AMEX | Belastung | ✔ | ✔ | ✔ |
| AMEX | Android Pay | ✔ |  |  |
| AMEX | Apple Pay | ✔ |  |  |
| AMEX | Samsung Pay | ✔ |  |  |
| AMEX | AMEX Gewerbekunden | ✔ | ✔ | ✔ |
| AMEX | AMEX Privatkunden | ✔ | ✔ | ✔ |
| AMEX | AMEX Unternehmenskunden | ✔ | ✔ | ✔ |
| AMEX | AMEX kleine Unternehmen | ✔ | ✔ | ✔ |
| Erkennen | Standard | ✔ | ✔ | ✔ |
| Erkennen | Android Pay | ✔ |  |  |
| Erkennen | Apple Pay | ✔ |  |  |
| Erkennen | Samsung Pay | ✔ |  |  |
| Diners | Standard | ✔ | ✔ | ✔ |
| Dineromail | Standard | ✔ | ✔ | ✔ |
| JCB | Standard | ✔ | ✔ | ✔ |
| Union Pay\* | Standard | ✔ |  |  |
| Interac Debit\* | Standard | ✔ |  |  |

\*Adyen stellt keine wiederkehrenden Interac- und Union-Pay-Karten-Token bereit, daher können sie für Transaktionen ohne vorgelegte Karte nicht unterstützt werden.

#### <a name="supported-gift-cards"></a>Unterstützte Geschenkkarten
| Schema | Karte vorhanden | Karte nicht vorhanden |
|---|:-:|---|
| Givex | ✔ | ✔ |
| SVS | ✔ | ✔ |

Um diese externen Geschenkkartensysteme über den Dynamics 365 Payment Connector für Adyen zu unterstützen, müssen Sie zusätzliche Schritte ausführen. Weitere Informationen finden Sie unter [Externe Geschenkkarten unterstützen](/dynamics365/unified-operations/retail/dev-itpro/gift-card).

#### <a name="supported-wallets"></a>Unterstützte Wallets

| Schema | Karte vorhanden | Karte nicht vorhanden |
|---|---|---|
| Alipay | Diese Funktion wird in einer späteren Version unterstützt. | Nein |
| WeChat | Diese Funktion wird in einer späteren Version unterstützt. | Nein |

#### <a name="supported-card-present-input-methods"></a>Unterstützte Eingabemethoden mit vorgelegter Karte
| Eingabemethode | Unterstützt | Notizen |
|---|:-:|---|
| Einstecken | ✔ | |
| Karte durch Lesegerät ziehen | ✔ | |
| Antippen | ✔ | |
| Manuelle Eingabe über die POS-Benutzeroberfläche. |  | Wird derzeit nicht unterstützt |
| Manuelle Eingabe über das Zahlungsterminal. | ✔ | Unterstützt die manuelle Eingabe von Kredit-, Debit- und Geschenkkarten mit PIN-Eingabe. | 


#### <a name="supported-card-present-countries"></a>Unterstützte Länder mit vorgelegter Karte

In den folgenden Ländern stehen derzeit Commerce-Komponenten mit vorgelegter Karte von Adyen zur Verfügung. Informationen zur aktuellen internationalen Verfügbarkeit von Commerce finden Sie auf der Seite der [internationalen Verfügbarkeit](/dynamics365/get-started/availability).

| Land | Unterstützt |
| --- | :-: |
| Australien | ✔ |
| Österreich | ✔ |
| Belgien | ✔ |
| Kanada | ✔ |
| Tschechische Republik | ✔ |
| Dänemark | ✔ |
| Estland | ✔ |
| Finnland | ✔ |
| Frankreich | ✔ |
| Deutschland | ✔ |
| Hongkong SAR | ✔ |
| Ungarn | ✔ |
| Island | ✔ |
| Irland | ✔ |
| Italien | ✔ |
| Japan | Zukünftige Versionen |
| Lettland | ✔ |
| Litauen | ✔ |
| Malaysia | ✔ |
| Niederlande | ✔ |
| Neuseeland | ✔ |
| Norwegen | ✔ |
| Polen | ✔ |
| Singapur | ✔ |
| Schweiz | ✔ |
| Spanien | ✔ |
| Schweden | ✔ |
| Schweiz | ✔ |
| Vereinigtes Königreich | ✔ |
| USA | ✔ |
| Brasilien | Zukünftige Versionen |

#### <a name="supported-card-not-present-countries"></a>Aktuelle Länder mit nicht vorgelegter Karte

Die folgenden Länder werden von Adyen für Transaktionen ohne vorgelegte Karte unterstützt. [Wenden Sie sich an Adyen](https://www.adyen.com/contact/sales), um Details zur Unterstützung für ein bestimmtes Land zu erhalten. Informationen zur aktuellen internationalen Verfügbarkeit von Commerce finden Sie auf der Seite der [internationalen Verfügbarkeit](/dynamics365/get-started/availability).

| Land | 
| --- |
| Argentinien |
| Armenien |
| Australien |
| Österreich |
| Bahrain |
| Belgien |
| Brasilien |
| Bulgarien |
| Kanada |
| Chile |
| China |
| Kolumbien |
| Kroatien |
| Zypern |
| Tschechische Republik  |
| Dänemark |
| Ägypten |
| Estland |
| Finnland |
| Frankreich |
| Georgien |
| Deutschland |
| Gibraltar |
| Griechenland |
| Guernsey |
| Hongkong SAR |
| Ungarn |
| Island |
| Indien |
| Indonesien |
| Irland |
| Isle of Man |
| Israel |
| Italien |
| Japan |
| Jersey |
| Südkorea |
| Kuwait |
| Lettland |
| Litauen |
| Luxemburg |
| Malaysia |
| Malta |
| Mexiko |
| Marokko |
| Niederlande |
| Neuseeland |
| Norwegen |
| Peru |
| Polen |
| Portugal |
| Katar |
| Rumänien |
| Saudi-Arabien |
| Serbien |
| Singapur |
| Slowakei |
| Slowenien |
| Südafrika |
| Spanien |
| Schweden |
| Schweiz |
| Taiwan |
| Tansania |
| Thailand |
| Türkei |
| Vereinigte Arabische Emirate (VAE) |
| Vereinigtes Königreich |
| Vereinigte Staaten von Amerika einschließlich Puerto Rico  |

#### <a name="supported-dynamics-365-payment-features"></a>Unterstützte Zahlungsfunktionen von Dynamics 365

Die folgende Tabelle zeigt den Funktionssatz, den der Dynamics 365 Payment Connector für Adyen unterstützt. Diese Funktionen verwenden Verbesserungen, die im Dezember 2018 im Zahlungs-SDK und einigen Komponenten eingeführt wurden. Sie sind nicht exklusiv für den Dynamics 365 Payment Connector für Adyen. Weitere Informationen zur Übernahme dieser Verbesserungen für einen anderen Zahlungs-Connector finden Sie unter [Zahlungsintegration für ein End-to-End-Zahlungsterminal erstellen](/dynamics365/unified-operations/retail/dev-itpro/end-to-end-payment-extension).

| Schema | Karte vorhanden | Karte nicht vorhanden |
|---|:-:|:-:|
| [Saldo Geschenkkarten-Barauszahlung](/dynamics365/unified-operations/retail/dev-itpro/gift-card-cash-out) | ✔ | |
| [Vermeidung doppelter Zahlungen](/dynamics365/unified-operations/retail/duplicate-payment-protection) | ✔ | |
| Omnichannel-Tokenisierung | ✔ | ✔ |
| Verknüpfte Rückerstattungen | ✔<br>(Ab 10.0.1) | ✔<br>(Ab 10.0.1) |
| [Online-Zahlungen speichern](../dev-itpro/adyen-connector-listPI.md) | | ✔<br>(Ab 10.0.2) | 
| [Externe Geschenkkarten für Callcenter und E-Commerce](./gift-card.md) | ✔<br>(Ab 10.0.10) | 
| [SCA-Zahlungsumleitung](../adyen_redirect.md) | | ✔<br>(Ab 10.0.12) |
| [Spezielle Zahlungsterminals und Eingabeaufforderungen für Drucker und Kassenschublade](../pos-multi-hws.md) | ✔<br>(Ab 10.0.12) | |
| [Trinkgeldunterstützung auf SDK-Ebene durch den Adyen-Connector](tipping.md) | ✔<br>(Ab 10.0.14) | |
| [Inkrementelle Erfassung zur Auftragsrechnungsstellung](incremental-capture.md) |  | ✔<br>(Ab 10.0.18) |
| [Wallet-Zahlungen](../wallets.md) |  | ✔<br>(Ab 10.0.20) |
| [Google Pay mit Adyen](google-pay-adyen.md) |  | ✔<br>(Ab 10.0.27) |

## <a name="next-steps"></a>Nächste Schritte

Weitere Informationen über die Anmeldung und das Konfigurieren des Dynamics 365 Payment Connectors für Adyen finden Sie unter [Dynamics 365 Payment Connector für Adyen](adyen-connector-setup.md).

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Dynamics 365 Payment Connector für Adyen einrichten](adyen-connector-setup.md)

[Häufig gestellte Fragen zum Dynamics 365 Payment Connector für Adyen](adyen-connector-faq.md)

[Fehler im Zusammenhang mit dem Dynamics 365 Payment Connector für Adyen beheben](adyen-connector-troubleshoot.md)

[FAQs zu Zahlungen](/dynamics365/unified-operations/retail/dev-itpro/payments-retail)

[!INCLUDE [footer-include](../../includes/footer-banner.md)]
