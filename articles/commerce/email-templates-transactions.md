---
title: Mail-Vorlagen für Transaktionsereignisse erstellen
description: In diesem Thema wird beschrieben, wie Sie E-Mail-Vorlagen für Transaktionsereignisse in Microsoft Dynamics 365 Commerce erstellen, hochladen und konfigurieren.
author: bicyclingfool
ms.date: 12/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 25d7fcb803645f50ee4f5c608f5b6e789dfe3c31
ms.sourcegitcommit: eef5d9935ccd1e20e69a1d5b773956aeba4a46bc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/11/2021
ms.locfileid: "7913751"
---
# <a name="create-email-templates-for-transactional-events"></a>Mail-Vorlagen für Transaktionsereignisse erstellen

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

In diesem Thema wird beschrieben, wie Sie E-Mail-Vorlagen für Transaktionsereignisse in Microsoft Dynamics 365 Commerce erstellen, hochladen und konfigurieren.

Dynamics 365 Commerce bietet eine sofort einsatzbereite Lösung zum Versenden von E-Mails, die Kunden über Transaktionsereignisse informiert. Beispielsweise können E-Mails versendet werden, wenn eine Bestellung aufgegeben wurde, zur Abholung bereitsteht oder versandt wurde. In diesem Thema werden die Schritte zum Erstellen, Hochladen und Konfigurieren der E-Mail-Vorlagen beschrieben, die zum Senden von Transaktions-E-Mails verwendet werden.

## <a name="notification-types"></a>Benachrichtungstypen

Benachrichtigungen können konfiguriert werden, um Kunden per E-Mail zu informieren, wenn bestimmte Ereignisse im Rahmen des Bestell- und Kundenlebenszyklus auftreten. Um Benachrichtigungen zu konfigurieren, müssen Sie eine E-Mail-Vorlage einem Benachrichtigungstyp zuordnen, indem Sie ein Commerce-E-Mail-Benachrichtigungsprofil erstellen. Informationen zum Einrichten von E-Mail-Benachrichtigungsprofilen finden Sie unter [Richten Sie ein E-Mail-Benachrichtigungsprofil ein](email-notification-profiles.md).

Dynamics 365 Commerce unterstützt die folgenden Benachrichtigungstypen:

### <a name="order-created"></a>Auftrag erstellt

Der Benachrichtigungstyp *Bestellung erstellt* wird ausgelöst, wenn ein neuer Kundenauftrag in der Commerce-Zentrale erstellt wird.

> [!NOTE]
> Die Benachrichtigungsart Bestellung erstellt wird nicht für Cash-and-Carry-Transaktionen ausgelöst, die an einem Verkaufstellenterminal (POS) erfolgen. In diesem Fall wird stattdessen ein per E-Mail gesendeter und/oder gedruckter Beleg erstellt. Weitere Informationen finden Sie unter [Senden Sie E-Mail-Belege von Modern POS (MPOS)](email-receipts.md).

### <a name="order-confirmed"></a>Auftrag bestätigt

Der Benachrichtigungstyp *Bestellung bestätigt* wird ausgelöst, wenn ein Auftragsbestätigungsbeleg für einen Kundenauftrag von der Commerce-Zentrale generiert wird.

### <a name="picking-completed"></a>Entnahme abgeschlossen

Der Benachrichtigungstyp *Kommissionierung abgeschlossen* wird ausgelöst, wenn eine Kommissionierliste für einen Auftrag in der Commerce-Zentrale als erledigt markiert wird.

> [!NOTE]
> Der Benachrichtigungstyp Kommissionierung abgeschlossen wird nicht ausgelöst, wenn ein Artikel an einem POS-Terminal als kommissioniert markiert wird.

### <a name="packing-completed"></a>Verpackung abgeschlossen

Der Benachrichtigungstyp *Verpacken abgeschlossen* wird ausgelöst, wenn eine Lieferscheindokument für einen Auftrag in der Commerce-Zentrale an einem POS-Terminal generiert wird.

Der Benachrichtigungstyp Verpackung abgeschlossen unterstützt die folgenden zusätzlichen E-Mail-Platzhalter, um die Funktion Bestellung bereit zur Abholung und die Nachschlagefunktion für Bestellungen aus Transaktions-E-Mails zu erleichtern.

