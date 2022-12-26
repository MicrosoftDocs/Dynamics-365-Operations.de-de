---
title: Apple Pay mit Adyen in Dynamics 365 Commerce einrichten
description: Dieser Artikel beschreibt, wie Sie Apple Pay mit Adyen in Microsoft Dynamics 365 Commerce einrichten.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2022-06-20
ms.openlocfilehash: 896847cee696e221b2114f7f28a0b56e73fc911b
ms.sourcegitcommit: bdee5e642d417a13abdb778c14ec5f2dbbf8dee7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2022
ms.locfileid: "9838228"
---
# <a name="set-up-apple-pay-with-adyen-in-dynamics-365-commerce"></a>Apple Pay mit Adyen in Dynamics 365 Commerce einrichten

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Dieser Artikel beschreibt, wie Sie Apple Pay mit Adyen in Microsoft Dynamics 365 Commerce einrichten.

## <a name="key-terms"></a>Schlüsselbegriffe

| Zeitdauer | Description |
|---|---|
| Apple Pay | Apple Pay, auch bekannt als die Apple Pay „Schaltfläche“, ist ein Wallet-Zahlungsangebot, das über den Adyen-Konnektor unterstützt wird. Es ermöglicht das Debitor-Erlebnis und die Integration, die vom Microsoft Dynamics 365 Apple Connector unterstützt werden. |
| Brieftasche | Eine Zahlungsart, die keine traditionellen Zahlungsmerkmale enthält, wie z.B. den Bereich der Bankleitzahl (BLZ) und das Ablaufdatum, die zur Unterscheidung von Kredit- und Debitkarten verwendet werden. |

Dynamics 365 Commerce bietet eine standardmäßige Integration für Apple Pay, wenn der Adyen Payment Gateway Service verwendet wird. Apple Pay ist eine digitale Brieftaschen-Zahlungsmethode, die ein Apple Pay-Händlerkonto in Abstimmung mit dem Adyen-Zahlungsdienst verwendet. Wenn sie konfiguriert ist, ist die Schaltfläche Apple Pay eine auswählbare Zahlungsmethode, die Teil der der Kaufabwicklungsseite eines Online-Händlers ist. Die Apple Pay-Schaltfläche wird nur für unterstützte Apple Pay-Geräte als Zahlungsoption angezeigt. Wenn Benutzer **Apple Pay** in einem unterstützten Browser oder Gerät auswählen, werden sie an den Apple Pay-Dienst weitergeleitet, um ihre Zahlung direkt abzuschließen. Sie werden dann zum Online-Store zurückgeleitet, um die Bestellung abzuschließen.

Die Referenz des Dynamics 365 Payment Connector for Apple Pay Konnektors wird zusätzlich zum Dynamics 365 Payment Connector for Adyen verwendet, um Apple Pay und Kreditkartenzahlungen auf einer Seite zu aktivieren. Apple Pay kann auch für die Verwendung in Geschäften konfiguriert werden, die über Adyen-Zahlungsterminals verfügen, die den Dynamics 365 Payment Connector für Adyen mit dem Commerce Point of Sale (POS) verwenden. In diesem Fall verarbeitet der Dynamics 365 Payment Connector for Adyen den Tap des Apple Payment-Geräts über das Terminal.

## <a name="prerequisites"></a>Voraussetzungen

