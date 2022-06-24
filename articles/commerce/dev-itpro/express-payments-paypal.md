---
title: Expresszahlungen für PayPal konfigurieren
description: In diesem Artikel wird beschrieben, wie Expresszahlungen für PayPal konfiguriert werden, um schnellere Auschecken-Funktionen in Microsoft Dynamics 365 Commerce zu ermöglichen.
author: BrianShook
ms.date: 05/11/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: b69b7384992fb86370ff6881824a7d2c9a77d2c4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8905281"
---
# <a name="configure-express-payments-for-paypal"></a>Expresszahlungen für PayPal konfigurieren

[!include [banner](../includes/banner.md)]

In diesem Artikel wird beschrieben, wie Expresszahlungen für PayPal konfiguriert werden, um schnellere Auschecken-Funktionen in Microsoft Dynamics 365 Commerce zu ermöglichen.

## <a name="key-terms"></a>Schlüsselbegriffe

| Zeitdauer | Description |
|---|---|
| PayPal Wallet | Das Kundenerlebnis und die Integration, die vom PayPal-Connector unterstützt werden. Sie wird auch als PayPal-Schaltfläche bezeichnet. |
| Brieftasche | Eine Zahlungsart, die keine herkömmlichen Zahlungsmerkmale wie den Bereich der Bankidentifikationsnummer (BIN) und das Ablaufdatum enthält, die zur Unterscheidung von Kredit- und Debitkartentypen verwendet werden. |
| Zahlungsexpress | Ein Commerce-Modul, das ein schnelleres Verhalten beim Auschecken unterstützt, wenn unterstützte Zahlungsmethoden verwendet werden. Dieser Artikel behandelt die Verwendung des Zahlungsexpress-Moduls mit PayPal. |

Dynamics 365 Commerce bietet eine sofort einsatzbereite Integration für PayPal Wallet. Wenn der Dynamics 365 Payment Connector für PayPal konfiguriert ist, wird die PayPal-Schaltfläche als auswählbare Zahlungsmethode während der Online-Bestellungsabwicklung angezeigt. Wenn Benutzer PayPal auswählen, werden sie angewiesen, ihre Zahlung direkt über PayPal abzuschließen, und werden dann zum Onlineshop zurückgeleitet, um ihre Bestellung abzuschließen. Mit dem PayPal-Warenkorb-Auscheckvorgang können Kunden ihre Zahlungskontoinformationen verwenden, um das Bezahlformular vorab auszufüllen, damit sie den Bezahlvorgang schneller abschließen können.

Commerce hat ein Zahlungsexpress-Modul hinzugefügt, um Express-Auscheckvorgänge zu erleichtern. Das Zahlungsexpress-Modul kann in einem Fragment verwendet werden, das auf einer Auschecken- oder Warenkorbseite enthalten sein kann. Wenn PayPal konfiguriert ist, wird die gleiche Connector-Referenz von Dynamics 365 Payment Connector für PayPal sowohl für die Zahlungsexpress-Option als auch für die reguläre Auschecken-Option verwendet.

## <a name="paypal-checkout-in-commerce"></a>PayPal-Auscheckvorgang in Commerce

### <a name="prerequisites"></a>Voraussetzungen

Richten Sie PayPal Wallet für Ihre Umgebung wie in [Dynamics 365 Payment Connector für PayPal](../paypal.md) beschrieben ein.

Wenn Sie PayPal als Option im regulären Bezahlvorgang verwenden (bei dem Benutzer ihre Kontoinformationen manuell eingeben, ohne die Express-Vorausfüllaktionen für Zahlungen zu verwenden), befolgen Sie die Einrichtungsanweisungen in [Zahlungsmodul](../payment-module.md).

### <a name="payment-express-module-with-paypal"></a>Zahlungsexpress-Modul mit PayPal

Das Zahlungsexpress-Modul arbeitet mit unterstützenden Zahlungsmethoden, um Site-Kunden die Möglichkeit zu bieten, schneller auszuchecken, indem sie ihre Zahlungsdienstkontoinformationen während des Auschecken-Prozesses vorab ausfüllen. Das Zahlungsexpress-Modul verwendet den konfigurierten Zahlungsconnector, um das Auschecken-Formular mit Benutzerkontodaten wie Adresse, Kontaktinformationen und ausgewählter Zahlungsmethode vorab auszufüllen.