| Platzhaltername    | Kostenträger |
| ------------------- | ------- |
| `pickupstorename`     | Der Name des Geschäfts, in dem die Bestellung zur Abholung bereitsteht. |
| `pickupstoreaddress`  | Der Adresse des Geschäfts, in dem die Bestellung zur Abholung bereitsteht. |
| `pickupstorehourfrom` | Die Öffnungszeiten des Abholgeschäfts. |
| `pickupstorehourto`   | Die Schließzeiten des Abholgeschäfts. |
| `pickupchannelid`     | Die Geschäftskanal-ID des Abholgeschäfts. |
| `packingslipid`      | Die ID des Lieferscheins für die Bestellung, die abgeholt wird. |
| `confirmationid`      | Die Bestellbestätigungs-ID des Lieferscheins für die Bestellung, die abgeholt wird. (Diese ID wird manchmal als Kanalreferenz-ID bezeichnet.) |

Weitere Informationen zu den Funktionen zum Kunden-Check-in und zur Bestellungssuche finden Sie unter [Geo-Erkennung und -Umleitung einrichten](geo-detection-redirection.md) und unter [Bestellsuche für Gast-Check-Outs aktivieren](order-lookup-guest.md).

### <a name="order-ready-for-pickup"></a>Auftrag bereit für Abholung

Der Benachrichtigungstyp *Bestellung abholbereit* wird ausgelöst, wenn eine Bestellung als verpackt markiert ist und die Versandart auf einer oder mehreren Auftragszeilen auf **Kundenabholung** eingestellt ist.

> [!NOTE]
> Der Benachrichtigungstyp Bestellung bereit für Abholung wurde zugunsten des Benachrichtigungstyps Verpackung abgeschlossen abgeschafft. Dieser Benachrichtigungstyp wird durch die Zustellungsart angepasst.

### <a name="order-shipped"></a>Auftrag versendet

Der Benachrichtigungstyp *Bestellung versandt* wird ausgelöst, wenn eine Bestellung mit einer Lieferart außerhalb der Filiale fakturiert wird.

> [!NOTE]
> Der Benachrichtigungstyp Bestellung versandt wurde zugunsten des Benachrichtigungstyps Bestellung fakturiert abgeschafft. Dieser Benachrichtigungstyp wird durch die Zustellungsart angepasst.

### <a name="order-invoiced"></a>Auftrag fakturiert

Der Benachrichtigungstyp *Bestellung fakturiert* wird ausgelöst, wenn eine Bestellung in POS oder in der Commerce-Zentrale fakturiert wird.

### <a name="issue-gift-card"></a>Geschenkkarte ausstellen

Der Benachrichtigungstyp *Geschenkgutschein ausstellen* wird ausgelöst, wenn ein Kundenauftrag fakturiert wird, der ein Produkt vom Typ Geschenkkarte enthält.

> [!NOTE]
> Die Benachrichtigungs-E-Mail für die Ausstellung der Geschenkkarte wird an den Geschenkkartenempfänger gesendet. Der Empfänger des Geschenkgutscheins wird in der Commerce-Zentrale in einer einzelnen Auftragszeile auf der **Verpackung**-Registerkarte unter **Zeilendetails** angegeben. Er kann entweder manuell oder programmgesteuert angegeben werden.

Der Benachrichtigungstyp Geschenkgutschein ausstellen unterstützt die folgenden zusätzlichen Platzhalter.

| Platzhaltername      | Kostenträger |
| --------------------- | ------- |
| `giftcardnumber`        | Die Geschenkkartennummer für Produkte vom Typ Geschenkkarte. |
| `giftcardbalance`       | Der Geschenkkartensaldo für Produkte vom Typ Geschenkkarte. |
| `giftcardmessage`       | Die Geschenkkartennachricht für Produkte vom Typ Geschenkkarte. |
| `giftcardpin`         | Die Geheimzahl (PIN) der Geschenkkarte für Produkte vom Typ Geschenkkarte. (Dieser Platzhalter gilt nur für externe Geschenkkarten.) |
| `giftcardexpiration`    | Das Ablaufdatum der Geschenkkarte für Produkte vom Typ Geschenkkarte. (Dieser Platzhalter gilt nur für externe Geschenkkarten.) |
| `giftcardrecipientname` | Der Name des Geschenkkartenempfängers für Produkte vom Typ Geschenkkarte. |
| `giftcardbuyername`     | Der Name des Geschenkkartenkäufers für Produkte vom Typ Geschenkkarte. |

