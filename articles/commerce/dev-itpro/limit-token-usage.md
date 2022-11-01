---
title: Verwendung von Zahlungstoken einschränken
description: Dieser Artikel beschreibt die Funktion, die die Verwendung von Zahlungstoken in Microsoft Dynamics 365 Commerce einschränkt.
author: BrianShook
ms.date: 10/20/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2022-09-20
ms.openlocfilehash: 8092ab0724f33f21759aa84d25e0bdcb5b2ad5dd
ms.sourcegitcommit: 6bd8822f7aa781d596b70956bead834117cf302c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2022
ms.locfileid: "9709655"
---
# <a name="limit-payment-token-usage"></a>Verwendung von Zahlungstoken einschränken

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Dieser Artikel beschreibt die Funktion, die die Verwendung von Zahlungstoken in Microsoft Dynamics 365 Commerce einschränkt. Die Token-Verwendung ist auf den Umfang eines Verkaufsauftrags beschränkt oder wird, wenn der Kunde zustimmt, als Karte in der Datei gespeichert.

## <a name="key-terms"></a>Schlüsselbegriffe

| Zeitdauer | Description |
|---|---|
| Token | Ein referenzierter XML blob im Dynamics 365 System, der Zahlungsreferenzen für Transaktionszwecke speichert. |
| Karte in der Datei | Ein gespeicherter Kartenreferenz-Token, der für die künftige Verwendung im Dynamics 365-System oder im Zahlungs-Gateway vereinbart wurde und der spezifisch für ein Kundenkonto ist. |

Die Beschränkungen für die Verwendung von Zahlungstoken gelten für jede Umgebung, die einen Gateway-Zahlungsdienst verwendet, bei dem wiederkehrende Token eingesetzt werden. Der standardmäßige [Dynamics 365 Payment Connector für Adyen](adyen-connector.md) verwendet wiederkehrende Zahlungstoken, um nachfolgende Bestellvorgänge durchzuführen, z.B. Autorisierungsanpassungen und erneute Autorisierungen.

Um zu steuern, wie diese wiederkehrenden Zahlungstoken im gesamten System verwendet werden, schränkt die Funktion **Zahlungstoken auf den Auftragskontext beschränken** die Verwendung eines wiederkehrenden Tokens auf den Umfang eines Verkaufsauftrags im System ein. Wenn sie aktiviert ist, ändert die Funktion die Benutzeroberfläche (UI) Commerce headquarters, indem sie die Zahlungseingabeseiten aktualisiert und die Möglichkeit einschränkt, Zahlungsreferenzen früherer Kunden zur Verwendung in neuen Transaktionen auszuwählen.

