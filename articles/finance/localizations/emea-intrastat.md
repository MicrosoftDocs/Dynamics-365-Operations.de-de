---
title: Intrastat – Übersicht
description: Dieser Artikel enthält Informationen zur Intrastat-Berichterstattung für den Warenhandel und in einigen Fällen Dienstleistungen unter Ländern/Regionen der Europäischen Union (EU).
author: mrolecki
ms.date: 11/30/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: Intrastat
audience: Application User
ms.reviewer: kfend
ms.custom:
- "28581"
- intro-internal
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: mrolecki
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 762de8a098c61bc0d717c038d6ca0ff6d649bff3
ms.sourcegitcommit: 2804b05214c87f76457608b5db072582ff339852
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/01/2022
ms.locfileid: "9815710"
---
# <a name="intrastat-overview"></a>Intrastat – Übersicht

[!include [banner](../includes/banner.md)]

Dieser Artikel enthält Informationen zur Intrastat-Berichterstattung für den Warenhandel und in einigen Fällen Dienstleistungen unter Ländern/Regionen der Europäischen Union (EU). Dieser Artikel bietet zudem einen Überblick über Berichterstellungsprozesse und beschreibt die erforderlichen Einstellungen und die Voraussetzungen.

Intrastat ist das System für die Sammlung von Informationen und Generierung von statistischen Daten über den Warenhandel zwischen Ländern/Regionen der Europäischen Union (EU). Intrastat-Berichte werden benötigt, wenn ein Produkt die Grenze eines anderen EU-Landes/einer anderen Region überschreitet. In einigen Ländern/Regionen sind Intrastat-Berichte außerdem für Dienstleistungen nötig. Erforderliche und optionale Elemente können im Intrastat-Bericht erfasst werden. Die folgenden Elemente sind erforderlich: Die Umsatzsteuernummer (VAT ID) der Partei, die für die Bereitstellung der Informationen verantwortlich ist, der Referenzzeitraum, der Flow (Eingang oder Ausgang), der Warencode mit acht Ziffern, der Mitgliedsstaat des Partners (Mitgliedsstaat der Lieferung bei Eingang und Mitgliedsstaat des Ziels bei Ausgang), der Warenwert, die Warenmenge (Nettogewicht und zugehörige Einheit) sowie die Art der Transaktion. Länder/Regionen können auch optionale Elemente gemäß verschiedenen Bedingungen erfassen. Einige optionale Elemente sind Ursprungsland/-region, Lieferbedingungen, die Art des Transports, ein ausführlicherer Warencode als CN8, die Region des Ursprungs auf Dispositionen und die Region des Ziels auf Eingängen, das Statistikverfahren, der statistische Wert, einer Beschreibung der Waren und der Anschluss/der Flughafen des Ladens/Entladens.

## <a name="overview-of-the-intrastat-reporting-process"></a>Überblick des Intrastat-Berichterstellungsprozesses
Die folgenden Abschnitte beschreiben den allgemeinen Informationsfluss, der für Intrastat-Berichte verwendet wird.

### <a name="enter-a-transaction-that-crosses-the-border-of-another-eu-countryregion"></a>Geben Sie eine Buchung ein, welche die Grenze eines anderen EU-Landes/einer anderen Region überschreitet

Eine Debitorenrechnung, eine Freitextrechnung, eine Einkaufsrechnung, Projektrechnung, ein Debitorenlieferschein, ein Kreditorenproduktzugang oder Umlagerungsauftrag wird in die Intrastat-Erfassung übertragen, wenn die Länder-/Regionsart des Ziels (auf Dispositionen) oder Lieferung (auf Eingängen) ist **EU**. Diese Funktion wurde für Microsoft Dynamics 365 for Operations (1611) erweitert und ermöglicht Ihnen, Ladungsadressen für eine innergemeinschaftliche Transaktion anzugeben. Wenn eine Ladungsadresse sich von einer Kreditoren-Geschäftsadresse unterscheidet (oder Debitoren-Geschäftsadresse für Rücklieferung) funktioniert der Intrastat-Bericht mit diesen Informationen. Wenn Sie einen Auftrag, eine Freitextrechnung, eine Bestellung, eine Kreditorenrechnung, Projektrechnung oder einen Umlagerungsauftrag erstellen, besitzen einige Felder, die für Außenhandel zugeordnet sind, Standardwerte im Dokumentkopf oder in der Position. Der standardmäßige Buchungscode wird aus dem entsprechenden Feld auf der Seite **Außenhandelsparameter** entnommen. Der standardmäßige Warencode, Ursprungsland/-region und Bundesland/Kanton des Ursprungs werden dem Artikel selbst übernommen. Sie können die Standardwerte ändern und können auch andere außenhandelsbezogene Informationen ausfüllen: Statistiken-Verfahren, Transportmethode und Port.

### <a name="use-the-intrastat-journal-to-generate-information-about-trade-among-eu-countriesregions"></a>Mithilfe der Intrastat-Erfassung können Sie Informationen zum Handel zwischen EU-Ländern/Regionen generieren und melden

