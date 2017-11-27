---
title: Intrastat
description: "Dieser Artikel enthält Informationen zur Intrastat-Berichterstattung für den Warenhandel und in einigen Fällen Dienstleistungen unter Ländern/Regionen der Europäischen Union (EU). Er gibt einen Überblick über Berichterstellungsprozesses und beschreibt die erforderlichen Einstellungen und die Voraussetzungen."
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: Intrastat
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 28581
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 7c713f3a1cb5aa4758a72a7cc42c73c57b602219
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="intrastat"></a>Intrastat

[!include[banner](../includes/banner.md)]


Dieser Artikel enthält Informationen zur Intrastat-Berichterstattung für den Warenhandel und in einigen Fällen Dienstleistungen unter Ländern/Regionen der Europäischen Union (EU). Er gibt einen Überblick über Berichterstellungsprozesses und beschreibt die erforderlichen Einstellungen und die Voraussetzungen.

Intrastat ist das System für die Sammlung von Informationen und Generierung von statistischen Daten über den Warenhandel zwischen Ländern/Regionen der Europäischen Union (EU). Intrastat-Berichte werden benötigt, wenn ein Produkt die Grenze eines anderen EU-Landes/einer anderen Region überschreitet. In einigen Ländern/Regionen sind Intrastat-Berichte außerdem für Dienstleistungen nötig. Erforderliche und optionale Elemente können im Intrastat-Bericht erfasst werden. Die folgenden Elemente sind erforderlich: Die Umsatzsteuernummer (VAT ID) der Partei, die für die Bereitstellung der Informationen verantwortlich ist, der Referenzzeitraum, der Flow (Eingang oder Ausgang), der Warencode mit acht Ziffern, der Mitgliedsstaat des Partners (Mitgliedsstaat der Lieferung bei Eingang und Mitgliedsstaat des Ziels bei Ausgang), der Warenwert, die Warenmenge (Nettogewicht und zugehörige Einheit) sowie die Art der Transaktion. Länder/Regionen können auch optionale Elemente gemäß verschiedenen Bedingungen erfassen. Einige optionale Elemente sind Ursprungsland/-region, Lieferbedingungen, die Art des Transports, ein ausführlicherer Warencode als CN8, die Region des Ursprungs auf Dispositionen und die Region des Ziels auf Eingängen, das Statistikverfahren, der statistische Wert, einer Beschreibung der Waren und der Anschluss/der Flughafen des Ladens/Entladens.

## <a name="overview-of-the-intrastat-reporting-process"></a>Überblick des Intrastat-Berichterstellungsprozesses
Die folgenden Abschnitte beschreiben den allgemeinen Informationsfluss, der für Intrastat-Berichte verwendet wird.

### <a name="1-enter-a-transaction-that-crosses-the-border-of-another-eu-countryregion"></a>1. Geben Sie eine Buchung ein, welche die Grenze eines anderen EU-Landes/einer anderen Region überschreitet

Eine Debitorenrechnung, eine Freitextrechnung, eine Einkaufsrechnung, Projektrechnung, ein Debitorenlieferschein, ein Kreditorenproduktzugang oder Umlagerungsauftrag wird in die Intrastat-Erfassung übertragen, wenn die Länder-/Regionsart des Ziels (auf Dispositionen) oder Lieferung (auf Eingängen) ist **EU**. Diese Funktion wurde für Microsoft Dynamics 365 for Operations (1611) erweitert und gestattet, Ladungsadressen für eine Intragemeinschaftsbuchung anzugeben. Wenn eine Ladungsadresse sich von einer Kreditoren-Geschäftsadresse unterscheidet (oder Debitoren-Geschäftsadresse für Rücklieferung) funktioniert der Intrastat-Bericht mit diesen Informationen. Wenn Sie einen Auftrag, eine Freitextrechnung, eine Bestellung, eine Kreditorenrechnung, Projektrechnung oder einen Umlagerungsauftrag erstellen, besitzen einige Felder, die für Außenhandel zugeordnet sind, Standardwerte im Dokumentkopf oder in der Position. Der standardmäßige Buchungscode wird aus dem entsprechenden Feld auf der Seite **Außenhandelsparameter** entnommen. Der standardmäßige Warencode, Ursprungsland/-region und Bundesland/Kanton des Ursprungs werden dem Artikel selbst übernommen. Sie können die Standardwerte ändern und können auch andere außenhandelsbezogene Informationen ausfüllen: Statistiken-Verfahren, Transportmethode und Port.