Ein Apple-Händlerkonto muss Apple Pay mit Ayden in Commerce verwenden. Informationen zur Einrichtung von Apple Pay in Ihrem Testkundenbereich finden Sie unter [Apple Pay Drop-in-Integration](https://docs.adyen.com/payment-methods/apple-pay/web-drop-in#set-up-apple-pay). Informationen dazu, was zu tun ist, wenn Sie bereit sind, in Ihrer Produktionsumgebung live zu gehen, finden Sie unter [Live gehen](https://docs.adyen.com/payment-methods/apple-pay/web-drop-in#going-live).

Die Zahlungsmethode Apple Pay muss auch in Ihr Adyen-Konto integriert werden. Adyen kann Ihnen dabei helfen, die Zahlungsmethode einzurichten und sicherzustellen, dass die Domains, für die Sie das Zertifikat verwenden, für die Verwendung mit dem Zertifikat zugewiesen werden.

Um die Funktionsflag „Erweiterte Brieftasche“ in Commerce headquarters zu aktivieren, gehen Sie zu **Arbeitsbereiche \> Funktionsverwaltung**, und suchen Sie nach der Funktion **Erweiterte Wallet-Unterstützung und Zahlungsverbesserungen**. Wählen Sie die Funktion aus und wählen Sie dann **Aktivieren** aus. Nachdem die Funktion aktiviert wurde, führen Sie den **1110** Verteilungsplan aus, um die Änderung in allen Kanälen verfügbar zu machen.

## <a name="map-the-apple-pay-payment-method"></a>Zuordnung der Zahlungsmethode Apple Pay

Apple Pay ist eine Zahlungsmethode für digitale Brieftaschen. Informationen darüber, wie Sie die Zuordnung von Zahlungen für Apple Pay festlegen, finden Sie unter [Wallet-Zahlungsunterstützung](../wallets.md).

Um die Apple Pay-Zahlungsmethode in Commerce headquarters zuzuordnen, führen Sie diese Schritte aus.

1. Gehen Sie zu **Einzelhandel und Handel \> Kanaleinstellung \> Zahlungsmethoden \> Kartentypen**.
1. Wählen Sie **Neu** aus, um eine Position für Apple Pay hinzuzufügen, und legen Sie die folgenden Werte fest:

    - **ID:** ApplePay
    - **Name des elektronischen Zahlungsverkehrs:** Apple Pay
    - **Typ:** Wallet
    - **Aussteller:** Apple

1. Wählen Sie im **Prozessorzuordnung**, um das Dialogfeld **Prozessor-Zahlungszuordnungsmethoden** zu öffnen. Die Spalte **Zahlungsmethoden für nicht zugeordnete Prozessoren** listet die unterstützten Zahlungsmethoden für jeden verfügbaren Connector (Adyen, PayPal und Apple) auf.
1. Ordnen Sie die unterstützten Zahlungsmethoden zu, die Sie für den Connector **Dynamics 365 Payment Connector für Adyen** (zur Verwendung am POS) als auch den **Dynamics 365 Payment Connector für Apple Pay** (für den Online-Kanal) möchten.
1. Für jede Mapping-Zeile in der Spalte **Zahlungsmethoden für nicht zugeordnete Prozessoren** wählen Sie die zu unterstützende Linie aus, und wählen Sie dann **Hinzufügen**, um die Auswahl zur Spalte **Zahlungsmethoden für zugeordnete Prozessoren** zu verschieben.
1. Wählen Sie **OK**, und dann auf der Seite **Kartentypen** die Option **Speichern**.

## <a name="set-up-the-apple-pay-certificate-for-your-site"></a>Richten Sie das Apple Pay-Zertifikat für Ihre Website ein

Für jede Website müssen Sie die Domänenzuordnungsdatei (auch bekannt als Apple Pay-Zertifikat) hochladen, wie in [Adyen Apple Pay-Dokumentation](https://docs.adyen.com/payment-methods/apple-pay/web-drop-in#going-live) beschrieben. Sie können den Commerce Site Builder verwenden, um die Domänenzuordnungsdatei in die Medienbibliothek für Ihre Site hochzuladen.

Führen Sie die folgenden Schritte aus, um das Apple Pay-Zertifikat einzurichten.

1. Laden Sie das Zertifikat (Domänenzuordnungsdatei) von [Adyen](https://docs.adyen.com/payment-methods/apple-pay/web-drop-in#going-live) herunter.
1. Fügen Sie der Domänenzuordnungsdatei die Erweiterung .txt hinzu.
1. Im Website-Builder [hochladen](../upload-serve-static-files.md) die Domänenzuordnungsdatei in die Medienbibliothek Ihrer Website.
1. Gehen Sie zu **URLs**.
1. Wählen Sie **Neu \> Neue URL** aus.
1. Im Dialogfeld **Neue URL** wählen Sie **Medienbibliotheksobjekt** aus.
1. Im Feld **URL-Pfad** geben Sie den URL-Pfad ein (sofern noch nicht geschehen). Geben Sie nach der Domain-Basis-URL die folgende erforderliche Apple-Zeichenfolge ein: `<domain>/.well-known/apple-developer-merchantid-domain-association.txt`.
1. Wählen Sie **Weiter**. Die Medienbibliothek zeigt alle Medienobjekte des Typs **Dokument** (.txt) an.
1. Wählen Sie die Domänenzuordnungsdatei aus, die für Anforderungen an die von Ihnen zuvor definierte URL bedient werden soll.
1. Wählen Sie **Erstellen** aus.

An diesem Punkt ist die URL, die Sie erstellt haben, in einem Entwurfzustand. Veröffentlichen Sie die URL, um den Prozess abzuschließen. Die Datei, auf die die URL verweist, wird erst zurückgegeben, wenn Sie die URL veröffentlichen.

## <a name="configure-a-commerce-online-store-for-apple-pay"></a>Konfigurieren Sie einen Commerce Online Store für Apple Pay

Um einen Commerce Store für die Verwendung von Apple Pay zu konfigurieren, gehen Sie folgendermaßen vor.

1. In der Commerce headquarters gehen Sie zu **Einzelhandel und Commerce \> Kanäle \> Online Stores**.
1. Wählen Sie den Wert **Retail Channel ID** des Online Store-Kanals Ihrer Website.
1. Fügen Sie im Inforegister **Zahlungskonten** den Connector **Dynamics 365 Payment Connector für Adyen** hinzu, falls er noch nicht eingerichtet ist, indem Sie den Anweisungen in [Richten Sie Dynamics 365 Payment Connector für Adyen ein](adyen-connector-setup.md) folgen.
1. Wählen Sie nach der Konfiguration des Adyen-Connectors **Hinzufügen** aus, um den Connector **Dynamics 365 Payment Connector für Apple Pay** hinzuzufügen.
1. Geben Sie Werte für die Händlereigenschaften des Connectors ein.

    | Eigenschaft               | Description | Erforderlich | Automatisch festgelegt auf | Beispielwert |
    | ---------------------- | ----------- | -------- | ----------------- | ------------ |
    | Assemblyname          | Der Name der Assembly für den Dynamics 365 Payment Connector for Apple Pay. | Ja | Ja | Binärname |
    | Dienstkontokennung     | Die eindeutige Kennung für die Einrichtung der Händlereigenschaften. Diese Kennung wird auf Zahlungstransaktionen gestempelt und identifiziert die Eigenschaften des Händlers, die nachgelagerte Prozesse (z.B. die Rechnungsstellung) verwenden sollten. | Ja | Ja | Guid |
    | Einzelhändlerkontokennung    | Geben Sie die eindeutige Adyen-Händler-Kennung ein. Dieser Wert wird angegeben, wenn Sie sich bei Adyen anmelden, wie unter [Anmelden bei Adyen](adyen-connector-setup.md#sign-up-with-adyen) beschrieben. | Ja | Nein | MerchantIdentifier |
    | Cloud-API-Schlüssel          | Geben Sie den Adyen Cloud API-Schlüssel ein. Sie können diesen Schlüssel erhalten, indem Sie den Anweisungen unter [Wie Sie den API-Schlüssel erhalten](https://docs.adyen.com/developers/user-management/how-to-get-the-api-key) folgen. | Ja | Nein | abcdefg |
    | Gatewayumgebung    | Geben Sie die Adyen Gateway Umgebung ein, die zugeordnet werden soll. Die möglichen Werte sind **Test** und **Live**. Sie sollten dieses Feld nur für Produktionsgeräte und Transaktionen auf **Live** festlegen. | Ja | Ja | Live |
    | Unterstützte Währungen   | Geben Sie die Währungen ein, die der Konnektor verarbeiten soll. In Szenarien mit Kartenzahlung kann Adyen über [Dynamische Währungsumrechnung](https://www.adyen.com/pos-payments/dynamic-currency-conversion) zusätzliche Währungen unterstützen, nachdem die Transaktionsanforderung an das Zahlungsterminal gesendet wurde. Wenden Sie sich an den Adyen-Support, um eine Liste der unterstützten Währungen zu erhalten. | Ja | Ja | USD;EUR |
    | Unterstützte Zahlungsmitteltypen | Geben Sie die Ausschreibungsarten ein, die der Konnektor verarbeiten soll. | Ja | Ja | ApplePay |

1. Nachdem die Händlerinformationen eingegeben wurden, führen Sie den **1070** Zeitplanjob für die Kanalkonfigurationsverteilung aus.


### <a name="configure-content-security-policies-in-site-builder"></a>Konfigurieren Sie Inhaltssicherheitsrichtlinien im Site Builder

Bevor Sie Ihre Fragmente oder Seiten mit Apple Pay konfigurieren, müssen Sie sicherstellen, dass die Sicherheitsrichtlinien (CSPs) für Ihre Website in Commerce Site Builder konfiguriert sind.

Gehen Sie folgendermaßen vor, um Richtlinien für die Inhaltssicherheit in Site Builder zu konfigurieren.

1. Gehen Sie zu **Seiteneinstellungen \> Erweiterungen**.
1. Wählen Sie auf der Registerkarte **Sicherheitsrichtlinie für Inhalte** die Option **Hinzufügen**, um eine Position mit `https://applepay.cdn-apple.com/jsapi/v1/apple-pay-sdk.js` zu den Abschnitten **child-src**, **connect-src**, **frame-src**, **img-src**, **script-src**, und **style-src** hinzuzufügen.
1. Wählen Sie, wenn Sie fertig sind, **Speichern und veröffentlichen**, um die Änderungen zu speichern.

### <a name="set-up-apple-pay-as-a-checkout-payment-option"></a>Richten Sie Apple Pay als Zahlungsoption an der Kasse ein

Führen Sie die folgenden Schritte aus, um Apple Pay als Checkout-Zahlungsoption auf der (nicht Express-) Checkout-Seite Ihrer Website einzurichten.

1. Gehen Sie im Site Builder zu **Fragmente** und wählen Sie das Kassenfragment Ihrer Website aus.
1. Wählen Sie **Bearbeiten** aus.
1. Auf der neuen Seite wählen Sie **Kassenbereichcontainer**-Slot und wählen dann die Ellipsen (**...**) und wählen **Modul hinzufügen**.
1. Wählen Sie im Dialogfeld **Module auswählen** das Modul **Apple Pay** und dann **OK** aus.
1. Wählen Sie **Speichern** aus.
1. Wählen **Bearbeiten beenden**, um das Fragment einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.

Einstellungen für das **ApplePay** Modul sind in das Modul integriert und verbinden sich mit dem konfigurierten Dynamics 365 Payment Connector für Apple Pay Connector, der für den Online-Kanal in Commerce headquarters eingerichtet ist.

### <a name="apple-pay-payment-behavior"></a>Apple Pay Zahlungsverhalten

Die **ApplePay** Zahlungsschaltfläche wird nur auf unterstützten Apple Pay-Geräten (iPhones, iPads und Safari-Browsern, die Apple Pay unterstützen) angezeigt. Wenn ein Benutzer eines dieser Geräte nicht verwendet, wird die **ApplePay** Zahlungsschaltfläche nicht sichtbar.

Wenn ein Benutzer die Zahlungsschaltfläche **ApplePay** auswählt, wird ein **ApplePay** Dialogfeld angezeigt. Dort kann sich der Benutzer gegenüber seinem Apple Pay-Gerät oder Browser authentifizieren. Das **ApplePay** Dialogfeld zeigt eine Zusammenfassung des Bestellbetrags und der Zahlungsmethode, die der Benutzer für sein Apple Wallet konfiguriert hat. Der Benutzer kann diese Details überprüfen und dann **Zahlen** auswählen, um die Zahlung abzuschließen. Nachdem die Zahlung abgeschlossen ist, wird der Benutzer zur **Bestellung ausgeführt** Webeite weitergeleitet, die eine detaillierte Bestellzusammenfassung für die abgeschlossene Transaktion anzeigt.

## <a name="configure-commerce-pos-for-apple-pay"></a>Konfigurieren Sie Commerce POS für Apple Pay

Die POS-Konfiguration verwendet die Konfiguration des Feldes **EFT-Service** des Hardwareprofils für den Dynamics 365 Payment Connector for Adyen. In Commerce headquarters konfigurieren Sie den EFT-Dienst für Dynamics 365 Payment Connector für Adyen wie beschrieben in [Einrichten eines Dynamics 365 POS-Hardwareprofils](adyen-connector-setup.md#set-up-a-dynamics-365-pos-hardware-profile).

Stellen Sie sicher, dass Sie **ApplePay** zur Liste der Ausschreibungsarten im Feld **Unterstützte Zahlungsmitteltypen** hinzufügen. Verwenden Sie Semikolons (;), um Zahlungsmitteltypen in der Liste zu trennen.

Die Prozessor-Zuordnung für den Adyen Konnektor erfasst die Wallet-Kartentypen, die von Apple Pay am POS Terminal verwendet werden.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[FAQs zu Zahlungen](payments-retail.md)

[Auschecken-Modul](../add-checkout-module.md)

[Zahlungsmodul](../payment-module.md)
