---
title: Mechanismus zur Verlagerung der Steuerschuld für USt./GST-Regelung
description: In diesem Thema wird erläutert, wie die Verlagerung der Steuerschuld (MwSt.) für europäische Länder, Saudi-Arabien und Singapur eingerichtet wird.
author: epodkolz
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Saudi Arabia, Spain, Sweden, United Kingdom, Singapore, Bahrain, Kuwait, Oman, Qatar
ms.author: epodkolz
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 326a74d0f962cf0455033b04950ded7ca26bfc77
ms.sourcegitcommit: e40a9fac5bac9f57a6dcfe73a1f21856eab9b6a9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/02/2021
ms.locfileid: "7594718"
---
# <a name="reverse-charge-mechanism-for-vatgst-scheme"></a>Mechanismus zur Verlagerung der Steuerschuld für USt./GST-Regelung

[!include [banner](../includes/banner.md)]

In diesem Thema wird ein allgemeiner Ansatz zum Einrichten der Funktionalität zur Verlagerung der Steuerschuld für Länder/Regionen beschrieben, welche die USt.- oder GST-Regelungen anwenden.
                                                                                 
Die länder-/regionsspezifische Verfügbarkeit der Funktionalität wird durch die folgenden Funktionen im Arbeitsbereich **Funktionsverwaltung** verwaltet.