Weitere Informationen zu Geschenkkarten finden Sie unter [Digitale E-Commerce-Geschenkkarten](digital-gift-cards.md) und [Unterstützung für externe Geschenkkarten](dev-itpro/gift-card.md).

### <a name="order-cancellation"></a>Auftragsstornierung

Der Benachrichtigungstyp *Bestellungsstornierung* wird ausgelöst, wenn eine Bestellung in der Commerce-Zentrale storniert wird.

### <a name="customer-created"></a>Ein Debitor wurde erstellt.

Der Benachrichtigungstyp *Kunde erstellt* wird ausgelöst, wenn eine neue Kundenentität in der Commerce-Zentrale erstellt wird.

### <a name="b2b-prospect-approved"></a>B2B-Interessent genehmigt

Der Benachrichtigungstyp *B2B-Interessent genehmigt* wird ausgelöst, wenn die Onboarding-Anfrage eines Interessenten in der Commerce-Zentrale genehmigt wird. Weitere Informationen zum Genehmigen oder Ablehnen von B2B-Interessenten finden Sie unter [Richten Sie den Administratorbenutzer für einen neuen Geschäftspartner ein](b2b/manage-b2b-users.md#set-up-the-administrator-user-for-a-new-business-partner). 

Der Benachrichtigungstyp B2B-Interessent genehmigt unterstützt die folgenden zusätzlichen Platzhalter.

| Platzhaltername | Kostenträger                                                      |
| ---------------- | ------------------------------------------------------------ |
| `firstname`       | Der Vorname des B2B-Interessenten, wie er in der Bewerbung eingetragen ist. |
| `lastname`         | Der Nachname des B2B-Interessenten, wie er in der Bewerbung eingetragen ist. |
| `company`          | Der Name des Unternehmens des Bewerbers, wie er in der Bewerbung eingetragen ist. |
| `email`            | Die E-Mail-Adresse des Interessenten, wie sie in der Bewerbung eingetragen ist.   |
| `zipcode`          | Die Postleitzahl der Hauptadresse des Interessenten. |
| `comments`         | Der Kommentar, den der Interessent in die Bewerbung eingegeben hat. |
| `storename`        | Der Name des Kanals, in dem der Interessent erstellt wurde. |
| `storeurl`         | Standardmäßig leer. Um diesen Platzhalter zu verwenden, muss eine benutzerdefinierte Erweiterung erstellt werden. |

### <a name="b2b-prospect-rejected"></a>B2B-Interessent abgelehnt

Der Benachrichtigungstyp *B2B-Interessent abgelehnt* wird ausgelöst, wenn die Onboarding-Anfrage eines Interessenten in der Commerce-Zentrale abgelehnt wird. Weitere Informationen zum Genehmigen oder Ablehnen von B2B-Interessenten finden Sie unter [Richten Sie den Administratorbenutzer für einen neuen Geschäftspartner ein](b2b/manage-b2b-users.md#set-up-the-administrator-user-for-a-new-business-partner). 

Der Benachrichtigungstyp B2B-Interessent abgelehnt unterstützt die folgenden zusätzlichen Platzhalter.

| Platzhaltername | Kostenträger                                                      |
| ---------------- | ------------------------------------------------------------ |
| `firstname`        | Der Vorname des B2B-Interessenten, wie er in der Bewerbung eingetragen ist. |
| `lastname`         | Der Nachname des B2B-Interessenten, wie er in der Bewerbung eingetragen ist. |
| `company`          | Der Name des Unternehmens des Bewerbers, wie er in der Bewerbung eingetragen ist. |

## <a name="create-an-email-template"></a>E-Mail-Vorlage erstellen

Bevor Sie ein bestimmtes Transaktionsereignis einer E-Mail-Vorlage zuordnen können, müssen Sie die Vorlage erstellen.

Führen Sie folgende Schritte aus, um eine E-Mail-Vorlage zu erstellen:

1. Gehen Sie in der Commerce-Zentrale zu **Retail und Commerce \> Zentralverwaltungseinrichtung \> Organisations-E-Mail-Vorlagen** oder **Organisationsverwaltung \> Einrichten \> Organisations-E-Mail-Vorlagen**.
1. Wählen Sie **Neu** aus.
1. Unter **Allgemeines** setzen Sie die folgenden Felder:

    - **E-Mail-ID** – Die E-Mail-ID ist die eindeutige Kennung für eine Vorlage. Dies ist der Wert, der angezeigt wird, wenn Sie eine Vorlage auswählen, die einem Ereignis zugeordnet werden soll.
    - **E-Mail-Beschreibung** – In diesem optionalen Feld können Sie eine Beschreibung der Vorlage bereitstellen. Der von Ihnen eingegebene Wert wird nur in der Commerce-Zentrale angezeigt.
    - **Absendername** – Der von Ihnen eingegebene Name wird bei den meisten E-Mail-Clients im Feld „Von“ angezeigt.
    - **Absender-E-Mail** – Geben Sie die E-Mail-Adresse ein, die für E-Mails verwendet werden soll, die mithilfe dieser Vorlage gesendet werden.
    - **Standard-Sprachcode** – Dieses Feld gibt die lokalisierte Version der E-Mail an, die standardmäßig gesendet wird, wenn der Kanal, der diese Vorlage aufruft, keine Sprache angibt.

1. Wählen Sie unter **Inhalt der E-Mail-Nachricht** die Option **Neu** aus.
1. Im Feld **Sprache** geben die Sprache für die E-Mail-Vorlage ein. Sie können später weitere Sprachen und lokalisierte Vorlagen hinzufügen.
1. Im Feld **Betreff** geben Sie den Betreff der E-Mail ein, der in der E-Mail angezeigt werden soll.
1. Wählen Sie **Bearbeiten** aus, um Ihre E-Mail-Vorlage hochzuladen.

## <a name="create-an-email-message-body-by-using-html"></a>Erstellen Sie einen E-Mail-Nachrichtentext mithilfe von HTML

Der Nachrichtentext Ihrer E-Mail besteht aus HTML. Sie können jedes für HTML- und Inline-Cascading Style Sheets verwenden (CSS) zulässige Layout, Stilelement und Branding. Sie können Bilder auch verwenden, wenn Sie sie auf einem öffentlich verfügbaren Webendpunkt hosten. Um ein Bild hinzuzufügen, geben Sie die URL des Bildes in das **src**-Attribut des HTML **&lt;img&gt;**-Tags ein.

> [!NOTE]
> E-Mail-Clients legen Layout- und Stilbeschränkungen fest, die möglicherweise Anpassungen an HTML und CSS erfordern, die Sie für den Nachrichtentext verwenden. Wir empfehlen Ihnen, sich mit den bewährten Verfahren zum Erstellen von HTML vertraut zu machen, die von den gängigsten E-Mail-Clients unterstützt werden.

## <a name="add-placeholders-to-the-email-message-body"></a>Fügen Sie dem E-Mail-Nachrichtentext Platzhalter hinzu

Ihre E-Mail kann Platzhalter enthalten, die beim Generieren der E-Mail durch kundenspezifische und transaktionsspezifische Werte ersetzt werden. Platzhalter sind immer von Prozentzeichen (%) umgeben und werden direkt in das HTML-Dokument eingefügt.

Hier ist ein Beispiel.

```html
<p>
    Hello %customername%,<br />
    Order number %salesid%, can be picked up from the <b>%pickupstorename%</b> store.
</p>
```

### <a name="order-placeholders-sales-order-level"></a>Platzhalter bestellen (Kundenauftragsebene)

Die folgenden Platzhalter rufen Daten ab und zeigen sie an, die auf Kundenauftragsebene definiert sind (im Gegensatz zur Kundenzeilenebene).

| Platzhaltername     | Kostenträger                                                      |
| -------------------- | ------------------------------------------------------------ |
| `customername`         | Der Name des Debitors, der die Bestellung platziert hat.               |
| `customeraddress`      | Die Debitorenadresse.                                 |
| `customeremailaddress` | Die E-Mail-Adresse, die der Kunde an der Kasse eingegeben hat.     |
| `salesid`              | Die Auftragskennung des Auftrags.                                   |
| `orderconfirmationid`  | Die kanalübergreifende Kennung, die bei der Auftragserstellung generiert wurde.   |
| `channelid`            | Die Kennung des Einzelhandels- oder Online-Kanals, über den der Auftrag aufgegeben wurde. |
| `deliveryname`         | Der Name, der für die Lieferadresse spezifiziert ist.         |
| `deliveryaddress`      | Die Lieferadresse für versandte Bestellungen.                     |
| `deliverydate`         | Das Lieferdatum.                                           |
| `shipdate`             | Das Versanddatum.                                               |
| `modeofdelivery`       | Der Versandmodus der Bestellung.                              |
| `ordernetamount`       | Der Gesamtbetrag für die Bestellung abzüglich der Gesamtsteuer.         |
| `discount`            | Die Gesamtrabatt für die Bestellung.                            |
| `charges`              | Die Gesamtkosten für die Bestellung.                             |
| `tax`                  | Die Gesamtsteuern für die Bestellung.                                 |
| `total`                | Der Gesamtbetrag für die Bestellung.                              |
| `storename`            | Der Name des Shops, bei dem die Bestellung platziert wurde.            |
| `storeaddress`         | Die Adresse des Shops, der die Bestellung platziert hat.              |
| `storeopenfrom`        | Die Öffnungszeiten des Shops, der die Bestellung platziert hat.         |
| `storeopento`          | Die Schließzeiten des Shops, der die Bestellung platziert hat.         |
| `pickupstorename`      | Der Name des Shops, bei dem die Bestellung abgeholt wird.\*   |
| `pickupstoreaddress`   | Die Adresse des Shops, bei dem die Bestellung abgeholt wird.\* |
| `pickupopenstorefrom`  | Die Öffnungszeiten des Shops, bei dem die Bestellung abgeholt wird.\* |
| `pickupopenstoreto`    | Die Schließzeiten des Shops, bei dem die Bestellung abgeholt wird.\* |
| `pickupchannelid`     | Die Kanalkennung des Geschäfts, die für eine die Lieferart der Abholung angegeben ist.\* |
| `packingslipid`        | Die Kennung des Lieferscheins, der beim Verpacken von Positionen eines Auftrags generiert wurde.\* |

\*Diese Platzhalter geben nur dann Daten zurück, wenn sie für den Benachrichtigungstyp **Bestellung zur Abholung bereit** verwendet werden. 

### <a name="order-line-placeholders-sales-line-level"></a>Auftragspositionsplatzhalter (Verkaufspositionsebene)

Die folgenden Platzhalter rufen Daten für einzelne Produkte (Positionen) im Kundenauftrag ab und zeigen sie an.

| Platzhaltername               | Kostenträger |
|--------------------------------|-------------------|
| `productid`                      | <p>Die Kennung des Produkts. Diese Kennung berücksichtigt Varianten.</p><p><strong>Hinweis:</strong> Dieser Platzhalter wurde zugunsten von `lineproductrecid` eingestellt.</p> |
| `lineproductrecid`               | Die Kennung des Produkts. Diese Kennung berücksichtigt Varianten. Er identifiziert einen Artikel eindeutig auf Variantenebene. |
| `lineitemid`                     | Die Kennung des Produkts auf Produktebene. (Diese Kennung berücksichtigt keine Varianten.) |
| `lineproductvariantid`           | Die Kennung der Produktvariante. |
| `lineproductname`                | Der Name des Produkts. |
| `lineproductdescription`         | Die Beschreibung des Produkts. |
| `linequantity`                   | Die Anzahl der Einheiten, die für die Position bestellt wurden, plus die Maßeinheit (z. B. **ea** oder **Paar**). |
| `lineunit`                       | Die Maßeinheit für die Position. |
| `linequantity_withoutunit`       | Die Anzahl der Einheiten, die für die Position bestellt wurden, ohne die Maßeinheit. |
| `linequantitypicked`             | Wenn das **PickOrder**-Ereignis verwendet wird, ist dies die Anzahl der Einheiten, die ausgewählt wurden. Andernfalls, **0** (null). |
| `linequantitypicked_withoutunit` | Wenn das **PickOrder**-Ereignis verwendet wird, ist dies die Anzahl der Einheiten, die ausgewählt wurden, ohne die Maßeinheit. Andernfalls, **0** (null). |
| `linequantitypacked`             | Wenn die Ereignisse **PackOrder** und **Bestellung zur Abholung bereit** verwendet werden, ist dies die Anzahl der Einheiten, die gepackt wurden. Andernfalls, **0** (null). |
| `linequantitypacked_withoutuom`  | Wenn die Ereignisse **PackOrder** und **Bestellung zur Abholung bereit** verwendet werden, ist dies die Anzahl der Einheiten, die gepackt wurden, ohne die Maßeinheit. Andernfalls, **0** (null). |
| `linequantityshipped`            | Immer **0**, außer wenn bestimmte Ereignisse verwendet werden, wie in der nächsten Zeile beschrieben. |
| `linequantityshipped_withoutuom` | Wenn das **ShipOrder**-Ereignis verwendet wird, ist dies die Anzahl der Einheiten, die ausgewählt wurden, ohne die Maßeinheit. Andernfalls, **0** (null). |
| `lineprice`                      | Der Preis einer einzelnen Einheit. |
| `linenetamount`                  | Der Preis der Position nach Anzahl der Einheiten und Rabatt wird angewendet. |
| `linediscount`                   | Der Rabatt für eine einzelne Einheit. |
| `lineshipdate`                   | Das Versanddatum für die Position. |
| `linedeliverydate`               | Das Lieferdatum für die Position. |
| `linedeliverymode`               | Der Liefermodus für die Position. |
| `linedeliveryaddress`            | Die Lieferadresse für die Position. |
| `linepickupdate`                 | Das vom Kunden angegebene Abholdatum für Bestellungen mit der Lieferart Abholung. |
| `linepickuptimeslot`             | Das vom Kunden angegebene Abholdzeitraum für Bestellungen mit der Lieferart Abholung. |
| `giftcardnumber`                 | Die Geschenkkartennummer für Produkte vom Typ Geschenkkarte. |
| `giftcardbalance`                | Der Geschenkkartensaldo für Produkte vom Typ Geschenkkarte. |
| `giftcardmessage`                | Die Geschenkkartennachricht für Produkte vom Typ Geschenkkarte. |
| `giftcardpin`                    | Die PIN der Geschenkkarte für Produkte vom Typ Geschenkkarte. (Dieser Platzhalter gilt nur für externe Geschenkkarten.) |
| `giftcardexpiration`             | Das Ablaufdatum der Geschenkkarte für Produkte vom Typ Geschenkkarte. (Dieser Platzhalter gilt nur für externe Geschenkkarten.) |
| `giftcardrecipientname`          | Der Name des Geschenkkartenempfängers für Produkte vom Typ Geschenkkarte. |
| `giftcardbuyername`              | Der Name des Geschenkkartenkäufers für Produkte vom Typ Geschenkkarte. |

### <a name="format-of-order-line-placeholders-in-the-email-message-body"></a>Format der Bestellpositionsplatzhalter im E-Mail-Nachrichtentext

Wenn Sie den HTML-Code für die einzelnen Bestellpositionen im E-Mail-Nachrichtentext erstellen, umgeben Sie den sich wiederholenden HTML-Block und die Platzhalter für die Positionen mit den folgenden Platzhaltern. Beachten Sie, dass sich die Platzhalter in HTML-Kommentar-Tags befinden.

```html
<!--%tablebegin.salesline%-->

(Insert the repeating block of HTML and placeholders for individual lines here.)

<!--%tableend.salesline%-->
```

Hier ist ein Beispiel.

```HTML
<table>
    <tr>
        <td>Product name</td>
        <td>Quantity</td>
        <td>Price</td>
    </tr>
    <!--%tablebegin.salesline%-->
    <tr>
        <td>%lineproductname%</td>
        <td>%linequantity_withoutunit%</td>
        <td>%lineprice%</td>
    </tr>
    <!--%tableend.salesline%-->
</table>
```

## <a name="create-a-template-for-emailed-receipts"></a>Erstellen Sie eine Vorlage für per E-Mail gesendete Belege

Belege können per E-Mail an Kunden gesendet werden, die an einer Verkaufsstelle (POS) einkaufen. Im Allgemeinen sind die Schritte zum Erstellen der E-Mail-Belegvorlage dieselben wie die Schritte zum Erstellen von Vorlagen für andere Transaktionsereignisse. Die folgenden Änderungen sind jedoch erforderlich:

- Der **%message%**-Parthalter wird verwendet, um den Text der Quittung in die E-Mail einzufügen. Um sicherzustellen, dass der Belegtext korrekt gerendert wird, umgeben Sie den **%message%**-Platzhalter mit den HTML-Tags **&lt;pre&gt;** und **&lt;/pre&gt;**.
- Mit dem Platzhalter **%receiptid%** kann ein QR-Code oder ein Barcode angezeigt werden, der die Beleg-ID darstellt. (QR-Codes und Barcodes werden dynamisch generiert und von einem Drittanbieter bereitgestellt.) Weitere Informationen zum Anzeigen eines QR-Codes oder Barcodes in einer per E-Mail gesendeten Quittung finden Sie unter [Transaktions- und Quittungs-E-Mails einen QR-Code oder Barcode hinzufügen](add-qr-code-barcode-email.md).

## <a name="upload-the-email-html"></a>Laden Sie den E-Mail-HTML-Code hoch

Nachdem Sie den HTML-Code für Ihren Nachrichtentext erstellt und getestet haben, muss er in die Commerce-Zentrale hochgeladen werden. Derzeit kann E-Mail-HTML nicht exportiert werden. Daher müssen Sie die Masterkopie Ihres HTML-Codes außerhalb der Commerce-Zentrale verwalten.

Führen Sie die folgenden Schritte aus, um eine neue oder bearbeitete HTML-E-Mail-Vorlage hochzuladen.

1. Gehen Sie in der Commerce-Zentrale zu **Einzelhandel und Handel \> Zentralverwaltungseinrichtung \> Organisations-E-Mail-Vorlagen**.
1. Wählen Sie die Zeile für die Sprache aus, für die Sie HTML hinzufügen oder ersetzen möchten. Alternativ wählen Sie **Neu** aus, um eine Position für eine neue Sprache zu erstellen.
1. Wählen Sie **Bearbeiten** aus.
1. Im angezeigten Dialogfeld wählen Sie **Durchsuchen** aus. Navigieren Sie zu dem HTML-Dokument, das Sie hochladen möchten, wählen Sie es aus und wählen Sie dann **Öffnen** aus.
1. Wählen Sie **Hochladen** aus.
1. Nachdem Ihr E-Mail-HTML im Vorschaufenster angezeigt wurde, wählen Sie **OK** aus.
1. Stellen Sie sicher, dass das Kontrollkästchen **Hat Text** für die Zeile ausgewählt ist.

Wenn Sie die Commerce-Zentrale bereits für das Senden von E-Mails konfiguriert haben, wird Ihre neue oder aktualisierte E-Mail an alle Kunden gesendet, die eine Transaktion ausführen, die das der Vorlage zugeordnete Ereignis aufruft.

Weitere Informationen über die Konfiguration von E-Mails in Dynamics 365 Commerce finden Sie unter [E-Mails konfigurieren und senden](../fin-ops-core/fin-ops/organization-administration/configure-email.md).

## <a name="additional-resources"></a>Zusätzliche Ressourcen 

[Ein E-Mail-Benachrichtigungsprofil einrichten](email-notification-profiles.md)

[E-Mails konfigurieren und senden](../fin-ops-core/fin-ops/organization-administration/configure-email.md)

[Einrichten von E-Mail-Bons](/dynamicsax-2012/appuser-itpro/set-up-email-receipts)

[E-Mail-Zugänge von Modern POS senden](email-receipts.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
