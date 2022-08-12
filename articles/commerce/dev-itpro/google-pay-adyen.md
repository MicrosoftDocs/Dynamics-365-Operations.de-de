---
title: Google Pay mit Adyen konfigurieren
description: Dieser Artikel beschreibt, wie Sie Google Pay mit Adyen in Microsoft Dynamics 365 Commerce konfigurieren.
author: BrianShook
ms.date: 07/05/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: c3f049946c66fcd8560f7c08a4cb2beab0dcd5b2
ms.sourcegitcommit: 3d2c0a39c4f987e9ac71df2f2fa6df0f64f10b2b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/06/2022
ms.locfileid: "9115029"
---
# <a name="configure-google-pay-with-adyen"></a>Google Pay mit Adyen konfigurieren

[!include [banner](../includes/banner.md)]

Dieser Artikel beschreibt, wie Sie Google Pay mit Adyen in Microsoft Dynamics 365 Commerce konfigurieren.

Dynamics 365 Commerce bietet eine standardmäßige Integration für Google Pay, wenn der Adyen Payment Gateway Service verwendet wird. Google Pay ist eine digitale Brieftaschen-Zahlungsmethode, die ein Google Pay-Händlerkonto in Abstimmung mit dem Adyen-Zahlungsdienst verwendet. Wenn sie konfiguriert ist, ist die Schaltfläche Google Pay als auswählbare Zahlungsmethode während der Online-Kaufabwicklung verfügbar. Wenn Benutzer **Google Pay** in einem unterstützten Browser oder Gerät auswählen, werden sie angewiesen, ihre Zahlung direkt mit dem Google Pay-Dienst abzuschließen. Sie werden dann zum Online-Store zurückgeleitet, um die Bestellung abzuschließen.

Wenn Google Pay mit dem Express-Checkout-Modul in Commerce verwendet wird, werden die Zahlungskontoinformationen des Benutzers automatisch im Formular für den Checkout vorausgefüllt, damit der Benutzer den Checkout-Prozess schneller durchlaufen kann. Commerce enthält ein Express-Zahlungsmodul, das ein Express-Checkout-Verhalten ermöglicht. Das Express-Zahlungsmodul kann in einem Fragment verwendet werden, das auf der Seite der Kasse oder des Warenkorbs enthalten ist. Die Referenz des Dynamics 365 Payment Connector for Google Pay Konnektors wird zusätzlich zum Dynamics 365 Payment Connector for Adyen verwendet, um sowohl die Express- als auch die regulären Checkout-Optionen zu aktivieren, wenn PayPal konfiguriert ist. Google Pay kann auch mit Adyen Zahlungsterminals und dem Point of Sale (POS) von Commerce für die Verwendung in Geschäften konfiguriert werden.

## <a name="key-terms"></a>Schlüsselbegriffe

| Zeitdauer | Description |
|---|---|
| Google Pay | Google Pay, auch bekannt als die Google Pay „Schaltfläche“, ist ein Wallet-Zahlungsangebot, das über den Adyen-Konnektor unterstützt wird. Es ermöglicht das Debitor-Erlebnis und die Integration, die vom Dynamics Google Pay Connector unterstützt werden. |
| Brieftasche | Eine Zahlungsart, die keine traditionellen Zahlungsmerkmale enthält, wie z.B. den Bereich der Bankleitzahl (BLZ) und das Ablaufdatum, die zur Unterscheidung von Kredit- und Debitkarten verwendet werden. |
| Modul Zahlungsexpress | Ein Dynamics 365 Commerce-Modul, das ein schnelleres Checkout-Verhalten mit unterstützten Zahlungsformen unterstützt. |

## <a name="prerequisites"></a>Voraussetzungen