| Funktion                                              | Land/Region                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Keine spezielle Funktion                                | Österreich </br>Belgien </br>Bulgarien </br>Kroatien </br>Zypern </br>Tschechische Republik </br>Dänemark  </br>Estland  </br>Finnland  </br>Frankreich  </br>Deutschland  </br>Ungarn  </br>Island  </br>Irland  </br>Italien  </br>Lettland  </br>Liechtenstein  </br>Litauen  </br>Luxemburg  </br>Niederlande  </br>Norwegen Polen </br>Portugal </br>Rumänien  </br>Saudi-Arabien </br>Singapur  </br>Slowakei  </br>Slowenien  </br>Spanien  </br>Schweden  </br>Schweiz  </br>Vereinigtes Königreich  </br>Vereinigte Arabische Emirate |
| Verlagerung der Steuerschuld für weitere Länder            | Bahrain  </br>Kuwait  </br>Oman  </br>Katar                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Mechanismus zur Verlagerung der Steuerschuld für USt./GST-Regelung aktivieren | Alle anderen Länder/Regionen, außer:  </br>Brasilien  </br>Indien  </br>Russische Föderation                                                                                                                                                                                                                                                                                                                                                                                         |
 
 Weitere Informationen finden Sie im Abschnitt [Mechanismus für Verlagerung der Steuerschuld für USt./GST-Regelung aktivieren](#enable-reverse-charge) weiter unten in diesem Thema.

Die Verlagerung der Steuerschuld ist ein Steuerschema, das die Zuständigkeit für die Buchhaltung und das Melden der Mehrwertsteuer vom Verkäufer auf den Einkäufer von Waren und/oder Dienstleistungen verschiebt. Daher melden Empfänger von Waren und/oder Dienstleistungen sowohl die Ausgangssteuer (in der Rolle eines Verkäufers) als auch die Vorsteuer (in der Rolle des Einkäufers) in ihrer MwSt.-Abrechnung.

Das Schema der Verlagerung der Steuerschuld wird in einigen Ländern oder Regionen nur für einige Waren und/oder Dienstleistungen implementiert, und es gibt zusätzliche Bedingungen oder Schwellenwerte bei Umsatzbeträgen. In anderen Ländern oder Regionen hängt die Zuständigkeit für die Mehrwertsteuerzahlung vom Status des Lieferanten und des Käufers ab. Wenn der Käufer verpflichtet ist, die MwSt. zu bezahlen, muss diese Tatsache eindeutig auf der Rechnung angegeben werden, die vom Lieferanten gestellt wird. So müssen z. B. die Worte "Verlagerung der Steuerschuld" auf der Rechnung vorkommen und es muss angegeben werden, welche Positionen vom Steuerschuldumkehrschema erfasst werden. 

Um die Verlagerung der Steuerschuld anzuwenden, müssen Sie die folgende Einrichtung abschließen.

## <a name="set-up-sales-tax-codes"></a>Mehrwertsteuercodes einrichten
Es wird empfohlen, dass Sie separate Mehrwertsteuercodes für Verkaufs- und Einkaufsvorgänge verwenden.

<table>
<tr>
<td><strong>Mehrwertsteuercode für Umsätze</strong></td>
<td>Erstellen Sie einen Mehrwertsteuercode für Verkaufsvorgänge mit Verlagerung der Steuerschuld (<strong>Steuer</strong> &gt; <strong>Indirekte Steuern</strong> &gt; <strong>Mehrwertsteuer</strong> &gt; <strong>Mehrwertsteuercodes</strong>).
</td>
</tr>
<tr>
<td><strong>Mehrwertsteuercode für Einkäufe</strong></td>
<td><p>Erstellen Sie positive und negative Mehrwertsteuercodes für die Verlagerung der Steuerschuld für Einkäufe (<strong>Steuer</strong> &gt; <strong>Indirekte Steuern</strong> &gt; <strong>Mehrwertsteuer</strong> &gt; <strong>Mehrwertsteuercodes</strong>).</p>
<ol>
<li>Erstellen Sie einen Mehrwertsteuercode mit positivem Wert.</li>
<li>Erstellen Sie einen Mehrwertsteuercode mit negativem Wert. Legen Sie die <strong>Negativen Mehrwertsteuersatz zulassen</strong>-Option auf <strong>Ja</strong> fest.
Sie müssen diesen negativen Mehrwertsteuercode einer Artikel-Mehrwertsteuergruppe zuweisen und anschließend diese Artikel-Mehrwertsteuergruppe den Artikeln zuweisen, für die die Verlagerung der Steuerschuld gilt.</li>
</ol>
<p>Weitere Informationen finden Sie im nächsten Abschnitt &quot;Mehrwertsteuergruppen und Artikel-Mehrwertsteuergruppen einrichten&quot;.</p>
</td>
</tr>
</table>

## <a name="set-up-sales-tax-groups-and-item-sales-tax-groups"></a><a name="sales-tax-item-sales-tax-groups"></a>Mehrwertsteuergruppen und Artikel-Mehrwertsteuergruppen einrichten
Es wird empfohlen, dass Sie separate Mehrwertsteuergruppen für Verkaufs- und Einkaufsvorgänge verwenden.

<table>
<tr>
<td><strong>Mehrwertsteuergruppen für Verkäufe</strong></td>
<td>Erstellen Sie eine Mehrwertsteuergruppe für Verkaufsvorgänge mit Verlagerung der Steuerschuld (<strong>Steuer</strong> &gt; <strong>Indirekte Steuern</strong> &gt; <strong>Mehrwertsteuer</strong> &gt; <strong>Mehrwertsteuergruppen</strong>). Geben Sie auf der Registerkarte <strong>Einstellungen</strong> den Mehrwertsteuercode für die Verlagerung der Steuerschuld in dieser Gruppe an. Aktivieren Sie die Kontrollkästchen <strong>Befreit</strong> und <strong>Verlagerung der Steuerschuld</strong> für den Mehrwertsteuercode.</td>
</tr>
<tr>
<td><strong>Mehrwertsteuergruppen für Einkäufe</strong></td>
<td>Erstellen Sie eine Mehrwertsteuergruppe für Einkaufsvorgänge mit Verlagerung der Steuerschuld (<strong>Steuer</strong> &gt; <strong>Indirekte Steuern</strong> &gt; <strong>Mehrwertsteuer</strong> &gt; <strong>Mehrwertsteuergruppen</strong>). Geben Sie auf der Registerkarte <strong>Einstellungen</strong> die positiven und negativen Mehrwertsteuercodes in dieser Gruppe an. Aktivieren Sie das Kontrollkästchen <strong>Verlagerung der Steuerschuld</strong> für den Mehrwertsteuercode mit negativem Wert.</td>
</tr>
<tr>
<td><strong>Artikel-Mehrwertsteuergruppen</strong></td>
<td>Erstellen oder aktualisieren Sie die Artikel-Mehrwertsteuergruppe mit dem Mehrwertsteuercode, der einen negativen Wert hat (<strong>Steuer</strong> &gt; <strong>Indirekte Steuern</strong> &gt; <strong>Mehrwertsteuer</strong> &gt; <strong>Artikel-Mehrwertsteuergruppen</strong>). Sie müssen den Produkten und Kategorien, für die die Verlagerung der Steuerschuld gilt, die Artikel-Mehrwertsteuergruppe zuweisen.</td>
</tr>
</table>

## <a name="set-up-reverse-charge-item-groups"></a><a name="reverse-charge-item-group"></a>Einrichten von Artikelgruppen für Verlagerungen der Steuerschuld
Auf der Seite **Artikelgruppen für die Verlagerung der Steuerschuld** (**Steuer** &gt; **Einstellungen** &gt; **Mehrwertsteuer** &gt; **Artikelgruppen für die Verlagerung der Steuerschuld**) können Sie Gruppen von Produkten bzw. Diensten oder Einzelprodukte bzw. -dienste definieren, auf die die Verlagerung der Steuerschuld angewendet werden kann. Definieren Sie für jede Artikelgruppen für die Verlagerung der Steuerschuld die Liste der Artikel, Artikelgruppen oder Kategorien für Verkäufe und/oder Einkäufe.

## <a name="set-up-reverse-charge-rules"></a><a name="reverse-charge-rules"></a>Regeln für die Verlagerungen der Steuerschuld einrichten
Auf der Seite **Regeln für die Verlagerung der Steuerschuld** (**Steuer** &gt; **Einstellungen** &gt; **Mehrwertsteuer** &gt; **Regeln für die Verlagerung der Steuerschuld**) können Sie die Anwendbarkeitsregeln zu Einkaufs- und Vertriebszwecke definieren. Sie können einen Satz von Regeln für die Verlagerung der Steuerschuld konfigurieren. Legen Sie für jede Regel die folgenden Felder fest:

- **Dokumenttyp** – Wählen Sie **Bestellung**, **Kreditorenrechnungserfassung**, **Auftrag**, **Freitextrechnung**, **Debitorenrechnungserfassung** und/oder **Kreditorenrechnung** aus.
- **Länder-/Regionstyp des Partners** – Wählen Sie **Inland**, **EU**, **GCC** oder **Ausland** aus. Falls die Regel für alle Handelspartner unabhängig vom Land oder der Region ihrer Adresse gilt, wählen Sie **Alle** aus.
- **Inländische Lieferadresse** – Aktivieren Sie dieses Kontrollkästchen, um die Regel auf Lieferungen im gleichen Land oder der gleichen Region anzuwenden. Dieses Kontrollkästchen kann nicht für die Dokumenttypen **Kreditorenrechnungserfassung** und **Debitorenrechnungserfassung** aktiviert werden.
- **Artikelgruppe für Verlagerung der Steuerschuld** – Wählen Sie die Gruppe aus, auf die die Regel angewendet werden kann.
- **Schwellenwertbetrag** – Das Schema der Verlagerung der Steuerschuld wird nur dann bei einer Rechnung angewendet, wenn der Wert der Artikel und/oder Services in der Gruppe der Verlagerung der Steuerschuld das hier angegebene Limit überschreitet.

Sie können auch die Felder **Gültigkeitsdatum** und **Ablaufdatum** verwenden, um den Zeitraum festzulegen, in dem die Regel gültig ist.

Darüber hinaus können Sie angeben, ob eine Benachrichtigung angezeigt wird und die Dokumentposition mit der Mehrwertsteuergruppe für Verlagerungen der Steuerschuld aktualisiert wird, wenn die Bedingung für diese Dokumentposition erfüllt wird. Die folgenden Optionen sind verfügbar:

- **Keine** – Die Dokumentposition wird nicht aktualisiert.
- **Bestätigung** – Eine Benachrichtigung wird angezeigt, um zu bestätigen, dass die Verlagerung der Steuerschuld angewendet werden kann.
- **Satz** – Die Dokumentposition wird ohne zusätzliche Benachrichtigung aktualisiert.

## <a name="set-up-countryregion-properties"></a><a name="Set-up-Country/region-properties"></a>Länder-/Regionseigenschaften einrichten
Stellen auf der **Außenhandelsparameter**-Seite (**Steuer** &gt; **Einrichtung** &gt; **Mehrwertsteuer** &gt; **Außenhandel** &gt; **Außenhandelsparameter**) auf der **Land-/Regionseigenschaften**-Registerkarte das Land/die Region der aktuellen juristischen Person auf *Inländisch* ein. Legen Sie den **Land-/Regionstyp** der EU-Länder/Regionen fest, die am EU-Handel mit der aktuellen juristischen Person mit *EU* teilnehmen. Legen Sie den **Land-/Regionstyp** der GCC-Länder/Regionen fest, die am GCC-Handel mit der aktuellen juristischen Person mit *GCC* teilnehmen.

## <a name="set-up-default-parameters"></a>Einrichten von Standardparametern
Um die Funktionen für die Verlagerung der Steuerschuld zu aktivieren, legen Sie auf der Seite **Hauptbuchparameter** auf der Registerkarte **Verlagerung der Steuerschuld** die Option **Verlagerung der Steuerschuld aktivieren** auf **Ja** fest. Wählen Sie in den Feldern **Mehrwertsteuergruppe für Bestellung** und **Mehrwertsteuergruppe für Auftrag** die standardmäßigen Mehrwertsteuergruppen aus. Wenn eine Anwendbarkeitsbedingung für die Verlagerung der Steuerschuld erfüllt wird, wird die Bestellposition für den Auftrag oder die Bestellung mit diesen Mehrwertsteuergruppen aktualisiert.

## <a name="reverse-charge-on-a-sales-invoice"></a><a name="reverse-charge-sale"></a>Verlagerung der Steuerschuld für eine Verkaufsrechnung
Bei Aufträgen mit dem Schema der Verlagerung der Steuerschuld stellt der Verkäufer keine Mehrwertsteuer in Rechnung. Stattdessen gibt die Rechnung die Artikel, für die die Verlagerung der Steuerschuld gilt, und den Gesamtbetrag der Verlagerung der Steuerschuld an.

Wenn eine Verkaufsrechnung mit Verlagerung der Steuerschuld gebucht wird, weisen die **Mehrwertsteuerbuchungen** Steuerart Mehrwertsteuer sowie Null Mehrwertsteuer aus, und die Kontrollkästchen **Verlagerung der Steuerschuld** und **Befreit** sind aktiviert.

## <a name="reverse-charge-on-a-purchase-invoice"></a><a name="reverse-charge-purchase"></a>Verlagerung der Steuerschuld für eine Einkaufsrechnung
Für Einkäufe mit dem Schema der Verlagerung der Steuerschuld agiert der Käufer, der die Rechnung mit der Verlagerung der Steuerschuld erhält, für MwSt.-Buchhaltungszwecke als Einkäufer und Verkäufer.

Wenn eine Einkaufsrechnung mit Verlagerung der Steuerschuld gebucht wird, werden zwei Mehrwertsteuerbuchungen erstellt. Eine Buchung hat Steuerart die **Vorsteuer**. Die zweite Buchung hat die Steuerart **Mehrwertsteuer** und das Kontrollkästchen **Verlagerung der Steuerschuld** ist aktiviert.

Im folgenden Bildschirmfoto hat eine Buchung die Steuerart **Vorsteuer** und die andere Buchung weist die Steuerart **Mehrwertsteuer** auf. 

![Gebuchte Mehrwertsteuer.](media/apac-sau-posted-sales-tax.png)

## <a name="enable-reverse-charge-mechanism-for-vatgst-scheme-feature"></a><a name="enable-reverse-charge"></a>Mechanismus für Verlagerung der Steuerschuld für USt./GST-Regelung aktivieren
Suchen Sie im Arbeitsbereich **Funktionsverwaltung** die Funktion **Aktivieren** und wählen Sie sie aus.

Nachdem Sie die Funktion aktiviert haben, wird die Registerkarte **Umkehr der Steuerschuld** in allen juristischen Personen verfügbar. Aktivieren Sie die Funktion zur Verlagerung der Steuerschuld für eine juristische Person, indem Sie die Option **Verlagerung der Steuerschuld aktivieren** auf **Ja**.

Die folgenden Seiten und Menüelemente, die mit der Funktionseinstellung zusammenhängen, sind verfügbar:
 - **Artikelgruppen für die Verlagerung der Steuerschuld** (**Steuer** > **Einrichten** > **Mehrwertsteuer** > **Artikelgruppen für die Verlagerung der Steuerschuld**). Weitere Informationen finden Sie im Abschnitt zum [Einrichten von Artikelgruppen für die Verlagerung der Steuerschuld](#reverse-charge-item-group).
 - **Regeln für die Verlagerung der Steuerschuld** (**Steuer** > **Einrichten** > **Mehrwertsteuer** > **Regeln für die Verlagerung der Steuerschuld**). Siehe [Regeln für die Verlagerungen der Steuerschuld einrichten](#reverse-charge-rules).
 - **Außenhandelsparameter** (**USt.** > **Einrichten** > **Mehrwertsteuer** > **Außenhandel** > **Außenhandelsparameter**). Siehe [Länder-/Regionseigenschaften einrichten](#Set-up-Country/region-properties)

Das Kontrollkästchen **Verlagerung der Steuerschuld** ist auf den Seiten **Mehrwertsteuergruppe** und **Gebuchte Mehrwertsteuer** verfügbar. Weitere Informationen finden Sie in den Abschnitten [Mehrwertsteuergruppen und Artikel-Mehrwertsteuergruppen einrichten](#sales-tax-item-sales-tax-groups), [Verlagerung der Steuerschuld für eine Verkaufsrechnung](#reverse-charge-sale) und [Verlagerung der Steuerschuld für eine Einkaufsrechnung](#reverse-charge-purchase).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]