Zu statistischen Zwecken generieren Sie Informationen zum Handel zwischen EU-Ländern/Regionen jeden Monat. Sie können Buchungen übertragen aus einer Freitextrechnung, einer Debitorenrechnung, einem Debitorenlieferschein, einer Kreditorenrechnung, einem Lieferschein des Kreditors, einer Projektrechnung oder aus einem Umlagerungsauftrag, entsprechend den Übertragungskriterien, die auf der Seite **Außenhandelsparameter** eingerichtet werden. Ersatzweise können Sie Transaktionen manuell eingeben. Sie können übertragene Buchungen in der Intrastat-Erfassung manuell aktualisieren, wenn derzeit Aktualisierungen erforderlich sind. Unter bestimmten Bedingungen, die auf der Seite **Komprimierung von Intrastat** eingerichtet werden, können Sie die Buchungen in der Intrastat-Erfassung komprimieren. In einigen Ländern/Regionen können Sie einen kleinen Buchungsschwellenwert übernehmen. Sie können dann Buchungen melden, die unter dem Schwellenwert unter dem angegebenen Warencode sind. Sie können den Warencode in den entsprechenden Intrastat-Erfassungspositionen aktualisieren, basierend auf der Einstellung **Untergrenze** auf der Seite **Außenhandelsparameter**. Sie können diese Buchungen auch komprimieren, basierend auf den Einstellungen auch **Komprimierung von Intrastat**. Sie können die Vollständigkeit der Buchungen in der Intrastat-Erfassung überprüfen, basierend auf der Einstellung **Einstellungen prüfen** auf der Seite **Außenhandelsparameter**. Die Daten in den entsprechenden Feldern werden auf Vollständigkeit geprüft möglicherweise: Land/Region, Bundesland oder Kanton., Gewicht, Warencode, Buchungscode, zusätzliche Einheit, Port, Buchungsgrundlage, Lieferbedingungen, Transportmethode und Steuernummer. Buchungen, die nicht abgeschlossen sind, werden markiert als ungültig.

### <a name="use-the-intrastat-journal-to-report-information-about-trade-among-eu-countriesregions"></a>Mithilfe der Intrastat-Erfassung können Sie Informationen zum Handel zwischen EU-Ländern/Regionen melden

Zu statistischen Zwecken melden Sie Informationen zum Handel zwischen EU-Ländern/Regionen jeden Monat. Sie können den Intrastat-Bericht, basierend auf den Einstellungen **Berichtsformatzuordnung** drucken auf der **Außenhandelsparameter** Seite. Sie können auch eine elektronische Datei generieren, basierend auf den Einstellungen **Dateiformatzuordnung** auf der **Außenhandelsparameter** Seite. Siehe auch die zusammenfassende Meldungs-Berichterstellungs-Wiki-Seite für weitere Informationen zu zusammenfassenden Meldungen, einschließlich der erforderlichen Komponenten.

  - Generieren Sie eine EU-Intrastat-Meldung
  - Übertragen Sie Transaktionen an den Intrastat
  - Angeben der Ladungsadresse für eine Innergemeinschaftliche Buchung.

## <a name="prerequisites"></a>Voraussetzungen
In der folgenden Tabelle werden die Komponenten für Intrastat-Berichte angezeigt.