Die Verwendung von Google Pay mit Adyen in Commerce erfordert ein Google Merchant-Konto. Informationen darüber, wie Sie Ihr Google Merchant-Konto festlegen, finden Sie in der [Adyen-Dokumentation zu Google Pay](https://docs.adyen.com/payment-methods/google-pay/) und in der [Integrations-Checkliste](https://developers.google.com/pay/api/web/guides/test-and-deploy/integration-checklist) von Google.

Die Zahlungsmethode Google Pay muss auch in Ihr Adyen-Konto integriert werden. Anleitungen für den Integrationslink finden Sie unter [Adyen Google Pay](https://www.adyen.com/payment-methods/google-pay).

Außerdem müssen Sie die Funktion „Erweiterte Brieftasche“ in Dynamics 365 Commerce headquarters aktivieren. Gehen Sie zu **Arbeitsbereiche \> Funktionsverwaltung**, suchen Sie nach der Funktion **Erweiterte Brieftaschenunterstützung und Zahlungsverbesserungen**, wählen Sie die Funktion aus und wählen Sie dann **Aktivieren**. Nachdem die Funktion aktiviert wurde, führen Sie den **1110** Verteilungsplan aus, um die Änderung in allen Kanälen verfügbar zu machen.

## <a name="map-the-google-pay-payment-method"></a>Zuordnung der Zahlungsmethode Google Pay

Google Pay ist eine Zahlungsmethode für digitale Brieftaschen. Informationen darüber, wie Sie die Zuordnung von Zahlungen für Google Pay festlegen, finden Sie unter [Wallet-Zahlungsunterstützung](../wallets.md).

So ordnen Sie die Google Pay-Zahlungsmethode den Kartenausschreibungsarten sowohl für POS- als auch für Online-Kanäle zu.

1. In der Commerce headquarters gehen Sie zu **Einzelhandel und Commerce \> Einrichtung der Kanäle \> Zahlungsformen \> Kartentypen**.
1. Wählen Sie **Neu**, um eine Zeile für Google Pay hinzuzufügen.
1. Geben Sie in das Feld **ID** **GooglePay** ein.
1. Geben Sie in das Feld **Elektronische Zahlung** **Google Pay** ein.
1. Geben Sie in das Feld **Typ** **Wallet** ein.
1. In das Feld **Absender** geben Sie **Google** ein.
1. Wählen Sie im Aktionsbereich **Prozessorzuordnung**, um das Dialogfeld **Prozessor-Zahlungszuordnungsmethoden** zu öffnen.
1. Unter **Nicht zugeordnete Zahlungsformen für Prozessoren** sehen Sie eine Liste der nicht zugeordneten Zahlungsformen für Prozessoren, von denen jede mit dem entsprechenden Konnektor gepaart ist. Um nicht zugeordnete Google Pay-Prozessor-Zahlungsformen den Kartenausschreibungsarten zuzuordnen, führen Sie diese Schritte für jede Kartenausschreibungsart aus:

    1. Wählen Sie unter **Kartenbelegtypen** einen Kartenbelegtyp aus.
    1. Wählen Sie in der Spalte **Unmapped Processor Payment Methods** sowohl den **Dynamics 365 Payment Connector for Adyen** Konnektor (zur Verwendung am POS) als auch den **Dynamics 365 Payment Connector for Google Pay** Konnektor (zur Verwendung in Online-Kanälen).
    1. Wählen Sie **Hinzufügen** aus. Die Auswahlen werden in der Spalte **Zugeordnete Zahlungsformen** des Prozessors hinzugefügt.

1. Wenn Sie die Zuordnung der Zahlungsformen abgeschlossen haben, wählen Sie **Speichern**.
1. Auf der Seite **Kartentypen** wählen Sie **Speichern**.

## <a name="configure-a-commerce-online-store-for-google-pay"></a>Konfigurieren Sie einen Commerce Online Store für Google Pay

Um einen Commerce Store für die Verwendung von Google Pay zu konfigurieren, gehen Sie folgendermaßen vor.

1. In der Commerce headquarters gehen Sie zu **Einzelhandel und Commerce \> Kanäle \> Online Stores**.
1. Wählen Sie den Online Store-Kanal Ihrer Website, indem Sie den Wert **Retail Channel Id** des Kanals auswählen.
1. Bestätigen Sie auf der Registerkarte **Zahlungskonten** unter **Konnektor**, dass der **Dynamics 365 Payment Connector for Adyen** Konnektor aufgeführt ist. Wenn er nicht aufgeführt ist, folgen Sie den Anweisungen unter [Einrichten des Dynamics 365 Payment Connector for Adyen](adyen-connector-setup.md), um ihn hinzuzufügen.

    > [!NOTE]
    > In den meisten Fällen muss der **Dynamics 365 Payment Connector for Adyen** Konnektor als erster Konnektor für Ihren Kanal aufgeführt sein (der erste Konnektor wird auch als primärer Konnektor bezeichnet). Anschließend müssen andere Konnektoren verwendet werden, wie z.B. die Konnektoren **Dynamics 365 Payment Connector for PayPal** und **Dynamics 365 Payment Connector for GooglePay**.

1. Nachdem der **Dynamics 365 Payment Connector for Adyen** Konnektor hinzugefügt wurde, wählen Sie **Hinzufügen**, um den **Dynamics 365 Payment Connector for GooglePay** Konnektor hinzuzufügen. Legen Sie dann die folgenden Eigenschaften für den Konnektor fest.

    | Feld                  | Description | Erforderlich | Automatisch festgelegt auf | Beispielwert |
    | ---------------------- | ----------- | -------- | ----------------- | ------------ |
    | Assemblyname          | Der Name der Assembly für den Dynamics 365 Payment Connector for GooglePay. | Ja | Ja | *Binärname* |
    | Dienstkontokennung     | Die eindeutige Kennung für die Einrichtung der Händlereigenschaften. Diese Kennung wird auf Zahlungstransaktionen gestempelt und identifiziert die Eigenschaften des Händlers, die nachgelagerte Prozesse (z.B. die Rechnungsstellung) verwenden sollten. | Ja | Ja | *GUID* |
    | Google-Händler-ID     | Geben Sie die Google Merchant ID ein, die Ihrem Google Merchant Konto zugewiesen ist. Diese Eigenschaft ist für Produktionsumgebungen erforderlich, für Testumgebungen ist sie jedoch optional. Für weitere Informationen besuchen Sie <https://pay.google.com/>. | Ja | Nein | *Numerischer Bezeichner* |
    | Einzelhändlerkontokennung    | Geben Sie die eindeutige Adyen-Händler-Kennung ein. Dieser Wert wird angegeben, wenn Sie sich bei Adyen anmelden, wie unter [Anmelden bei Adyen](adyen-connector-setup.md#sign-up-with-adyen) beschrieben. | Ja | Nein | *Händler-Identifikator* |
    | Cloud-API-Schlüssel          | Geben Sie den Adyen Cloud API-Schlüssel ein. Um diesen Schlüssel zu erhalten, folgen Sie den Anweisungen unter [Wie Sie den API-Schlüssel erhalten](https://docs.adyen.com/developers/user-management/how-to-get-the-api-key). | Ja | Nein | „abcdefg“ |
    | Gatewayumgebung    | Die Adyen Gateway Umgebung, die zugeordnet werden soll. Die möglichen Werte sind **Test** und **Live**. Sie sollten dieses Feld nur für Produktionsgeräte und Transaktionen auf **Live** festlegen. | Ja | Ja | „Live“ |
    | Unterstützte Währungen   | Die Währungen, die der Konnektor verarbeiten soll. In Szenarien mit Kartenzahlung kann Adyen über [Dynamische Währungsumrechnung](https://www.adyen.com/pos-payments/dynamic-currency-conversion) zusätzliche Währungen unterstützen, nachdem die Transaktionsanforderung an das Zahlungsterminal gesendet wurde. Wenden Sie sich an den Adyen-Support, um eine Liste der unterstützten Währungen zu erhalten. | Ja | Ja | „USD;EUR“ |
    | Unterstützte Zahlungsmitteltypen | Die Ausschreibungsarten, die der Konnektor verarbeiten soll. | Ja | Ja | „GooglePay“ |

1. Nachdem Sie die Eigenschaften des Konnektors festgelegt haben, führen Sie den Auftrag **1070 (Kanalkonfiguration**) Verteilungsplan aus.

## <a name="configure-commerce-pos-for-google-pay"></a>Konfigurieren Sie Commerce POS für Google Pay

Die POS-Konfiguration verwendet die Einstellung des Feldes **EFT-Service** des Hardwareprofils für den Dynamics 365 Payment Connector for Adyen. Informationen darüber, wie Sie den EFT-Dienst (Electronic Funds Transfer) für den Payment Connector for Adyen in der Commerce headquarters konfigurieren, finden Sie im Abschnitt [Einrichten eines Dynamics 365 POS-Hardwareprofils](adyen-connector-setup.md#set-up-a-dynamics-365-pos-hardware-profile).

Die Prozessor-Zuordnung für den Adyen Konnektor erfasst die Wallet-Kartentypen, die Google Pay am POS Terminal verwendet.

### <a name="use-the-payment-express-module-with-google-pay"></a>Verwenden Sie das Zahlungsexpress-Modul mit Google Pay

Das Commerce-Zahlungsexpressmodul arbeitet mit unterstützenden Zahlungsmethoden, um den Debitor einer Website die Möglichkeit zu geben, schneller auszuchecken, indem er seine Kontodaten des Zahlungsdienstleisters während des Bezahlvorgangs verwendet. Das Expresszahlungsmodul verweist auf die konfigurierte Schaltfläche des Konnektors und gibt die vom Benutzer ausgewählten Bestelldaten (Adresse, Kontaktinformationen und Zahlungsmethode) zurück, um das Formular der Kaufabwicklung vorauszufüllen.

Wenn das Zahlungsexpress-Modul mit Google Pay verwendet wird, wird, wenn Debitor die Schaltfläche Google Pay im Abschnitt **Zahlungsexpress** auswählt, das iframe-Fenster von Google Pay geöffnet. Benutzer können sich dann bei ihrem Google-Konto anmelden und ihre Lieferadresse, Rechnungsadresse, E-Mail-Adresse und die Google Pay-Zahlungsmethode ihrer Wahl verwenden, um die Transaktion zu bezahlen.

Wenn Benutzer die Aktion im Google Pay-Fenster abschließen, werden sie auf die Commerce-Website zur Kasse geleitet, wo das Formular für die Kasse mit ihren Google Pay-Kontodaten vorausgefüllt wird. Nachdem die Benutzer vom Google Pay-Fenster auf die Kassenseite zurückgekehrt sind, sehen sie die folgenden Details:

- Im Payment Express Flow wird die erste Lieferoption, die für die zurückgegebene Lieferadresse verfügbar ist, für den Debitor vorausgewählt.
- Bei der Verwendung von Google Pay wird keine Kontakt-E-Mail-Adresse zurückgegeben. Benutzer, die als Gast zur Kasse gehen, müssen eine E-Mail-Adresse in den Abschnitt „Kontakt“ auf der Seite „Kasse“ eingeben. Bei angemeldeten Benutzern werden die Kontaktdaten automatisch aus ihrem Dynamics Debitorenkonto (die primäre E-Mail-Adresse, die sie zur Authentifizierung verwendet haben) ausgefüllt.

Debitor haben die Möglichkeit, Bestellungen zu überprüfen und Details der Kassenbestellung zu ändern, bevor sie **Bestellung aufgeben** wählen, um die Bestellung abzuschließen.

### <a name="configure-google-pay-in-site-builder"></a>Konfigurieren Sie Google Pay im Site Builder 

Bevor Sie Ihre Fragmente oder Seiten mit Google Pay konfigurieren, müssen Sie sicherstellen, dass die Sicherheitsrichtlinien für Ihre Website in Commerce Site Builder festgelegt sind.

Gehen Sie folgendermaßen vor, um sicherzustellen, dass Ihre Richtlinien für die Inhaltssicherheit in Site Builder festgelegt sind.

1. Gehen Sie in Ihrer Website auf **Site-Einstellungen \> Erweiterungen**.
1. Fügen Sie auf der Registerkarte **Sicherheitsrichtlinie für Inhalte** eine Zeile für `*.google.com` zu den Richtlinien **child-src**, **connect-src**, **frame-ancestors**, **frame-src**, **img-src**, **script-src** und **style-src** hinzu.
1. Wenn Sie fertig sind, wählen Sie **Speichern und veröffentlichen**.

### <a name="configure-the-payment-express-fragment-with-google-pay-in-site-builder"></a>Konfigurieren Sie das Zahlungsexpress-Fragment mit Google Pay im Site Builder

Um das Zahlungsexpress-Fragment mit Google Pay für den Online-Shop festzulegen, führen Sie diese Schritte aus.

1. Gehen Sie im Website-Builder zu **Fragmente**.
1. Wählen Sie **Neu** aus.
1. Wählen Sie im Dialogfeld **Neues Fragment** das Modul **Container**, geben Sie einen Fragmentnamen ein (z.B. **Express Checkout**) und wählen Sie dann **OK**. 
1. Wählen Sie die Zuteilung des neuen Fragments **Standard Container**.
1. Legen Sie im Eigenschaftsfenster rechts die Eigenschaften für das Container-Modul fest:

    - **Überschrift** – Geben Sie eine Überschrift ein, die für den Express-Kassenbereich Ihrer Website angezeigt werden soll (zum Beispiel **Express-Kasse**).
    - **Container Layout** – Wählen Sie **Flow**.
    - **Breite** – Wählen Sie **Container füllen** aus.
    - **Angezeigte untergeordnete Elemente** – Wählen Sie **Drei**, um die Anzahl der untergeordneten Elemente festzulegen, die in eine Zeile des Express-Checkout-Abschnitts der Checkout-Seite passen (z.B. ein Textfeld, Zahlungsexpress für PayPal und Zahlungsexpress für Google Pay).
    - **CSS Klassenname** – Geben Sie **msc-express-payment-container** ein (erforderlich).

    > [!IMPORTANT]
    > - Der Wert **CSS Klassenname** muss auf **msc-express-payment-container** festgelegt werden, um das Verhalten des Containers beim Checkout zu steuern. Dieses Verhalten umfasst das Ausblenden, Zusammenklappen und andere Aktionen, die für den Express-Checkout-Bereich während des Checkout Flows gelten. Die Klasse **msc-express-payment-container** arbeitet mit den Standardvorgängen, die mit der Modulbibliothek checkout module freigegeben werden.
    > - Zusätzliche Stile können über den **CSS Klassennamen** eingefügt werden. Wenn Sie das Verhalten des Moduls anpassen, überprüfen Sie die Steuerelemente des Stils, ob Sie das gleiche, in der Modulbibliothek kodierte Verhalten im Checkout-Modul für das Express-Checkout-Verhalten verwenden.

1. Wählen Sie im Slot **Standard-Container** die Ellipsen-Schaltfläche (**...**) und wählen Sie **Modul hinzufügen**.
1. Wählen Sie im Dialogfeld **Module auswählen** das Modul **Zahlungsexpress** und dann **OK** aus.
1. Legen Sie im Bereich Eigenschaften des Moduls **Payment express** den Wert **Höhe der iFrame** in Pixel fest oder passen Sie ihn an (zum Beispiel **60**).
1. Geben Sie in das Feld **Unterstützte Zahlungsarten** **GooglePay** ein. Der Wert muss mit der Zeichenfolge **Unterstützte Ausschreibungsarten** im Konnektor übereinstimmen, der für den Kanal festgelegt ist (wie im Abschnitt [Konfigurieren Sie einen Commerce Online Store für Google Pay](#configure-a-commerce-online-store-for-google-pay) weiter oben in diesem Artikel beschrieben).

    > [!NOTE]
    > Sie können die Schritte 6 bis 9 wiederholen, um **Zahlungsexpress**-Bausteine für andere Zahlungsformen hinzuzufügen. Richten Sie den Wert **Unterstützte Angebotsarten** an den zusätzlich konfigurierten Zahlungsarten aus (zum Beispiel **Paypal**).

1. Optional: Sie können dem Standard-Container-Modul einen Textblock hinzufügen, um Anweisungen oder Informationen zur Offenlegung aufzunehmen. Nachdem Sie das Modul hinzugefügt haben, geben Sie im Eigenschaftenbereich den gewünschten Text in das Feld **Rich-Text** ein. Sie können den Text über oder unter den Zahlungsexpress-Modulen positionieren, indem Sie die Auslassungspunkte (**...**) in der Zuteilung von Zeitfenstern (**Textblock**) auswählen und dann **Nach oben** oder **Nach unten** wählen.
1. Wählen Sie **Speichern**, um Ihre Änderungen zu speichern, und wählen Sie dann **Bearbeitung beenden**.
1. Wählen Sie **Veröffentlichen**, um das Fragment zu veröffentlichen.

### <a name="add-the-payment-express-fragment-to-the-checkout-page"></a>Das Zahlungsexpress-Fragment zur Auschecken-Seite hinzufügen

Führen Sie diese Schritte aus, um das Expresszahlungsfragment zur Kassenseite hinzuzufügen.

1. Gehen Sie im Site Builder zu **Seiten** und wählen Sie dann die Kassenseite Ihrer Website aus.
1. Wählen Sie **Bearbeiten** aus.
1. Markieren Sie im Feld **Zuteilung von Zeitfenstern** die Auslassungspunkte (**...**) und wählen Sie dann **Modul hinzufügen**.
1. Wählen Sie im Dialogfeld **Module auswählen** das Modul **Container** und dann **OK** aus.
1. Legen Sie im Eigenschaftsfenster rechts die Eigenschaften für das Container-Modul fest:

    - **Container-Layout** – Wählen Sie **Gestapelt** aus.
    - **Breite** – Wählen Sie **Container füllen** aus.
    - **Angezeigte untergeordnete Elemente** – Wählen Sie **Drei**, um die Anzahl der untergeordneten Elemente festzulegen, die in eine Zeile des Express-Checkout-Abschnitts der Checkout-Seite passen (z.B. ein Textfeld, Zahlungsexpress für PayPal und Zahlungsexpress für Google Pay).

1. Markieren Sie im Modulsteckplatz **Container** die Auslassungspunkte (**...**) und wählen Sie dann **Fragment hinzufügen**.
1. Wählen Sie im Dialogfeld **Wählen Sie ein Fragment** das Fragment Expresszahlung, das Sie erstellt haben, und wählen Sie dann **OK**.
1. Wählen Sie **Speichern**, um Ihre Änderungen zu speichern, und wählen Sie dann **Bearbeitung beenden**.
1. Wählen Sie **Veröffentlichen** aus, um die Seite zu veröffentlichen.

> [!NOTE]
> Wenn die Checkout-Seite bereits einen Container mit dem Checkout-Fragment enthält und Sie möchten, dass das Express-Zahlungsmodul über dem normalen Checkout-Container angezeigt wird, können Sie es über oder unter dem bestehenden Checkout positionieren, indem Sie die Auslassungspunkte (**...**) im **Hauptfenster** auswählen und dann **Nach oben** oder **Nach unten** wählen.

### <a name="add-the-payment-express-fragment-to-the-cart-page"></a>Das Zahlungsexpress-Fragment zur Warenkorb-Seite hinzufügen

Führen Sie diese Schritte aus, um das Expresszahlungsfragment zur Warenkorb-Seite hinzuzufügen.

1. Gehen Sie im Site Builder zu **Seiten** und wählen Sie dann die Einkaufswagenseite Ihrer Website aus.
2. Wählen Sie **Bearbeiten** aus.
3. Erweitern Sie in der Gliederungsansicht den **Hauptsteckplatz** in der Baum-Ansicht und suchen Sie den Container, der das Modul **Karte** enthält.
4. Wählen Sie im Modul **Warenkorb** den Steckplatz **Payment Express**, markieren Sie die Auslassungspunkte (**...**) und wählen Sie dann **Modul hinzufügen**.
5. Wählen Sie im Dialogfeld **Module auswählen** das Modul **Zahlungsexpress** und dann **OK** aus.
6. Wählen Sie die Zuteilung des Moduls **Zahlungsexpress**. Geben Sie dann im Eigenschaftenbereich rechts unter **Unterstützte Zahlungsarten** **GooglePay** ein. Der Wert muss mit der Zeichenfolge **Unterstützte Ausschreibungsarten** im Konnektor übereinstimmen, der für den Channel festgelegt wurde (wie im Abschnitt [Konfigurieren Sie einen Commerce Online Store für Google Pay](#configure-a-commerce-online-store-for-google-pay) weiter oben in diesem Artikel beschrieben).
1. Wählen Sie **Speichern**, um Ihre Änderungen zu speichern, und wählen Sie dann **Bearbeitung beenden**.
1. Wählen Sie **Veröffentlichen** aus, um die Seite zu veröffentlichen.

Benutzer können bis zu drei unterstützte **Payment Express**-Module (d.h. drei verfügbare unterstützte Zahlungsoptionen) in die Zuteilung von **Payment Express** im Warenkorb aufnehmen.

### <a name="set-up-google-pay-as-an-option-in-the-checkout-payment-section"></a>Legen Sie Google Pay als Option im Abschnitt für die Bezahlung an der Kasse fest.

Sie können Google Pay als Option im Abschnitt für die Bezahlung an der Kasse festlegen, um eine reine Bezahlfunktion ohne Expressfunktion zu erhalten. Das Formular für die Kaufabwicklung wird vom Benutzer ausgefüllt, und die Zahlungsseite für Google Pay bereitet die Kaufabwicklung nur für die Zahlung mit Google Pay vor. Es werden keine Google-Kontoinformationen verwendet, um die ausgefüllten Checkout-Details zu überschreiben.

> [!NOTE]
> Das folgende Verfahren geht davon aus, dass Ihre Website ein Checkout-Fragment verwendet, das mit Abholinformationen, einer Lieferadresse, Lieferoptionen, Kontaktinformationen, optionalen Bestimmungen und einem Abschnitt für Checkout-Elemente konfiguriert ist. Die Standardmodulbibliothek Kassenmodul wird mit einem Container für den Kassenbereich freigegeben, der Textblöcke, Treuepunkte, Geschenkkarten und Zahlungsmodule enthält. Weitere Informationen finden Sie unter [Zahlungsmodul](../payment-module.md).

Um Google Pay als reguläre Zahlungsoption im Abschnitt **Zahlungsmethode** der Kassenseite festzulegen, folgen Sie diesen Schritten.

1. Gehen Sie im Site Builder zu **Fragmente** und wählen Sie dann das Kassenfragment Ihrer Website aus.
1. Wählen Sie **Bearbeiten** aus.
1. Markieren Sie im Bereich **Kasseninformationen** die Auslassungspunkte (**...**) und wählen Sie dann **Modul hinzufügen**.
1. Wählen Sie im Dialogfeld **Module auswählen** das Modul **Zahlung** und wählen Sie dann **OK**.
1. Legen Sie im Eigenschaftsfenster des Moduls **Payment** auf der rechten Seite die Eigenschaften für das Container-Modul fest:

    - **Überschrift** – Geben Sie eine Überschrift ein, die für den Express-Kassenbereich Ihrer Website angezeigt werden soll (z.B. **Google Pay**).
    - **Höhe der iFrame** – Ändern Sie den Wert in Ihre bevorzugte Designhöhe in Pixeln (zum Beispiel **75**). 
    - **Unterstützte Angebotsarten** – Geben Sie **GooglePay** ein, um die Konfiguration für den Google Pay Konnektor in der Commerce headquarters zu übernehmen.
    - **Ist primäre Zahlung** – Lassen Sie das Kontrollkästchen deaktiviert. (Diese Eigenschaft ist in der Regel für das Adyen Checkout-Modul aktiviert.)
    - **Zahlungsstil außer Kraft setzen** – Diese Eigenschaft wird für die Google Pay-Konfiguration nicht unterstützt.
    - **Konnektor-ID verwenden** – Diese Eigenschaft muss ausgewählt werden, wenn mehrere Zahlungskonnektoren auf der Seite verwendet werden.

1. Positionieren Sie das Modul über oder unter anderen Zahlungsmodulen, indem Sie die Auslassungspunkte (**...**) in der Zuteilung von Zeitfenstern **Zahlung** auswählen und dann **Nach oben** oder **Nach unten** wählen.
1. Wählen Sie **Speichern**, um Ihre Änderungen zu speichern, und wählen Sie dann **Bearbeitung beenden**.
1. Wählen Sie **Veröffentlichen** aus.

### <a name="modes-of-delivery"></a>Lieferarten

Mit dem Zahlungsexpress-Modul, das Google Pay verwendet, wird die erste Lieferoption, die gegen die ausgewählte Lieferadresse aus dem Google Pay-Konto zurückgegeben wird, vorausgewählt. Benutzer haben die Möglichkeit, die Lieferadresse auf eine andere Option einzustellen, wenn sie dies wünschen.

Die Reihenfolge, in der die Liefermethoden im Payment Express-Modul angezeigt werden, wird auf der Seite **Lieferarten** des Channels in der Commerce headquarters konfiguriert. Gehen Sie in der Commerce headquarters zu **Einzelhandel und Commerce \> Kanäle \> Online-Shops**, und wählen Sie den Wert **Einzelhandelskanal-ID** für Ihr Store. Wählen Sie im Aktionsbereich auf der Registerkarte **Einrichtung** die Option **Liefermodi**. Die aufgeführten Lieferarten werden in der gleichen Reihenfolge im Zahlungsexpressmodul angezeigt. Wählen Sie **Lieferarten verwalten** im Aktionsbereich, um Lieferarten für einen Vertriebskanal oder ein Produkt hinzuzufügen oder zu entfernen. Weitere Informationen darüber, wie Sie Bereitstellungsmodi festlegen, finden Sie unter [Bereitstellungsmodi festlegen](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).

Das Checkout-Modul verwendet auch das Modul für die Lieferoptionen, wenn die Lieferarten während des Checkouts angezeigt werden. Weitere Informationen finden Sie unter [Lieferoptionenmodul](../delivery-options-module.md).

Die Lieferarten werden angezeigt, sobald sie der Liste **Lieferarten** im Online Store hinzugefügt werden.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[FAQs zu Zahlungen](payments-retail.md)

[Auschecken-Modul](../add-checkout-module.md)

[Zahlungsmodul](../payment-module.md)