### <a name="2-use-the-intrastat-journal-to-generate-information-about-trade-among-eu-countriesregions"></a>2. Mithilfe der Intrastat-Erfassung können Sie Informationen zum Handel zwischen EU-Ländern/Regionen generieren und melden

Zu statistischen Zwecken generieren Sie Informationen zum Handel zwischen EU-Ländern/Regionen jeden Monat. Sie können Buchungen übertragen aus einer Freitextrechnung, einer Debitorenrechnung, einem Debitorenlieferschein, einer Kreditorenrechnung, einem Lieferschein des Kreditors, einer Projektrechnung oder aus einem Umlagerungsauftrag, entsprechend den Übertragungskriterien, die auf der Seite **Außenhandelsparameter** eingerichtet werden. Ersatzweise können Sie Transaktionen manuell eingeben. Sie können übertragene Buchungen in der Intrastat-Erfassung manuell aktualisieren, wenn derzeit Aktualisierungen erforderlich sind. Unter bestimmten Bedingungen, die auf der Seite **Komprimierung von Intrastat** eingerichtet werden, können Sie die Buchungen in der Intrastat-Erfassung komprimieren. In einigen Ländern/Regionen können Sie einen kleinen Buchungsschwellenwert übernehmen. Sie können dann Buchungen melden, die unter dem Schwellenwert unter dem angegebenen Warencode sind. Sie können den Warencode in den entsprechenden Intrastat-Erfassungspositionen aktualisieren, basierend auf der Einstellung **Untergrenze** auf der Seite **Außenhandelsparameter**. Sie können diese Buchungen auch komprimieren, basierend auf den Einstellungen auch **Komprimierung von Intrastat**. Sie können die Vollständigkeit der Buchungen in der Intrastat-Erfassung überprüfen, basierend auf der Einstellung **Einstellungen prüfen** auf der Seite **Außenhandelsparameter**. Die Daten in den entsprechenden Feldern werden auf Vollständigkeit geprüft möglicherweise: Land/Region, Bundesland oder Kanton., Gewicht, Warencode, Buchungscode, zusätzliche Einheit, Port, Buchungsgrundlage, Lieferbedingungen, Transportmethode und Steuernummer. Buchungen, die nicht abgeschlossen sind, werden markiert als ungültig.

### <a name="3-use-the-intrastat-journal-to-report-information-about-trade-among-eu-countriesregions"></a>3. Mithilfe der Intrastat-Erfassung können Sie Informationen zum Handel zwischen EU-Ländern/Regionen melden

Zu statistischen Zwecken melden Sie Informationen zum Handel zwischen EU-Ländern/Regionen jeden Monat. Sie können den Intrastat-Bericht, basierend auf den Einstellungen **Berichtsformatzuordnung** drucken auf der **Außenhandelsparameter** Seite. Sie können auch eine elektronische Datei generieren, basierend auf den Einstellungen **Dateiformatzuordnung** auf der **Außenhandelsparameter** Seite. Siehe auch die zusammenfassende Meldungs-Berichterstellungs-Wiki-Seite für weitere Informationen zu zusammenfassenden Meldungen, einschließlich der erforderlichen Komponenten.

-   Generieren Sie eine EU-Intrastat-Meldung
-   Übertragen Sie Transaktionen an den Intrastat
-   Angeben der Ladungsadresse für eine Innergemeinschaftliche Buchung.