Wenn PayPal-Express-Checkout verwendet wird und ein Benutzer die PayPal-Schaltfläche im Zahlungsexpress-Bereich der Auschecken-Seite auswählt, wird ein iFrame-Fenster für die PayPal-Zahlung geöffnet. Der Benutzer meldet sich dann bei seinem PayPal-Konto an, um die Lieferadresse, Rechnungsadresse, E-Mail-Adresse und die gewünschte PayPal-Zahlungsmethode zur Bezahlung der Transaktion zu verwenden.

Nachdem der Benutzer die Aktion im PayPal-Fenster abgeschlossen hat, wird er zurück zur Auschecken-Seite der Commerce-Site geleitet, wo das Auschecken-Formular mit seinen ausgewählten Details vorausgefüllt ist. Im Zahlungsexpress-Flow wird die erste Lieferoption, die für die zurückgegebene Lieferadresse verfügbar ist, für den Benutzer vorausgefüllt. Der Benutzer hat dann die Möglichkeit, die Bestellung zu überprüfen und Bestelldetails zu ändern, bevor er **Bestellung aufgeben** auswählt, um die Bestellung abzuschließen.

### <a name="add-the-payment-express-module-with-paypal-to-a-fragment"></a>Das Zahlungsexpress-Modul mit PayPal zu einem Fragment hinzufügen

Gehen Sie folgendermaßen vor, um das Zahlungsexpress-Modul mit PayPal einem Fragment im Commerce Site Builder hinzuzufügen.

1. Navigieren Sie zu Ihrer Site.
1. Im linken Navigationsbereich wählen Sie **Fragmente** und dann **Neu** aus.
1. Finden und wählen Sie im Dialogfeld **Neues Fragment** das Modul **Zahlungsexpress**, und geben Sie dann unter **Fragmentname** einen Namen für das Fragment ein (z. B. **Express-Auschecken**).
1. Wählen Sie **OK**, um das Fragment zu erstellen.
1. Wählen Sie in der Gliederungsansicht den Slot des von Ihnen erstellten Zahlungsexpress-Moduls aus.
1. Wählen Sie im Eigenschaftenbereich **Überschrift** aus.
1. Geben Sie im **Überschrift**-Dialogfeld im Feld **Überschriftentext** den Überschriftentext ein, den Sie für den Abschnitt zum Expressauschecken Ihrer Site anzeigen möchten (z. B. **Express-Kasse**).
1. Unter **Überschriftenebene** wählen Sie die Überschriftenebene aus (z. B. **H2**).
1. Wählen Sie **OK** aus.
1. Im Eigenschaftenbereich im Feld **Höhe des iFrame** geben Sie die Höhe des iFrame-Elements ein oder passen sie an (zum Beispiel **60**).
1. Im Feld **Unterstützte Zahlungsmitteltypen** geben Sie **PayPal** ein.
1. Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um das Fragment einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.

### <a name="add-the-payment-express-fragment-to-the-checkout-page"></a>Das Zahlungsexpress-Fragment zur Auschecken-Seite hinzufügen

Führen Sie die folgenden Schritte aus, um ein Zahlungsexpress-Fragment zur Auschecken-Seite im Site Builder hinzuzufügen.

1. Navigieren Sie zu Ihrer Site.
1. Wählen Sie im linken Navigationsbereich **Seiten** und dann die Auschecken-Seite Ihrer Site aus.
1. Um die Seite zu bearbeiten, wählen Sie **Bearbeiten**.
1. Wählen Sie im **Haupt**-Slot die Ellipsen-Schaltfläche (**...**) und wählen Sie **Modul hinzufügen**.
1. Wählen Sie im Dialogfeld **Module auswählen** das Modul **Container** und dann **OK** aus.

    > [!NOTE]
    > Wenn bereits ein Containermodul vorhanden ist, das ein Auschecken-Fragment enthält, verschieben Sie den Zahlungsexpress-Abschnitt so, dass er über dem vorhandenen Auschecken-Container im **Haupt**-Slot angezeigt wird. Der Zahlungsexpress-Bereich wird dann über dem normalen Auschecken-Container gerendert. Um ein Container-Modul nach oben oder unten zu verschieben, wählen Sie die Ellipsen-Schaltfläche (**...**) und dann **Nach oben verschieben** oder **Nach unten verschieben** aus.

