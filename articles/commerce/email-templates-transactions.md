---
title: Mail-Vorlagen für Transaktionsereignisse erstellen
description: In diesem Thema wird beschrieben, wie Sie E-Mail-Vorlagen für Transaktionsereignisse in Microsoft Dynamics 365 Commerce erstellen, hochladen und konfigurieren.
author: bicyclingfool
manager: annbe
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: ea484bfc1e9b293c53d7293c50630c4955000131
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4412477"
---
# <a name="create-email-templates-for-transactional-events"></a>Mail-Vorlagen für Transaktionsereignisse erstellen

[!include [banner](includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie E-Mail-Vorlagen für Transaktionsereignisse in Microsoft Dynamics 365 Commerce erstellen, hochladen und konfigurieren.

## <a name="overview"></a>Übersicht

Dynamics 365 Commerce bietet eine sofort einsatzbereite Lösung zum Senden von E-Mails, die Kunden über Transaktionsereignisse informieren (z. B. wenn eine Bestellung aufgegeben wird, eine Bestellung zur Abholung bereit ist oder eine Bestellung versandt wurde). In diesem Thema werden die Schritte zum Erstellen, Hochladen und Konfigurieren der E-Mail-Vorlagen beschrieben, die zum Senden von Transaktions-E-Mails verwendet werden.

## <a name="create-an-email-template"></a>E-Mail-Vorlage erstellen

Bevor Sie ein bestimmtes Transaktionsereignis einer E-Mail-Vorlage zuordnen können, müssen Sie die Vorlage erstellen.

Führen Sie folgende Schritte aus, um eine E-Mail-Vorlage zu erstellen:

1. Gehen Sie in der Commerce-Zentrale zu **E-Mail-Vorlagen der Organisation**, die unter **Einzelhandel und Handel \> Einrichtung des Hauptsitzes \> E-Mail-Vorlagen der Organisation** oder **Organisationsverwaltung \> Installieren \> E-Mail-Vorlagen der Organisation** sind.
1. Wählen Sie **Neu** aus.
1. Unter **Allgemeines** setzen Sie die folgenden Felder:

    - **E-Mail-Kennung** – Die E-Mail-Kennung ist die eindeutige Kennung für eine Vorlage und der Wert, der angezeigt wird, wenn Sie eine Vorlage auswählen, die einem Ereignis zugeordnet werden soll.
    - **E-Mail-Beschreibung** – In diesem optionalen Feld können Sie eine Beschreibung der Vorlage bereitstellen. Der von Ihnen eingegebene Wert wird nur in der Commerce-Zentrale angezeigt.
    - **Absendername** – Der von Ihnen eingegebene Name wird bei den meisten E-Mail-Clients im Feld „Von“ angezeigt.
    - **Absender-E-Mail** – Geben Sie die E-Mail-Adresse ein, die für E-Mails verwendet werden soll, die mithilfe dieser Vorlage gesendet werden.
    - **Standard-Sprachcode** – Dieses Feld gibt die lokalisierte Version der E-Mail an, die standardmäßig gesendet wird, wenn der Kanal, der diese Vorlage aufruft, keine Sprache bereitstellt.

1. Wählen Sie unter **Inhalt der E-Mail-Nachricht** die Option **Neu** aus.
1. Im Feld **Sprache** geben die Sprache für die E-Mail-Vorlage ein. Sie können später weitere Sprachen und lokalisierte Vorlagen hinzufügen.
1. Im Feld **Betreff** geben Sie den Betreff der E-Mail ein, der in der E-Mail angezeigt werden soll.
1. Wählen Sie **Bearbeiten** aus, um Ihre E-Mail-Vorlage hochzuladen.

## <a name="create-an-email-message-body-by-using-html"></a>Erstellen Sie einen E-Mail-Nachrichtentext mithilfe von HTML

Der Nachrichtentext Ihrer E-Mail besteht aus HTML. Sie können jedes für HTML- und Inline-Cascading Style Sheets verwenden (CSS) zulässige Layout, Stilelement und Branding. Sie können Bilder auch verwenden, wenn Sie sie auf einem öffentlich verfügbaren Webendpunkt hosten. Um ein Bild hinzuzufügen, geben Sie die URL des Bildes in das **src**-Attribut des HTML **&lt;img&gt;**-Tags ein.

> [!NOTE]
> E-Mail-Clients legen Layout- und Stilbeschränkungen fest, die möglicherweise Anpassungen an HTML und CSS erfordern, die Sie für den Nachrichtentext verwenden. Wir empfehlen Ihnen, sich mit den Best Practices zum Erstellen von HTML vertraut zu machen, die von den beliebtesten E-Mail-Clients unterstützt werden.

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

| Platzhaltername    | Platzhalterwert                                                |
|---------------------|------------------------------------------------------------------|
| customername        | Der Name des Debitors, der die Bestellung platziert hat.                   |
| salesid             | Die Auftragskennung des Auftrags.                                       |
| deliveryaddress     | Die Lieferadresse für versandte Bestellungen.                         |
| customeraddress     | Die Debitorenadresse.                                     |
| deliverydate        | Das Lieferdatum.                                               |
| shipdate            | Das Versanddatum.                                                   |
| modeofdelivery      | Der Versandmodus der Bestellung.                                  |
| Zuschläge             | Die Gesamtkosten für die Bestellung.                                 |
| Steuer                 | Die Gesamtsteuern für die Bestellung.                                     |
| Gesamt               | Der Gesamtbetrag für die Bestellung.                                  |
| ordernetamount      | Der Gesamtbetrag für die Bestellung abzüglich der Gesamtsteuer.             |
| Rabatt            | Die Gesamtrabatt für die Bestellung.                                |
| storename           | Der Name des Shops, bei dem die Bestellung platziert wurde.                |
| storeaddress        | Die Adresse des Shops, der die Bestellung platziert hat.                  |
| storeopenfrom       | Die Öffnungszeiten des Shops, der die Bestellung platziert hat.             |
| storeopento         | Die Schließzeiten des Shops, der die Bestellung platziert hat.             |
| pickupstorename     | Der Name des Shops, bei dem die Bestellung abgeholt wird.         |
| pickupstoreaddress  | Die Adresse des Shops, bei dem die Bestellung abgeholt wird.      |
| pickupopenstorefrom | Die Öffnungszeiten des Shops, bei dem die Bestellung abgeholt wird. |
| pickupopenstoreto   | Die Schließzeiten des Shops, bei dem die Bestellung abgeholt wird. |

### <a name="order-line-placeholders-sales-line-level"></a>Auftragspositionsplatzhalter (Verkaufspositionsebene)

Die folgenden Platzhalter rufen Daten für einzelne Produkte (Positionen) im Kundenauftrag ab und zeigen sie an.

| Platzhaltername               | Platzhalterwert |
|--------------------------------|-------------------|
| productid                      | Die Produkt-ID für die Linie. |
| lineproductname                | Der Name des Produkts. |
| lineproductdescription         | Die Beschreibung des Produkts. |
| linequantity                   | Die Anzahl der Einheiten, die für die Position bestellt wurden, plus die Maßeinheit (z. B. **ea** oder **Paar**). |
| lineunit                       | Die Maßeinheit für die Position. |
| linequantity_withoutunit       | Die Anzahl der Einheiten, die für die Position bestellt wurden, ohne die Maßeinheit. |
| linequantitypicked             | Wenn das **PickOrder**-Ereignis verwendet wird, ist dies die Anzahl der Einheiten, die ausgewählt wurden. Andernfalls, **0** (null). |
| linequantitypicked_withoutunit | Wenn das **PickOrder**-Ereignis verwendet wird, ist dies die Anzahl der Einheiten, die ausgewählt wurden, ohne die Maßeinheit. Andernfalls, **0** (null). |
| linequantitypacked             | Wenn die Ereignisse **PackOrder** und **Bestellung zur Abholung bereit** verwendet werden, ist dies die Anzahl der Einheiten, die gepackt wurden. Andernfalls, **0** (null). |
| linequantitypacked_withoutuom  | Wenn die Ereignisse **PackOrder** und **Bestellung zur Abholung bereit** verwendet werden, ist dies die Anzahl der Einheiten, die gepackt wurden, ohne die Maßeinheit. Andernfalls, **0** (null). |
| linequantityshipped            | Immer **0**, außer wenn bestimmte Ereignisse verwendet werden, wie in der nächsten Zeile beschrieben. |
| linequantityshipped_withoutuom | Wenn das **ShipOrder**-Ereignis verwendet wird, ist dies die Anzahl der Einheiten, die ausgewählt wurden, ohne die Maßeinheit. Andernfalls, **0** (null). |
| lineprice                      | Der Preis einer einzelnen Einheit. |
| linenetamount                  | Der Preis der Position nach Anzahl der Einheiten und Rabatt wird angewendet. |
| linediscount                   | Der Rabatt für eine einzelne Einheit. |
| lineshipdate                   | Das Versanddatum für die Position. |
| linedeliverydate               | Das Lieferdatum für die Position. |
| linedeliverymode               | Der Liefermodus für die Position. |
| linedeliveryaddress            | Die Lieferadresse für die Position. |
| giftcardnumber                 | Die Geschenkkartennummer für Produkte vom Typ Geschenkkarte. |
| giftcardbalance                | Der Geschenkkartensaldo für Produkte vom Typ Geschenkkarte. |
| giftcardmessage                | Die Geschenkkartennachricht für Produkte vom Typ Geschenkkarte. |
| giftcardpin                    | Die Geheimzahl (PIN) der Geschenkkarte für Produkte vom Typ Geschenkkarte. (Dieser Platzhalter gilt nur für externe Geschenkkarten.) |
| giftcardexpiration             | Das Ablaufdatum der Geschenkkarte für Produkte vom Typ Geschenkkarte. (Dieser Platzhalter gilt nur für externe Geschenkkarten.) |
| giftcardrecipientname          | Der Name des Geschenkkartenempfängers für Produkte vom Typ Geschenkkarte. |
| giftcardbuyername              | Der Name des Geschenkkartenkäufers für Produkte vom Typ Geschenkkarte. |

### <a name="format-of-order-line-placeholders-in-the-email-message-body"></a>Format der Bestellpositionsplatzhalter im E-Mail-Nachrichtentext

Wenn Sie den HTML-Code für die einzelnen Bestellpositionen im E-Mail-Nachrichtentext erstellen, umgeben Sie den sich wiederholenden HTML-Block und die Platzhalter für die Positionen mit den folgenden Platzhaltern, die in HTML-Kommentar-Tags eingefügt werden.

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

- Die E-Mail-Kennung der E-Mail-Vorlage muss **emailRecpt** lauten.
- Der Text der Quittung wird mithilfe des **%message%**-Platzhalters in die E-Mail eingefügt. Um sicherzustellen, dass der Belegtext korrekt gerendert wird, umgeben Sie **%message%**-Platzhalter mit den HTML-Tags **&lt;pre&gt;** und **&lt;/pre&gt;**.
- Zeilenumbrüche im HTML-Code für Kopf- und Fußzeile der E-Mail werden in **&lt;br /&gt;**-HTML-Tags konvertiert, damit der Belegkörper korrekt gerendert wird. Um unerwünschte vertikale Leerzeichen in Ihren Quittungs-E-Mails zu entfernen, entfernen Sie Zeilenumbrüche an allen Stellen im HTML, an denen keine vertikalen Leerzeichen erforderlich sind.

Weitere Informationen über die Konfiguration von E-Mail-Belegen finden Sie unter [Einrichten von E-Mail-Bons](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-email-receipts).

## <a name="upload-the-email-html"></a>Laden Sie den E-Mail-HTML-Code hoch

Nachdem Sie den HTML-Code für Ihren Nachrichtentext erstellt und getestet haben, muss er in die Commerce-Zentrale hochgeladen werden. Derzeit kann E-Mail-HTML nicht exportiert werden. Daher müssen Sie die Masterkopie Ihres HTML-Codes außerhalb der Commerce-Zentrale verwalten.

Führen Sie die folgenden Schritte aus, um eine neue oder bearbeitete HTML-E-Mail-Vorlage hochzuladen.

1. Gehen Sie in der Commerce-Zentrale zu **Retail und Commerce \> Zentralverwaltungseinrichtung \> Organisations-E-Mail-Vorlagen**.
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

[Einrichten von E-Mail-Bons](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-email-receipts)

[E-Mail-Zugänge von Modern POS senden](email-receipts.md)