|  Voraussetzung  |  Beschreibung  |
|-------------------------|-------------------------|
| Adresseinstellungen | Codes der Internationalen Organisation für Normung (ISO) für Länder/Regionen. |
| Juristische Person | Einrichten von Umsatzsteuer-ID-Nummern für den Import/Exportieren, die Fillialnummer-Erweiterung für den Import/Export und den Intrastat-Code, der der juristischen Person zugeordnet wird. |
| Hierarchie der Produktkategorie (Vertriebshierarchie, Beschaffungshierarchie) | Weisen Sie die Intrastat-Warencodes den Kategorieknoten auf der Registerkarte **Warencodes** der Seite **Kategoriehierarchie** zu. Wenn Sie einen Warencode einem Knoten der übergeordneten Kategorie zuweisen, ist dieser Code auf alle Knoten der untergeordneten Kategorie anwendbar. Die ausgewählten Warencodes sind in der Ansicht **Ausgewählt** verfügbar, wenn Sie einen Warencode in den Details für Produkte und in Aufträgen, Bestellungen und Umlagerungsauftragspositionen auswählen. |
| Details für freigegebene Produkte | Richten Sie die folgenden Außenhandelsdaten für freigegebene Produkte ein:<ul><li>**Warencode** - Wählen Sie entweder aus der Liste der ausgewählten Waren aus, die von zugewiesenen Produktkategorien oder von der vollständigen Liste von Intrastat-Warencodes abgerufen wird.</li><li>**Statistischer Prozentsatz der Belastungen**</li><li>**Herkunftsland/-region** - Wählen Sie das Standardland /-region aus, in dem die Waren vollständig erhalten oder produziert wurden.</li><li>**Bundesland/Kanton für Ursprung/Ziel** - Wählen Sie das Standardbundesland/den Kanton des Ziels für Eingänge sowie das Ursprungsbundesland/den Kanton für den Versand aus.</li><li>**Nettogewicht in kg**</li><li>**Ausschließen** – Aktivieren Sie diesen Parameter, um Transaktionen mit diesem Produkt nicht an Intrastat zu übertragen</li></ul> |
| Kunden | Richten Sie die Lieferadresse des Debitors im EU-Land/der EU-Region ein. |
| Lieferanten | Richten Sie die Händleradresse im EU-Land/der EU-Region ein. |
| Sonstige Zuschläge | Richten Sie den Code für sonstige Zuschläge ein, der in den Rechnungsbetrag, im statistischen Betrag oder in beide einbezogen werden soll. Aktivieren Sie auf der Seite **Codes für Belastungen** auf der Registerkarte **Außenhandel** die Option **Intrastat-Rechnungswert**, um den Betrag der Zuschläge im Rechnungswert einzubeziehen, und aktivieren Sie **Intrastat-Statistikwert**, um den Betrag der Zuschläge im statistischen Wert einzubeziehen.</br>Weitere Informationen finden Sie unter dem [Transaktionscodes und sonstige Belastungen](#transaction-codes-and-miscellaneous-charges)-Beispiel. |
| Elektronische Berichterstellung | Einrichten von Konfigurationen zur elektronischen Berichterstellung, um Intrastat-Daten in einer elektronischen Datei zu exportieren, die das Format hat, das von den zuständigen Behörden angefordert wird, und um Intrastat-Daten in einem benutzerfreundlichen, lesbaren Format in der Vorschau anzuzeigen (beispielsweise in Microsoft Excel). |
| Lagerort | Zuordnen von Kreditorenkonten mit Lagerortcodes für das Ausfüllen der Steuernummer, wenn ein Umlagerungsauftrags übertragen wird.</br>Weitere Informationen finden Sie unter dem [Überweisungsauftrag](#transfer-order)-Beispiel.|

## <a name="setup"></a>Einrichtung
In den folgenden Abschnitten werden die Einstellungen beschrieben, die für Intrastat-Berichte erforderlich sind.

### <a name="set-up-all-required-intrastat-related-lists"></a>Einrichten aller erforderlichen Intrastat-zugeordneten Listen

|   Liste   |   Weitere Informationen   |
|-------------------------|-------------------------|
| Warencodes | Richten Sie eine Kategoriehierarchie vom Typ **Warencode** ein, und geben Sie alle Warencodes gemäß der Liste der kombinierten Nomenklatur ein. Für jede Ware richten Sie die folgenden Informationen ein:<ul><li>Der Name der Ware und der Warencode</li><li>Der Anzeigename und/oder übersetzte Name</li><li>Einstellungen für das Melden von zusätzlichen (ergänzenden) Einheiten auf der **Außenhandel** Registerkarte. Sie können zusätzlich die Einheit in der Einheitsliste auswählen. Sie können auch angeben, ob das Gewicht von Waren zusätzlich zur ausgewählten zusätzlichen Einheit angegeben werden muss.</li></ul>Weitere Informationen finden Sie unter dem [Zusätzliche Einheiten](#additional-units)-Beispiel.|
| Art des Geschäftes | Richten Sie die Art der Transaktion gemäß den Anforderungen Ihres Landes/Ihrer Region ein. Für jeden Buchungscode, den Sie einrichten, müssen Sie die Regeln für die Berechnung der Rechnungsbeträge und von statistischen Beträgen für Umlagerungsaufträge und Verkauf/Bestellungen einrichten.<ul><li>Für Umlagerungsaufträge richten Sie eine der folgenden Regeln für die Berechnung der Rechnungsbeträge und statistischen Beträgen ein:<ul><li>**Leer** – Der Betrag ist 0 (Null).</li><li>**Wertmäßiger Einstandsbetrag** – Der Betrag entspricht dem wertmäßigen Einstandsbetrag.</li><li>**Gesamtkosten** – Der Betrag entspricht die Gesamtkosten der Buchung.</li><li>**Manuell** – Der Betrag entspricht dem Betrag, der manuell auf der Umlagerungsauftragsposition angegeben ist.</li></ul></li><li>Für Aufträge und Bestellungen richten Sie eine der folgenden Regeln für die Berechnung der Rechnungsbeträge und statistischen Beträgen ein:<ul><li>**Leer** – Der Betrag ist 0 (Null).</li><li>**Rechnungsbetrag** - Der Betrag entspricht dem Betrag, der für die Ware in Rechnung gestellt wird.</li><li>**Grundbetrag** - Der Betrag entspricht dem Betrag, der gestellt werden, bevor einer beliebigen Rabatt angewendet wird.</li></ul></ul>Weitere Informationen finden Sie unter dem [Transaktionscodes und sonstige Belastungen](#transaction-codes-and-miscellaneous-charges)-Beispiel. |
| Transportmethoden | Richten Sie den Transportmodus gemäß den Anforderungen Ihres Landes/Ihrer Region ein. Für jede Lieferart können Sie eine standardmäßige Transportmethode auf der Registerkarte **Außenhandel** einrichten. |
| Ports | Richten Sie den Hafen/Flughafen des Ladens/Entladens ein, wenn diese Informationen von Ihrem Land/Ihrer Region erfasst werden. |
| Statistikverfahren | Richten Sie die Statistikverfahren ein, wenn diese Informationen von Ihrem Land/Ihrer Region erfasst werden. |



### <a name="set-up-rules-for-compressing-intrastat-transactions"></a>Einrichten von Regeln zur Komprimierung von Intrastat-Transaktionen

Auf der **Komprimierung von Intrastat** Seite können Sie die Felder festlegen, die für die Komprimierung zu verwenden. Alle Buchungen, die eine identische Kombination von Werten für die ausgewählten Felder in der Intrastat-Erfassung haben, werden in eine einzige Buchung komprimiert, wenn Sie die Komprimierungsfunktion in der Intrastat-Erfassung ausführen.

### <a name="set-up-foreign-trade-parameters"></a>Außenhandelsparameter einrichten

Verwenden Sie die **Außenhandelsparameter** Seite, um die Parameter in der folgenden Tabelle einzurichten.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Registerkarte</th>
<th>Parameter</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Allgemeines</td>
<td><ul>
<li><strong>Allgemein</strong> – Geben Sie die folgenden Informationen ein:
<ul>
<li>Die Standardtransaktionscodes für Aufträge, Bestellungen, Gutschriften und Umlagerungsaufträge. Der Buchungscode, der für Gutschriften eingerichtet wurde, wird auch als Code für die Rückgabe physischer Waren und zur Ermittlung der Abweichung von physischer Rückgaben gegenüber Korrekturgutschriften verwendet. Retouren physischer Waren werden in der Intrastat-Umlagerung mit einer anderen Richtung gemeldet. Die Rückgabe des Zugangs wird als Versand und die Rückgabe des Versands als Zugang gemeldet.</li>
<li>Der Mitarbeiter, der für die Vorbereitung von Intrastat-Berichten zuständig ist.</li>
</ul></li>
<li><strong>Untergrenze</strong> - Geben Sie die Einstellungen für die Aktualisierung von Buchungen an, die unter dem Schwellenwert sind:
<ul>
<li>Der Schwellenbetrag und das Gewicht</li>
<li>Der Warencode, der auf Buchungen angewendet werden soll, die unter dem Schwellenwert sind</li>
</ul></li>
<li><strong>Übertragen</strong> - Geben Sie die Kriterien für die Übertragung von Buchungen zur Intrastat-Erfassung an. Sie können angeben, dass Posten gebucht werden, wenn die Artikel eine oder alle der folgenden Kriterien erfüllen:
<ul>
<li>Die Artikel sind keine Dienstleistungsartikel.</li>
<li>Die Artikel haben einen Warencode.</li>
<li>Die Artikel werden ein Gewicht.</li>
<li>Die Artikel haben besonderer Maßeinheiten.</li>
</ul></li>
<li><strong>Einstellungen prüfen</strong> - Geben Sie die Regeln für die Überprüfung der Vollständigkeit von Intrastat-Daten an. Sie können auswählen, welche Daten geprüft werden.</li>
<li><strong>Rundungsregeln</strong> - Geben Sie die folgenden Einstellungen für Rundungsbeträge und Gewichten im Intrastat-Bericht an:
<ul>
<li>Die Rundungsregel (Genauigkeit)</li>
<li>Die Rundungsmethode: aufrunden, abrunden oder normal</li>
<li>Die Anzahl von Dezimalstellen für Beträge und Gewichten</li>
<li>Anweisungen für das Runden von Gewichtungen, die kleiner als 1 Kilogramm (kg) sind: bis 1 kg, normal oder keine Rundung</li>
</ul></li>
<li><strong>Elektronische Berichterstellung</strong> - Geben Sie Referenzen auf elektronische Berichterstellungskonfigurationen an, mit denen Sie eine Datei und einen Bericht generieren können.</li>
<li><strong>Warencodehierarchie</strong> - Geben Sie die Kategoriehierarchie vom <strong>Warencode</strong>-Typ an, der den Intrastat-Warencode CN8 darstellt.</li>
  <li> <strong>Wechselkurstyp</strong> - Geben Sie optional einen Wechselkurs an, der für die Meldung von Intrastat-Verkäufen und -Einkäufen in Fremdwährung verwendet werden soll. Dieser wird verwendet, wenn der Kurs von demjenigen abweicht, der beim Buchen der Transaktion verwendet wird.</li>  
</ul></td>
</tr>
<tr class="even">
<td>Kontaktinformationen des Beauftragten</td>
<td>Geben Sie den Namen, die Adresse, Umsatzsteuernummer, Telefonnummer und Faxnummer des Agenten an.</td>
</tr>
<tr class="odd">
<td>Länder-/Regionseigenschaften</td>
<td>Legen Sie das Land/die Region der aktuellen juristischen Person auf <strong>Inland</strong> fest. Festlegen des Lands oder einer Region aus EU-Ländern/Regionen, die am EU-Handel mit der aktuellen juristischen Person mit <strong>EU</strong> teilnehmen. Für jedes Land/Region kennzeichnen Sie auch Länder-/Regionscode zu den Außenhandelzwecken.</td>
</tr>
<tr class="even">
<td>Nummernkreis</td>
<td>Geben Sie hier den Kennungscode für die Intrastat-Erfassung an.</td>
</tr>
</tbody>
</table>

## <a name="example"></a>Beispiel

### <a name="transaction-codes-and-miscellaneous-charges"></a><a name= "transaction-codes-and-miscellaneous-charges"></a>Transaktionscodes und sonstige Belastungen

Dieser Artikel behandelt ein Szenario, in dem ein Unternehmen in Deutschland Waren von einem Unternehmen in Italien kaufen muss. Um diesen Kauf zu tätigen, muss das deutsche Unternehmen neue Transaktionscodes einrichten und Berechnungsregeln für den Rechnungsbetrag und den statistischen Betrag für diese Transaktionscodes konfigurieren. Wenn das Unternehmen eine Rechnung erstellt, muss es außerdem sonstige Belastungen und deren Prozentsätze angeben. Diese Werte werden bei der Berechnung des statistischen Wertes berücksichtigt.

Dieses Szenario verwendet die juristische Person **DEMF**.

#### <a name="preliminary-setup"></a>Vorläufige Einstellungen

1. Gehen Sie zu **Organisationsverwaltung** > **Organisation** > **Juristische Entitäten**, und wählen Sie **DEMF**.
2. Bestätigen Sie auf dem Inforegister **Adressen**, dass das Feld **Land/Region** auf **DEU(Deutschland)** festgelegt ist.
3. Gehen Sie zu **Kreditorenkonten** > **Kreditoren** > **Alle Kreditoren** aus.
4. Wählen Sie im Raster **DE-001** aus.
5. Wählen Sie auf der Inforegisterkarte **Adresse** die Option **Bearbeiten**.
6. Wählen Sie im Dialogfeld **Adresse bearbeiten** im Feld **Land/Region** die Option **ITA**.
7. Klicken Sie auf **OK**, um das Dialogfeld zu schließen.

#### <a name="set-up-transaction-codes"></a>Buchungscodes einrichten

1. Wechseln Sie zu **Steuer** > **Einstellungen** > **Außenhandel** > **Art des Geschäfts**.
2. Wählen Sie im Raster **11** aus. Wählen Sie dann im Aktivitätsbereich **Löschen** aus.
3. Wählen Sie im Aktivitätsbereich **Neu** aus.
4. Geben Sie auf dem **Transaktionscodes**-Inforegister im **Transaktionscode**-Feld **11** ein.
5. Geben Sie im Feld **Name** **Direkter Kauf/Verkauf** ein.
6. Wählen Sie im **Verkäufe und Einkäufe**-Abschnitt im **Rechnungsbetrag**-Feld **Rechnungsbetrag** aus.
7. Wählen Sie im Feld **Statistikbetrag** **Rechnungsbetrag** aus.
8. Wählen Sie im Aktionsbereich **Speichern** aus.

#### <a name="set-up-miscellaneous-charges"></a>Einrichten von sonstigen Gebüren

1. Wechseln Sie zu **Debitoren** > **Belastungseinstellungen** > **Belastungscode**.
2. Wählen Sie im Raster **Fracht** aus.
3. Wählen Sie im Aktionsbereich **Bearbeiten** aus.
4. Legen Sie im Inforegister **Außenhandel** die Optionen **Intrastat-Rechnungswert** und **Statistischer Intrastat-Wert** auf **Ja** fest.

#### <a name="set-up-foreign-trade-parameters"></a>Außenhandelsparameter einrichten

1. Gehen Sie zu **Steuer** > **Einstellungen** > **Außenhandel** > **Außenhandelsparameter**.
2. Auf der Registerkarte **Intrastat** wählen Sie auf dem Inforegister **Allgemein** im Feld **Art** **des Geschäfts** **11** aus.
3. Stellen Sie sicher, dass Sie im Inforegister **Warencodehierarchie** im Feld **Kategoriehierarchie** **Intrastat** ausgewählt ist.

#### <a name="create-a-purchase-order"></a>Eine Bestellung erstellen

1. Gehen Sie zu **Kreditoren** > **Bestellungen** > **Alle Bestellungen**.
2. Wählen Sie im Aktivitätsbereich **Neu** aus.
3. Wählen Sie im Dialogfeld **Bestellung erstellen** im Feld **Kreditorenkonto** **DE-001**.
4. Wählen Sie **OK** aus.
5. Stellen Sie auf der Registerkarte **Kopfzeile** im Inforegister **Ausland** **Transaktion** sicher, dass das Feld **Transaktionscode** auf **11** festgelegt ist.
6. Wählen Sie auf der Registerkarte **Zeilen** auf dem Inforegister **Bestellzeilen** im Feld **Positionsnummer** den Wert **D0003**. Geben Sie dann im Feld **Menge** den Wert **10** ein.
7. Stellen Sie im Inforegister **Zeilendetails** auf der Registerkarte **Außenhandel** im Abschnitt **Außenhandel** sicher, dass das Feld **Transaktionscode** automatisch festgelegt wird.
8. Wählen Sie im Inforegister **Bestellpositionen** im Menü **Finanzen** im **Belastungen**-Abschnitt **Belastungen beibehalten** aus.
9. Wählen Sie im Feld **Belastungscode** **FRACHT** aus.
10. Geben Sie im Feld **Belastungswert** **30** ein.
11. Wählen Sie im Aktionsbereich **Speichern** aus. Schließen Sie nun die Seite.
12. Wählen Sie im Aktionsbereich, auf der Registerkarte **Kauf**, in der Gruppe **Aktionen** den Eintrag **Bestätigen**.
13. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Rechnung** in der Gruppe **Generieren** **Rechnung** aus.
14. Wählen Sie im Aktionsbereich **Standard von**. Wählen Sie im Feld **Vorgabe Menge für Zeilen** die Option **Bestellte Menge**. Wählen Sie dann **OK** aus.
15. Auf dem Inforegister **Kreditor Rechnungskopf**, im Abschnitt **Rechnungsidentifikation**, im Feld **Nummer** geben Sie **00100** ein.
16. Wählen Sie im Abschnitt **Rechnungsdaten** im Feld **Rechnungsdatum** den Wert **24/11/2021** (24. November 2021).
17. Wählen Sie im Aktionsbereich **Buchen**, um die Rechnung zu buchen.

### <a name="transfer-the-vendor-invoice-to-the-intrastat-journal"></a>Die Kreditorenrechnung in das Intrastat-Journal übertragen

1. Wechseln Sie zu **Steuer** > **Meldungen** > **Außenhandel** > **Intrastat**.
2. Wählen Sie im Aktivitätsbereich **Übertragung**.
3. Legen Sie im Dialogfeld **Intrastat (Übertragung)** die Option **Kreditor-Rechnung** auf **Ja** fest.
4. Wählen Sie **OK**, um die Transaktionen zu übertragen, und überprüfen Sie das Intrastat-Buch.-Blatt.

   ![Position, die die Bestellung mit sonstigen Belastungen auf der Intrastat-Seite darstellt](media/intrastat_overview_1.png)

5. Überprüfen Sie die Registerkarte **Allgemein** für die Bestellung. Beachten Sie, dass das Feld **Rechnungswert** die Summe der Felder **Rechnungsbetrag** und **Rechnungsbetrag** zeigt und dass das Feld **Statistischer Wert** die Summe der Felder **Statistische Menge** und **Höhe der statistischen Belastungen** zeigt.

   ![Bestellungsdetails mit sonstigen Belastungen auf der Registerkarte „Allgemein“ der Intrastat-Seite](media/intrastat_overview_2.png)

### <a name="transfer-order"></a>Umlagerungsauftrag

In diesem Beispiel muss ein Unternehmen in Deutschland zwei Wareneinheiten von einem Lager in Deutschland zu einem Lager in Italien transportieren. Auch für dieses Produkt sind Belastungen in Höhe von 20 Prozent für die Abrechnung in der im Feld **Statistischer Wert** anzugeben. Dieses Beispiel verwendet die juristische Entität **DEMF**.

#### <a name="preliminary-setup"></a>Vorläufige Einstellungen

1. Gehen Sie zu **Organisationsverwaltung** > **Organisation** > **Juristische Entitäten**, und wählen Sie **DEMF**.
2. Bestätigen Sie auf dem Inforegister **Adressen**, dass das Feld **Land/Region** auf **DEU(Deutschland)** festgelegt ist.
3. Gehen Sie zu **Steuer** > **Einstellungen** > **Außenhandel** > **Außenhandelsparameter**.
4. Stellen Sie sicher, dass Sie im Inforegister **Warencodehierarchie** im Feld **Kategoriehierarchie** **Intrastat** ausgewählt ist.
5. Gehen Sie zu **Kreditorenkonten** > **Kreditoren** > **Alle Kreditoren** aus.
6. Wählen Sie im Raster **DE-001** aus.
7. Wählen Sie auf der Inforegisterkarte **Adresse** die Option **Bearbeiten**.
8. Wählen Sie im Dialogfeld **Adresse bearbeiten** im Feld **Land/Region** die Option **ITA**.
9. Klicken Sie auf **OK**, um das Dialogfeld zu schließen.

#### <a name="set-up-transaction-codes"></a>Buchungscodes einrichten

1. Wechseln Sie zu **Steuer** > **Einstellungen** > **Außenhandel** > **Art des Geschäfts**.
2. Wählen Sie im Raster **11** aus. Wählen Sie dann im Aktivitätsbereich **Löschen** aus.
3. Wählen Sie im Aktivitätsbereich **Neu** aus.
4. Geben Sie auf dem **Transaktionscodes**-Inforegister im **Transaktionscode**-Feld **11** ein.
5. Geben Sie im Feld **Name** **Direkter Kauf/Verkauf** ein.
6. Wählen Sie im **Umlagerungsauftrag**-Abschnitt im Feld **Rechnungsbetrag** **Gesamtkosten** aus.
7. Wählen Sie im Feld **Statistikbetrag** die Option **Gesamtkosten** aus.
8. Wählen Sie im Aktionsbereich **Speichern** aus.
9. Gehen Sie zu **Steuer** > **Einstellungen** > **Außenhandel** > **Außenhandelsparameter**.
10. Auf der **Intrastat**-Registerkarte, auf dem Inforegister **Allgemein** im **Umlagerungsauftrag**-Feld, wählen Sie **11** aus.

#### <a name="set-up-charges-for-an-item"></a>Einrichten von Gebüren für einen Artikel

1. Wechseln Sie zu **Produktinformationsverwaltung** > **Produkte** > **Freigegebene Produkte** aus.
2. Wählen Sie im Raster **D0001** aus.
3. Geben Sie im Inforegister **Außenhandel** im Abschnitt **Intrastat** im Feld **Belastungsanteil** **20** ein.

#### <a name="change-the-site-address"></a>Ändern Sie die Standortadresse

1. Gehen Sie zu **Lagerortverwaltung** > **Einrichtung** > **Lager** > **Standorte**.
2. Wählen Sie im Raster **1** aus.
3. Wählen Sie auf der Inforegisterkarte **Adressen** die Option **Bearbeiten**.
4. Wählen Sie im Dialogfeld **Adresse bearbeiten** im Feld **Land/Region** die Option **DEU**.
5. Wählen Sie **OK** aus.
6. Wählen Sie im Raster **2** aus.
7. Wählen Sie auf der Inforegisterkarte **Adressen** die Option **Bearbeiten**.
8. Wählen Sie im Dialogfeld **Adresse bearbeiten** im Feld **Land/Region** die Option **ITA**.
9. Wählen Sie **OK** aus.
10. Navigieren Sie zu **Lagerortverwaltung** > **Einstellungen** > **Lagerort** > **Lagerorte**.
11. Wählen Sie im Raster **21** aus.
12. Wählen Sie im Inforegister **Allgemein** im Abschnitt **Referenz** im Feld **Kreditorenkonto** **DE-001** aus.

#### <a name="create-a-transfer-order"></a>Erstellen eines Umlagerungsauftrags

1. Navigieren Sie zu **Lagerverwaltung** > **Ausgehende Aufträge** > **Umlagerungsauftrag**.
2. Wählen Sie im Aktivitätsbereich **Neu** aus.
3. Wählen Sie in der Registerkarte **Positionen** im Inforegister **Kopf des Umlagerungsauftrags** im **Überblick**-Abschnitt im **Ab Lager**-Feld **11** aus. Im Feld **An Lagerort** wählen Sie **21** aus.
4. Wählen Sie in der **Positionen**-Registerkarte auf dem **Umbuchungsauftragspositionen**-Inforegister **Hinzufügen** aus.
5. Wählen Sie im Feld **Artikelnummer** die Option **D0001** aus. Geben Sie dann im Feld **Umlagerungsmenge** den Wert **2** ein.
6. Stellen Sie im Inforegister **Zeilendetails** auf der Registerkarte **Außenhandel** im Abschnitt **Außenhandel** sicher, dass das Feld **Transaktionscode** automatisch festgelegt wird.
7. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Versenden** in der Gruppe **Operations** die Option **Umlagerungsauftrag versenden** aus.
8. Wählen Sie im Dialogfeld **Lieferung** auf der **Überblick**-Registerkarte im **Aktualisieren**-Feld **Alle** aus.
9. Wählen Sie **OK** aus, um den Auftrag zu versenden.
10. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Empfangen** in der Gruppe **Operations** auf **Empfangen**.
11. Wählen Sie im Dialogfeld **Empfangen** auf der **Überblick**-Registerkarte im **Aktualisieren**-Feld **Alle** aus.
12. Wählen Sie **OK** aus, um den Auftrag zu versenden.

#### <a name="transfer-the-transfer-order-to-the-intrastat-journal"></a>Den Umlagerungsauftrag in das Intrastat-Journal übertragen

1. Wechseln Sie zu **Steuer** > **Meldungen** > **Außenhandel** > **Intrastat**.
2. Wählen Sie im Aktivitätsbereich **Übertragung**.
3. Legen Sie im **Intrastat (Umlagerung)**-Dialogfeld die **Umlagerungsauftrag**-Option auf **Ja** und alle anderen Optionen auf **Nein** fest.
4. Wählen Sie **OK**, um die Transaktionen zu übertragen, und überprüfen Sie das Intrastat-Buch.-Blatt.

   ![Position, die die Umlagerung auf der Intrastat-Seite darstellt](media/intrastat_overview_3.png)

5.  Überprüfen Sie die Registerkarte **Allgemein** für die Umlagerung.

    Beachten Sie, dass die Felder in den Abschnitten **Rechnungswert** und **Statistischer Wert** automatisch festgelegt werden. Die Werte der Felder **Rechnungsbetrag** und **Statistische Menge** basieren auf Einstellungen auf der **Transaktionscodes**-Seite. Der Wert **20** in dem **Belastungsanteil**-Feld ist der Wert, der für die **Freigegebenes Produkt**-Seite festgelegt wird. Der Wert in der **Statistikbelastungsbetrag**-Feld ist ein quantitativer Ausdruck der Belastungen (weil 107,24 20 Prozent von 536,18 entspricht). Der Wert des **Statistischer Wert**-Felds ist die Summe der Werte aus den Feldern **Statistische Menge** und **Statistikbelastungsbetrag**.

  ![Umlagerungsauftragsdetails auf der Registerkarte „Allgemein“ der Intrastat-Seite](media/intrastat_overview_4.png)

### <a name="additional-units"></a>Besondere Maßeinheit

In diesem Beispiel muss ein Unternehmen in Deutschland 10 Wareneinheiten von einem Unternehmen in Italien kaufen. Zusätzlich zu den Warencodes müssen für diese Waren zusätzliche Einheiten angegeben werden. Das Beispiel zeigt, wie Sie neue Maßeinheiten erstellen, der Intrastat-Warennummer zusätzliche Einheiten zuweisen, Transaktionen mit zusätzlichen Einheiten buchen und das Intrastat-Journal überprüfen, in dem das Feld für die zusätzlichen Einheiten festgelegt ist.

#### <a name="preliminary-setup"></a>Vorläufige Einstellungen

1. Gehen Sie zu **Organisationsverwaltung** > **Organisation** > **Juristische Entitäten**, und wählen Sie **DEMF**.
2. Bestätigen Sie auf dem Inforegister **Adressen**, dass das Feld **Land/Region** auf **DEU(Deutschland)** festgelegt ist.
3. Gehen Sie zu **Steuer** > **Einstellungen** > **Außenhandel** > **Außenhandelsparameter**.
4. Auf der Registerkarte **Intrastat** wählen Sie auf dem Inforegister **Allgemein** im Feld **Art** **des Geschäfts** **11** aus.
5. Stellen Sie sicher, dass Sie im Inforegister **Warencodehierarchie** im Feld **Kategoriehierarchie** **Intrastat** ausgewählt ist.
6. Gehen Sie zu **Kreditorenkonten** > **Kreditoren** > **Alle Kreditoren** aus.
7. Wählen Sie im Raster **DE-001** aus.
8. Wählen Sie auf der Inforegisterkarte **Adresse** die Option **Bearbeiten**.
9. Wählen Sie im Dialogfeld **Adresse bearbeiten** im Feld **Land/Region** die Option **ITA**.
10. Klicken Sie auf **OK**, um das Dialogfeld zu schließen.

#### <a name="create-a-unit-of-measure"></a>Erstellen Sie eine Maßeinheit.

1. Gehen Sie zu **Organisationsverwaltung** > **Einstellen** > **Einheiten** > **Einheiten**.
2. Wählen Sie im Aktivitätsbereich **Neu** aus.
3. Wählen Sie im Feld **Einheit** aus, geben Sie einen Namen für die Maßeinheit ein. Geben Sie für dieses Beispiel **GRM** ein.
4. Wählen Sie auf dem Inforegister **Allgemein** im **Klassifizierung**-Abschnitt im **Einheitsklasse**-Feld die Eigenschaft aus, die die Einheit misst. Wählen Sie für dieses Beispiel **Masse** aus.
5. Im **Einheitensystem** wählen Sie das Maßsystem aus, zu dem die Einheit gehört. Wählen Sie zum Beispiel **Metrische Einheiten** aus.

#### <a name="set-up-unit-conversions"></a>Einheitenkonvertierungen einrichten

1. Gehen Sie zu **Organisationsverwaltung** > **Einstellen** > **Einheiten** > **Einheitenkonvertierungen**.
2. Wählen Sie auf der **Konvertierungen zwischen Klassen**-Registerkarte **Neu** aus.
3. Wählen Sie in dem Dialogfeld **Einheitskonvertierung** im Feld **Produkt** **F00007** aus.
4. Wählen Sie im Feld **Aus Einheit** die Option **ea** aus.
5. Wählen Sie im Feld **In Einheit** die Option **GRM** aus.
6. Überprüfen Sie, ob die Konvertierungsrate **1 = 1** ist.
7. Wählen Sie **OK** aus.
8. Wechseln Sie zu **Produktinformationsverwaltung** > **Produkte** > **Freigegebene Produkte** aus.
9. Wählen Sie im Raster **F00007** aus.
10. Wählen Sie im Inforegister **Lagerbestand verwalten** im Abschnitt **Bestand** im Feld **Einheit** **GRM** aus.
11. Wählen Sie im Aktionsbereich **Speichern** aus.

#### <a name="set-up-product-information"></a>Produktinformation festlegen

1. Wechseln Sie zu **Produktinformationsverwaltung** > **Produkte** > **Freigegebene Produkte** aus.
2. Wählen Sie im Raster **F00007** aus.
3. Auf dem Inforegister **Außenhandel** wählen Sie im Abschnitt **Intrastat** im Feld **Ware** **920 20 34** aus.
4. Wählen Sie im Aktionsbereich **Speichern** aus.

#### <a name="assign-the-additional-unit-to-an-intrastate-commodity-code"></a>Die Zusatzeinheit einem Intrastat-Warennummer zuordnen

1. Gehen Sie zu **Produktinformationsmanagement** > **Einrichtung** > **Kategorien und Attribute** > **Kategorie-Hierarchien**.
2. Wählen Sie in der Liste **Intrastat** aus.
3. Wählen Sie im Raster **Sprecher** aus.
4. Wählen Sie auf dem Inforegister **Außenhandel** im Feld **Zusatzeinheiten** die Option **GRM** aus.
5. Wählen Sie im Aktionsbereich **Speichern** aus.

   Weitere Informationen finden Sie unter [Maßeinheiten verwalten](../../supply-chain/pim/tasks/manage-unit-measure.md).

#### <a name="create-a-purchase-order"></a>Eine Bestellung erstellen

1. Gehen Sie zu **Kreditoren** > **Bestellungen** > **Alle Bestellungen**.
2. Wählen Sie im Aktivitätsbereich **Neu** aus.
3. Wählen Sie im Dialogfeld **Bestellung erstellen** im Feld **Kreditorenkonto** **DE-001**.
4. Wählen Sie **OK** aus.
5. Stellen Sie auf der Registerkarte **Kopfzeile** im Inforegister **Ausland** **Transaktion** sicher, dass das Feld **Transaktionscode** auf **11** festgelegt ist.
6. Wählen Sie auf der Registerkarte **Zeilen** auf dem Inforegister **Bestellzeilen** im Feld **Positionsnummer** den Wert **F00007**. Geben Sie dann im Feld **Menge** den Wert **10** ein.
7. Stellen Sie im Inforegister **Positionsdetails** auf der Registerkarte **Außenhandel** im Abschnitt **Außenhandel** sicher, dass die Felder **Transaktionscode** und **Ware** automatisch festgelegt werden.
8. Wählen Sie im Aktionsbereich, auf der Registerkarte **Kauf**, in der Gruppe **Aktionen** den Eintrag **Bestätigen**.
9. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Rechnung** in der Gruppe **Generieren** **Rechnung** aus.
10. Wählen Sie im Aktionsbereich **Standard von**. Wählen Sie im Feld **Vorgabe Menge für Zeilen** die Option **Bestellte Menge**. Wählen Sie dann **OK** aus.
11. Geben Sie auf dem Inforegister **Kreditorrechnungskopf** im Abschnitt **Rechnungsidentifikation** im Feld **Nummer** **VE-0010** ein.
12. Wählen Sie im Abschnitt **Rechnungsdaten** im Feld **Rechnungsdatum** den Wert **5/10/2021** (5. Oktober 2021).
13. Wählen Sie im Aktionsbereich **Buchen**, um die Rechnung zu buchen.

#### <a name="transfer-the-vendor-invoice-to-the-intrastat-journal"></a>Die Kreditorenrechnung in das Intrastat-Journal übertragen

1. Wechseln Sie zu **Steuer** > **Meldungen** > **Außenhandel** > **Intrastat**.
2. Wählen Sie im Aktivitätsbereich **Übertragung**.
3. Legen Sie im Dialogfeld **Intrastat (Übertragung)** die Option **Kreditor-Rechnung** auf **Ja** fest.
4. Wählen Sie **OK**, um die Transaktionen zu übertragen, und überprüfen Sie das Intrastat-Buch.-Blatt.

   ![Position, die die Bestellung auf der Intrastat-Seite darstellt](media/intrastat_overview_5.png)

5. Überprüfen Sie die Registerkarte **Allgemein** für die Bestellung. Beachten Sie, dass die Felder **Anzahl zusätzlicher Einheiten** und **Zusätzliche Einheit** im **Einheit**-Abschnitt automatisch festgelegt werden.

   ![Bestellungsdetails auf der Registerkarte „Allgemein“ der Intrastat-Seite](media/intrastat_overview_6.png)
   
## <a name="list-of-countryregion-specific-articles"></a>Liste länder-/regionsspezifischer Artikel
Die folgende Tabelle listet die verfügbaren länder-/regionsspezifischen Intrastat-Artikel auf.

| Land          | Verknüpfen      |
|------------------|-----------|
| Österreich          |[Intrastat (Österreich)](emea-aut-intrastat.md)| 
| Belgien          |[Intrastat (Belgien)](emea-bel-intrastat.md)|
| Tschechische Republik   |[Intrastat (Tschechische Republik)](emea-cze-intrastat.md)|
| Dänemark          |[Intrastat (Dänemark)](emea-dnk-intrastat.md)|
| Estland          |[Intrastat (Estland)](emea-est-intrastat.md)|
| Finnland          |[Intrastat (Finnland)](emea-fin-intrastat.md)|
| Frankreich           |[Französisch Intrastat](emea-fra-intrastat.md)|
| Deutschland          |[Deutsche Intrastat](emea-deu-intrastat.md)|
| Ungarn          |[Intrastat (Ungarn)](emea-hun-intrastat.md)|
| Italien            |[Italienische Intrastat](emea-ita-intrastat.md)|
| Lettland           |[Intrastat (Lettland)](emea-lva-intrastat.md)|
| Litauen        |[Intrastat (Litauen)](emea-ltu-intrastat.md)|
| Niederlande      |[Intrastat (Niederlande)](emea-nl-intrastat.md)|
| Polen           |[Intrastat (Polen)](emea-pol-intrastat.md)|
| Spanien            |[Intrastat (Spanien)](emea-esp-intrastat.md)|
| Schweden           |[Intrastat (Schweden)](emea-swe-intrastat.md)|


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