Diese Funktion hilft bei der Einhaltung der Nutzungsregeln für einige Zahlungsaussteller wie Visa. In den [Visa Core Rules and Visa Product and Service Rules](https://usa.visa.com/content/dam/VCOM/download/about-visa/visa-rules-public.pdf) legt Visa fest, dass die Verwendung von Zahlungstoken auf den Umfang einer Transaktion beschränkt sein sollte, es sei denn, der Karteninhaber stimmt etwas anderem zu.

Die Funktion **Verwendung von Zahlungstoken auf den Auftragskontext beschränken** ist nur relevant, wenn Sie einen Gateway-Dienst verwenden, der wiederkehrende Zahlungstoken-Referenzen verwendet.

## <a name="enable-the-feature"></a>Die Funktion aktivieren

Um die Funktion **Zahlungstoken im Bestellkontext einschränken** zu aktivieren, gehen Sie in Commerce headquarters für Ihre Umgebung zu **Arbeitsbereiche \> Funktionsverwaltung**, suchen und wählen Sie **Zahlungstoken im Bestellkontext einschränken** in der Liste und wählen Sie dann **Jetzt aktivieren**.

## <a name="limit-payment-token-usage"></a>Verwendung von Zahlungstoken einschränken

Wenn die Funktion aktiviert ist, werden die Seiten Commerce headquarters, die für die Erfassung von Zahlungsformen verwendet werden, aktualisiert, wie sie auf die für den Kunden hinterlegten Zahlungsformen verweisen. Diese Aktualisierung wird sich hauptsächlich auf zwei Vorgänge auswirken:

- Die Art und Weise, wie eine in der Datei gespeicherte Kundenkarte im Namen eines Kunden eingegeben wird
- Wie Zahlungsinformationen für einen Kunden für zukünftige Zahlungseingänge in Verkaufsaufträgen gespeichert werden

Wenn ein Kunde Transaktionen über Commerce-Kanäle tätigt, werden die Zahlungsinformationen mit einem Verkaufsauftragskontext gespeichert. Der Kontext des Verkaufsauftrags schränkt den Zahlungstoken ein, sodass er nicht als Zahlungsreferenz gegen den Datensatz des Kunden auf Zahlungsseiten für neue oder bearbeitete Verkaufsaufträge in Commerce headquarters verwendet wird.

### <a name="payment-form-changes"></a>Änderungen am Formular für Zahlungen

Wenn ein Benutzer des Call-Centers oder Commerce headquarters eine Zahlung für einen Kunden gegen einen Verkaufsauftrag vornimmt, werden auf der Zahlungsseite Details zur Auswahl der Zahlungsmethode angezeigt. Wenn die Funktion **Verwendung von Zahlungstoken auf den Auftragskontext beschränken** aktiviert ist und ein Benutzer auf der Zahlungsseite das Pluszeichen (**+**) auswählt, werden nur gespeicherte Datensätze mit „Karte in der Datei“ angezeigt. Änderungen erfordern, dass der Benutzer des Call-Centers oder Commerce headquarters die vollständigen Zahlungsdaten eingibt, die der Kunde beim Ausfüllen der Seite **Zahlungsinformationen des Kunden eingeben** für die neue Transaktion des Verkaufsauftrags angegeben hat.

Die Liste der Werte für das Feld **Nummer** enthält nur Kartenreferenzen, die mit dem Kunden verbunden sind, der die Karte in den Akten hat. Es filtert alle früheren Zahlungsreferenzen heraus, die nicht auf einen Verkaufsauftrag bezogen sind.

Das Pluszeichen (**+**) unter dem Feld **Nummer** bleibt verfügbar und kann verwendet werden, um die Zahlungsinformationen einzugeben, die der Kunde für die Transaktion angegeben hat, die mit dem zu verarbeitenden Verkaufsauftrag verknüpft ist.

### <a name="how-cards-on-file-work"></a>Wie Karten in der Datei funktionieren

Wenn die Funktion **Zahlungstoken auf den Auftragskontext beschränken** aktiviert ist, ist eine Karte auf Datei ein wiederkehrender Zahlungstoken, der für einen Datensatz des Kunden gespeichert wird und nicht auf den Umfang eines Verkaufsauftrags beschränkt ist. Eine Karte auf Datei ermöglicht Benutzern Commerce headquarters eine schnelle Referenz, wenn sie die Zahlungsseite für eine neue Verkaufsauftragszahlung ausfüllen. Diese Token-Referenz ist nur in der Dynamics 365 Umgebung anwendbar. Für Online-Kanäle, die einen Zahlungs-Gateway-Service verwenden, der es Benutzern ermöglicht, eine Zahlungsmethode für die zukünftige Verwendung im Zahlungsmodul iFrame zu speichern, speichert der Zahlungs-Gateway diese Referenzen sicher als eine separate Referenz auf die Dynamics 365-Karte in der Datei.

Wenn zum Beispiel der Konnektor für Adyen Dynamics 365 Commerce in einem Online-Kanal verwendet wird, sehen Kunden, die ihre Kreditkartendaten im Zahlungsmodul iFrame eingeben, bei der Authentifizierung nur die vom Gateway-Dienst gespeicherten Kartenreferenzen für ihren nächsten Online-Kauf. Sie sehen die in der Dynamics 365 Umgebung gespeicherte Karte nicht als Option im Zahlungsmodul iFrame. Ähnlich verhält es sich, wenn Kunden eine Bestellung über das Call-Center aufgeben: Ihre online gespeicherten Kartenreferenzen werden dem Call-Center-Benutzer nicht als Optionen angezeigt. Der Call-Center-Benutzer sieht nur frühere Kartenreferenzen aus dem Dynamics 365-System (wie vom Kunden vereinbart), die er für zukünftige Bestellungen speichern kann.

Benutzer Commerce headquarters können eine Kartei für einen Kunden speichern, indem sie zu **Retail und Commerce \> Kunden** gehen und den Datensatz des Kundenkontos auswählen. Im Bereich **Kunden \> Einrichten** können Benutzer, die über Berechtigungen zur Verarbeitung der Zahlungsseiten verfügen, auf der Eingabeseite **Kreditkarten** eine Zahlungskarte eingeben, die für künftige Transaktionen auf Datei festgelegt wird. Dieser Vorgang hilft, Zeit zu sparen, wenn künftige Zahlungen für Verkaufsaufträge des Kunden bearbeitet werden. Benutzer des Call-Centers und Commerce headquarters sollten die Karte nur dann eingeben, wenn der Kunde zustimmt, die Kartenreferenz für künftige Transaktionen zu verwenden.

Mit dem Kontrollkästchen **Zur zukünftigen Verwendung speichern** unten auf den Zahlungsseiten Commerce headquarters können Benutzer die Karte zur zukünftigen Verwendung in der Datei speichern. Dieses Kontrollkästchen sollte nur verwendet werden, wenn der Kunde zustimmt, die gespeicherte Karte für zukünftige Transaktionen zu verwenden. Sie können das Kontrollkästchen **Zur zukünftigen Verwendung speichern** einblenden oder einschränken, indem Sie die Option **Kundenkarte in Datei zulassen** auf der Registerkarte **Zahlung** der Seite **Call-Center-Parameter** in Commerce headquarters verwenden. Wenn diese Option auf **Ja** festgelegt ist, können Benutzer Commerce headquarters, die die Berechtigung haben, Zahlungsseiten zu verarbeiten, eine Karte in der Datei speichern, indem sie das Kontrollkästchen **Zur späteren Verwendung speichern** verwenden. Wenn die Option auf **Nein** festgelegt ist, steht das Kontrollkästchen Benutzern Commerce headquarters, die über Berechtigungen zum Verarbeiten von Zahlungsseiten verfügen, nicht zur Verfügung. Die Option **Kundenkarte in der Datei zulassen** kann verwendet werden, wenn Ihre Firma die Verwendung von wiederkehrenden Token in Commerce headquarters einschränken möchte, aber noch nicht zulassen will, dass eine Karte in der Datei gespeichert wird, ohne dass ein Verfahren zur Sicherstellung der Zustimmung des Kunden vorhanden ist.

### <a name="commerce-headquarters-pages-where-the-recurring-token-restrictions-are-enforced"></a>Seiten in Commerce headquarters, auf denen die Einschränkungen für wiederkehrende Token durchgesetzt werden

Die Token-Einschränkung betrifft die folgenden Bereiche in Commerce headquarters, wenn die Funktion aktiviert ist:

- Kundenzahlungsinformationen bei **Verkaufsauftrag \> Zahlungen \> Kundenzahlung eingeben**
- Anschlussaufträge
- Teilzahlungen
- Debitoren-Kreditkartenzahlungen

### <a name="manage-payment-tokens-archiving-or-removal"></a>Zahlungstoken verwalten (Archivierung oder Entfernung)

Zahlungstoken, die erstellt wurden, bevor das Flag der Funktion **Zahlungstoken-Verwendung auf den Bestellkontext beschränken** aktiviert wurde (oder während die Funktion deaktiviert war), bleiben im System „nicht abgedeckt“ und können in Auswahllisten auf der Zahlungsseite Commerce headquarters referenziert werden. Diese Token können in Commerce headquarters auf zwei Arten regelmäßig entfernt werden:

- Verwenden Sie die Seite **Kreditkartentransaktionsdaten archivieren**, um einen Auftrag festzulegen, der die Zahlungstoken regelmäßig bereinigt oder archiviert. Wenn Sie die Option **Daten ohne Archivierung löschen** auf **Ja** festlegen, werden die Token, die der Einstellung **Mindestalter der Transaktion (in Tagen)** entsprechen, gelöscht. Weitere Informationen finden Sie unter [Kreditkartentransaktionsdaten archivieren](archive-cc-data.md).
- Verwenden Sie die neue Seite **Kreditkarten-Token löschen** (**Debitoren \> Abfragen und Berichte \> Bereinigen \> Kreditkarten-Token löschen**), mit der Sie einen Batch-Auftrag ausführen oder festlegen können, der Zahlungs-Token löscht. Legen Sie die folgenden Parameter fest:

    - Der Wert **Mindestalter der Token in Tagen** muss 90 Tage oder mehr betragen.
    - Mit den Einstellungen **Im Hintergrund ausführen** können Sie Einstellungen für **Wiederholung** oder **Warnungen** festlegen.
    - Es kann eine Batch-Gruppe zugewiesen werden, um die Aufgabe für eine bestimmte Gruppe auszuführen.
    - Wenn die Option **Privat** auf **Ja** festgelegt ist, kann nur der Benutzer, der den Auftrag erstellt, diesen ausführen.
    - Wenn Sie für die Option **Kritischer Auftrag** die Option **Ja** festlegen, wird der Status des Auftrags aktiv verfolgt.

Gelöschte Token können nicht wiederhergestellt werden. Legen Sie das Feld **Mindestalter für Token in Tagen** auf einen Bereich fest, der der längsten Lebensdauer der Transaktion in Ihrer Umgebung entspricht (von der Autorisierung bis zur Erfassung oder Rückerstattung).

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[FAQs zu Zahlungen](payments-retail.md)

[Auschecken-Modul](../add-checkout-module.md)

[Zahlungsmodul](../payment-module.md)