## <a name="prerequisites"></a>Voraussetzungen
In der folgenden Tabelle werden die Komponenten für Intrastat-Berichte angezeigt.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Voraussetzung</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Adresseinstellungen</td>
<td>Codes der Internationalen Organisation für Normung (ISO) für Länder/Regionen.</td>
</tr>
<tr class="even">
<td>Juristische Person</td>
<td>Einrichten von Umsatzsteuer-ID-Nummern für den Import/Exportieren, die Fillialnummer-Erweiterung für den Import/Export und den Intrastat-Code, der der juristischen Person zugeordnet wird.</td>
</tr>
<tr class="odd">
<td>Hierarchie der Produktkategorie (Vertriebshierarchie, Beschaffungshierarchie)</td>
<td>Weisen Sie die Intrastat-Warencodes den Kategorieknoten auf der Registerkarte <strong>Warencodes</strong> der Seite <strong>Kategoriehierarchie</strong> zu. Wenn Sie einen Warencode einem Knoten der übergeordneten Kategorie zuweisen, ist dieser Code auf alle Knoten der untergeordneten Kategorie anwendbar. Die ausgewählten Warencodes sind in der Ansicht <strong>Ausgewählt</strong> verfügbar, wenn Sie einen Warencode in den Details für freigegebene Produkte und in Aufträgen, Bestellungen und Umlagerungsauftragspositionen auswählen.</td>
</tr>
<tr class="even">
<td>Details für freigegebene Produkte</td>
<td>Richten Sie die folgenden Außenhandelsdaten für freigegebene Produkte ein:
<ul>
<li><strong>Warencode</strong> - Wählen Sie entweder aus der Liste der ausgewählten Waren aus, die von zugewiesenen Produktkategorien oder von der vollständigen Liste von Intrastat-Warencodes abgerufen wird.</li>
<li><strong>Statistischer Prozentsatz der Belastungen</strong></li>
<li><strong>Herkunftsland/-region</strong> - Wählen Sie das Standardland /-region aus, in dem die Waren vollständig erhalten oder produziert wurden.</li>
<li><strong>Bundesland/Kanton für Ursprung/Ziel</strong> - Wählen Sie das Standardbundesland/den Kanton des Ziels für Eingänge sowie das Ursprungsbundesland/den Kanton für den Versand aus.</li>
<li><strong>Nettogewicht in kg</strong></li>
</ul></td>
</tr>
<tr class="odd">
<td>Kunden</td>
<td>Richten Sie die Lieferadresse des Debitors im EU-Land/der EU-Region ein.</td>
</tr>
<tr class="even">
<td>Lieferanten</td>
<td>Richten Sie die Händleradresse im EU-Land/der EU-Region ein.</td>
</tr>
<tr class="odd">
<td>Sonstige Zuschläge</td>
<td>Richten Sie den Code für sonstige Zuschläge ein, der in den Rechnungsbetrag, im statistischen Betrag oder in beide einbezogen werden soll. Aktivieren Sie auf der Seite <strong>Codes für Belastungen</strong> auf der Registerkarte <strong>Außenhandel</strong> die Option <strong>Intrastat-Rechnungswert</strong>, um den Betrag der Zuschläge im Rechnungswert einzubeziehen, und aktivieren Sie <strong>Intrastat-Statistikwert</strong>, um den Betrag der Zuschläge im statistischen Wert einzubeziehen.</td>
</tr>
<tr class="even">
<td>Elektronische Berichterstellung</td>
<td>Einrichten der elektronischen Berichterstellungskonfigurationen, um Intrastat-Daten in einer elektronischen Datei zu exportieren, die das Format hat, das von den zuständigen Behörden angefordert wird, und Intrastat-Daten in einem benutzerfreundlichen, lesbaren Format in der Vorschau anzuzeigen (beispielsweise in Microsoft Excel).</td>
</tr>
<tr class="even">
<td>Lagerort</td>
<td>Zuordnen von Kreditorenkonten mit Lagerortcodes für das Ausfüllen der Steuernummer, wenn ein Umlagerungsauftrags übertragen wird.</td>
</tr>
</tbody>
</table>

## <a name="setup"></a>Einrichten
In den folgenden Abschnitten werden die Einstellungen beschrieben, die für Intrastat-Berichte erforderlich sind.