1. In dem **Container**-Eigenschaftsbereich empfehlen wir Ihnen, die Eigenschaftseinstellungen wie folgt zu konfigurieren:

    - **Container-Layout** – Wählen Sie **Gestapelt** aus.
    - **Breite** – Wählen Sie **Container füllen** aus.
    - **Angezeigte untergeordnete Elemente** – Wählen Sie **Drei** aus.

1. Wählen Sie im Slot **Container** die Ellipsen-Schaltfläche (**...**) und dann **Fragment hinzufügen** aus.
1. Finden und wählen Sie im Dialogfeld **Ein Fragment auswählen** das Expresszahlung-Fragment aus, das Sie zuvor erstellt haben, und wählen Sie dann **OK** aus.
1. Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um die Seite einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.

### <a name="add-the-payment-express-fragment-to-the-cart-page"></a>Das Zahlungsexpress-Fragment zur Warenkorb-Seite hinzufügen

Führen Sie die folgenden Schritte aus, um ein Zahlungsexpress-Fragment zur Warenkorb-Seite im Site Builder hinzuzufügen.

1. Navigieren Sie zu Ihrer Site.
1. Wählen Sie im linken Navigationsbereich **Seiten** und dann die Warenkorb-Seite Ihrer Site aus.
1. Um die Seite zu bearbeiten, wählen Sie **Bearbeiten**.
1. Im **Haupt**-Slot finden Sie den Container, der das **Warenkorb**-Modul enthält. Das **Warenkorb**-Modul enthält einen **Zahlungsexpress**-Slot.
1. Wählen Sie den **Zahlungsexpress**-Slot aus, wählen Sie die Ellipsen (**...**) und dann **Modul hinzufügen** aus.
1. Wählen Sie im Dialogfeld **Module auswählen** das Modul **Zahlungsexpress** und dann **OK** aus.
1. Im Eigenschaftenbereich im Feld **Unterstützte Zahlungsmitteltypen** geben Sie **Paypal** ein.
1. Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um die Seite einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.

### <a name="modes-of-delivery"></a>Lieferarten

Wenn das Zahlungsexpress-Modul für die Verwendung von PayPal konfiguriert ist, wird die erste Lieferoption, die für die Lieferadresse zurückgegeben wird, die für das PayPal-Konto ausgewählt wurde, vorausgefüllt. Benutzer können die Lieferadresse ändern, wenn sie möchten.

Die Reihenfolge der Lieferart wird im **Lieferarten**-Abschnitt für den Kanal in Commerce headquarters konfiguriert. Weitere Informationen finden Sie unter [Lieferarten einrichten](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).

Das Auschecken-Modul verwendet auch das Lieferoptionsmodul, wenn Lieferarten während des Auscheckens gerendert werden. Weitere Informationen finden Sie unter [Lieferoptionenmodul](../delivery-options-module.md).

Lieferarten werden der Liste für den Onlineshop in Commerce headquarters hinzugefügt. Gehen Sie zu **Einzelhandel und Handel \> Kanäle \> Onlineshops**, und wählen Sie die Kanalkennung für Ihren Shop aus. Wählen Sie dann **Einrichtung \> Lieferarten** aus. Die in der Konfiguration angezeigten Lieferarten der Module erscheinen in ähnlicher Weise auf der Site. Um Lieferarten für einen Einzelhandelskanal oder ein Produkt hinzuzufügen oder zu entfernen, wählen Sie **Lieferarten verwalten** im Aktivitätsbereich aus.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[FAQs zu Zahlungen](payments-retail.md)

[Auschecken-Modul](../add-checkout-module.md)

[Zahlungsmodul](../payment-module.md)

[Lieferarten einrichten](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)

[Lieferoptionenmodul](../delivery-options-module.md)