### <a name="set-up-all-required-intrastat-related-lists"></a>Einrichten aller erforderlichen Intrastat-zugeordneten Listen

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Liste</th>
<th>Weitere Informationen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Warencodes</td>
<td>Richten Sie eine Kategoriehierarchie vom Typ <strong>Warencode</strong> ein, und geben Sie alle Warencodes gemäß der Liste der kombinierten Nomenklatur ein. Für jede Ware richten Sie die folgenden Informationen ein:
<ul>
<li>Der Name der Ware und der Warencode</li>
<li>Der Anzeigename und/oder übersetzte Name</li>
<li>Einstellungen für das Melden von zusätzlichen (ergänzenden) Einheiten auf der <strong>Außenhandel</strong> Registerkarte. Sie können zusätzlich die Einheit in der Einheitsliste auswählen. Sie können auch angeben, ob das Gewicht von Waren zusätzlich zur ausgewählten zusätzlichen Einheit angegeben werden muss.</li>
</ul></td>
</tr>
<tr class="even">
<td>Art des Geschäftes</td>
<td>Richten Sie die Art der Buchung gemäß den Anforderungen Ihres Landes/Ihrer Region ein. Für jeden Buchungscode, den Sie einrichten, müssen Sie die Regeln für die Berechnung der Rechnungsbeträge und von statistischen Beträgen für Umlagerungsaufträge und Verkauf/Bestellungen einrichten.
<ul>
<li>Für Umlagerungsaufträge richten Sie eine der folgenden Regeln für die Berechnung der Rechnungsbeträge und statistischen Beträgen ein:
<ul>
<li><strong>Leer</strong> – Der Betrag ist 0 (Null).</li>
<li><strong>Wertmäßiger Einstandsbetrag</strong> – Der Betrag entspricht dem wertmäßigen Einstandsbetrag.</li>
<li><strong>Gesamtkosten</strong> – Der Betrag entspricht die Gesamtkosten der Buchung.</li>
<li><strong>Manuell</strong> – Der Betrag entspricht dem Betrag, der manuell auf der Umlagerungsauftragsposition angegeben ist.</li>
</ul></li>
<li>Für Aufträge und Bestellungen richten Sie eine der folgenden Regeln für die Berechnung der Rechnungsbeträge und statistischen Beträgen ein:
<ul>
<li><strong>Leer</strong> – Der Betrag ist 0 (Null).</li>
<li><strong>Rechnungsbetrag</strong> - Der Betrag entspricht dem Betrag, der für die Ware in Rechnung gestellt wird.</li>
<li><strong>Grundbetrag</strong> - Der Betrag entspricht dem Betrag, der gestellt werden, bevor einer beliebigen Rabatt angewendet wird.</li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td>Transportmethoden</td>
<td>Richten Sie den Transportmodus gemäß den Anforderungen Ihres Landes/Ihrer Region ein. Für jede Lieferart können Sie eine standardmäßige Transportmethode auf der Registerkarte <strong>Außenhandel</strong> einrichten.</td>
</tr>
<tr class="even">
<td>Ports</td>
<td>Richten Sie den Hafen/Flughafen des Ladens/Entladens ein, wenn diese Informationen von Ihrem Land/Ihrer Region erfasst werden.</td>
</tr>
<tr class="odd">
<td>Statistikverfahren</td>
<td>Richten Sie die Statistikverfahren ein, wenn diese Informationen von Ihrem Land/Ihrer Region erfasst werden.</td>
</tr>
</tbody>
</table>

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
<li>Die Standardtransaktionscodes für Aufträge, Bestellungen, Gutschriften und Umlagerungsaufträge. Der Buchungscode, der für Gutschriften eingerichtet wurde, wird auch als Code für die Rückgabe physischer Waren und zur Ermittlung der Abweichung von physischer Rückgaben gegenüber Korrekturgutschriften verwendet.</li>
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
</ul></td>
</tr>
<tr class="even">
<td>Kontaktinformationen des Beauftragten</td>
<td>Geben Sie Name, Adresse, die Umsatzsteuernummer, Telefonnummer und die Faxnummer des Agenten an.</td>
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

 




