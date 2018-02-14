---
title: Zusammenfassende Meldung
description: "Dieser Artikel enthält Informationen über Verkaufslisten-Berichte der Europäischen Union (EU)."
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EUSalesList
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 12811
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: epopov
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: b55d64dba11f3bf0e0cb549752af44a487dcb348
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="eu-sales-list-reporting"></a>Zusammenfassende Meldung

[!include[banner](../includes/banner.md)]


Dieser Artikel enthält Informationen über Verkaufslisten-Berichte der Europäischen Union (EU).

<a name="eu-sales-list-reporting"></a>Zusammenfassende Meldung
-----------------------

Ein Lieferant, der innergemeinschaftliche Lieferungen von Waren oder Dienstleistungen an Unternehmen ausführt, die innerhalb der Europäischen Union (EU) gegründet wurden, muss eine Erklärung für innergemeinschaftliche Lieferungen (zusammenfassende Meldung oder ESL) einreichen. Im Allgemeinen muss die ESL an die Steuerbehörden spätestens bis zum letzten Tag des Monats nach dem Kalenderzeitraum, den die ESL umfasst, übermittelt werden. Der Lieferant muss seine Umsatzsteuer-Identifikationsnummer auf der ESL und nach Debitor auch die folgenden Informationen angeben:

-   Umsatzsteuer-Identifikationsnummer des EU-Debitors
-   Gesamtwert der innergemeinschaftlichen Lieferungen von Waren und Dienstleistungen an den EU-Kunden in diesem Zeitraum. Der Lieferant muss auch allgemeine Warenlieferungen von Dreieckshandellieferungen trennen. Eine Dreieckshandelbuchung umfasst Direktlieferung von Waren vom Lieferanten des Lieferanten an den Debitor, wenn beide Parteien in anderen EU-Mitgliedsstaaten erfasst sind.

Indem sie die ESL verwenden, können Steuerbehörden von jedem EU-Mitgliedsstaat überprüfen, ob USt für jede Innergemeinschaftsbuchung bezahlt wurde. Mit der Kombination von Listen und Umsatzsteuererklärungen können EU-Mitgliedsstaaten Informationen zu dem Fluss von Waren in der EU austauschen.

## <a name="overview-of-the-eu-sales-list-reporting-process"></a>Überblick über die zusammenfassende Meldung
Sie können die folgenden Aufgaben für eine zusammenfassende Meldung ausführen:

-   Sammeln von Informationen zu Innergemeinschaftshandelsbuchungen. Eine Innergemeinschaftshandelsbuchung kann eine Verkaufsrechnung, eine Freitextrechnung, Projektrechnung oder eine Kreditorenrechnung sein. Eine Buchung wird auf Basis des Landes/der Region der Gegenpartei identifiziert. Innergemeinschaftshandelsbuchungen verschiedener Arten werden in der Tabelle für die zusammenfassende Meldung gesammelt, in der sie im Allgemeinen Formular dargestellt werden. Jeder Datensatz der ESL-Tabelle stellt eine einzelne Buchung dar und besteht aus dem USt-Bezeichner einer Gegenpartei und dem Gesamtwert von Waren und Dienstleistungen, die geliefert wurden.
-   (Optional) Anzeigen der **zusammenfassenden Meldung** in der Vorschau. Sie können die **zusammenfassende Meldung** für eine bestimmte Periode in Form einer Microsoft-Excel-Arbeitsmappe in der Vorschau anzeigen und überprüfen.
-   Erstellen der **zusammenfassenden Meldung**. Die **zusammenfassende Meldung** wird in Form einer elektronischen Datei eines bestimmten Formats generiert, das für jeden Mitgliedsstaat der EU spezifisch ist. Im Allgemeinen enthält eine **zusammenfassende Meldung** grundlegende Informationen über die Berichterstellungspartei und Werte von Waren- und Dienstlieferungen. Die Informationen werden nach Land und das USt-Bezeichner einer Gegenpartei gruppiert.
-   Schließen des Zeitraums der zusammenfassenden Meldung. Nachdem die **zusammenfassende Meldung** generiert und an Behörden übermittelt wurde, können die Datensätze der ESL-Tabelle als **geschlossen** markiert werden. Diese Buchungen werden nicht in weitere Berichte eingeschlossen.

## <a name="prerequisites"></a>Erforderliche Komponenten
In der folgenden Tabelle werden die Voraussetzungen angezeigt, die vorhanden sein müssen, bevor Sie beginnen können.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Kategorie</th>
<th>Voraussetzung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Einrichten:</strong> Juristische Person</td>
<td>Die primäre Adresse der juristischen Person muss in einem EU-Mitgliedsstaat sein. Wählen Sie auf der Seite <strong>Juristische Personen</strong> (klicken Sie auf <strong>Organisationsverwaltung</strong> &gt; <strong>Organisationen</strong> &gt; <strong>Juristische Personen</strong>) und wählen Ihre juristische Person aus. Erstellen Sie auf dem <strong>Adressen</strong>-Inforegister eine Adresse, wählen Sie ein Land/eine Region und andere Adressenkomponenten aus, und markieren Sie die Adresse als <strong>Primär</strong>. Geben Sie im <strong>Steuerregistrierung</strong>-Inforegister im Feld <strong>Steuernummer</strong> die Steuernummer für Ihr Unternehmen an.</td>
</tr>
<tr class="even">
<td><strong>Einrichten:</strong> Parameter für Umsatzsteuernummer</td>
<td>Richten Sie die Parameter für Umsatzsteuernummer auf der Seite <strong>Länder-/Regionsparameter</strong> ein (klicken Sie auf <strong>Steuer</strong> &gt; <strong>Einstellungen</strong> &gt; <strong>Mehrwertsteuer</strong> &gt; <strong>Länder-/Regionsparameter</strong>). Für jede(s) Land/Region, in dem/der Sie Gegenparteien haben, erstellen Sie einen Datensatz auf der Seite und geben Sie die folgenden Informationen ein:
<ul>
<li><strong>Land/Region</strong> – Hier können Sie ein Land/eine Region auswählen, um es bzw. sie einer Umsatzsteuer-Identifikationsnummer zuzuordnen.</li>
<li><strong>Mehrwertsteuer</strong> – Geben Sie die Umsatzsteuernummer (das heißt, das Umsatzsteuernummernpräfix) für das/die ausgewählte Land/Region ein.</li>
<li><strong>Umsatzsteuernummer überprüfen</strong> – Aktivieren Sie dieses Kontrollkästchen, um die Umsatzsteuer-Identifikationsnummer für das ausgewählte Land/die ausgewählte Region zu überprüfen.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Einrichten: </strong>USt-IdNr.</td>
<td>Erstellen Sie Umsatzsteuer-ID-Nummern für Ihre Gegenparteien auf der Seite <strong>USt-IdNr.</strong> (klicken Sie auf <strong>Steuer</strong> &gt; <strong>Einstellungen</strong> &gt; <strong>Mehrwertsteuer</strong> &gt; <strong>USt-IdNr</strong>.). Erstellen Sie für jede Umsatzsteuernummer einen Datensatz auf der Seite, und geben Sie die folgenden Informationen an:
<ul>
<li><strong>Land/Region </strong>– Wählen Sie das Land/die Region der Steuerregistrierung der Gegenpartei aus.</li>
<li><strong>Umsatzsteuernummer</strong> – Geben Sie die Umsatzsteuernummer der Gegenpartei ein.</li>
<li><strong>Unternehmensname</strong> – (Optional) Geben Sie den Namen der Gegenpartei ein.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Einstellungen: </strong>Steuerregistrierung von Gegenparteien</td>
<td>Richten Sie Steuerregistrierungsinformationen für Ihre Gegenparteien entweder auf der Seite <strong>Alle Debitoren</strong> (klicken Sie auf <strong>Vertrieb und Marketing </strong>&gt; <strong> Debitoren</strong> &gt; <strong>Alle Debitoren</strong>, wählen Sie einen Debitorendatensatz aus, und klicken Sie dann auf <strong>Optionen</strong> &gt; <strong>Ansicht wechseln</strong> &gt; <strong>Detailansicht)</strong> oder der Seite <strong>Kreditoren</strong> (klicken Sie auf <strong>Beschaffung</strong> &gt; <strong>Kreditoren</strong> &gt; <strong>Kreditoren,</strong> wählen Sie einen Kreditorendatensatz aus, und klicken Sie dann auf <strong>Optionen</strong> &gt; <strong> Ansicht wechseln</strong> &gt; <strong>Detailansicht</strong>) ein. Wählen Sie im <strong>Rechnung und Lieferung</strong>-Inforegister im Feld <strong>Umsatzsteuernummer</strong> die USt-IdNr. aus.</td>
</tr>
<tr class="odd">
<td><strong>Einrichten: </strong>Mehrwertsteuer</td>
<td>Richten Sie die Steuercodes für die zusammenfassende Meldung auf der Seite <strong>EU Verkaufsliste</strong> auf der Seite <strong>Steuercodes</strong> (klicken Sie auf <strong>Steuer</strong> &gt; <strong>Indirekte Steuern</strong> &gt; <strong>Verkaufssteuer</strong> &gt; <strong>Verkaufssteuercodede</strong>). Deaktivieren Sie im <strong>Berichtseinstellungen</strong>-Inforegister für jeden Mehrwertsteuercode, der in den Bericht einbezogen werden soll, das <strong>Ausgeschlossen </strong>-Kontrollkästchen. Richten Sie die Mehrwertsteuerparameter für Artikel auf der <strong>Artikel-Mehrwertsteuergruppen</strong>-Seite ein (klicken Sie auf <strong>Steuer</strong> &gt; <strong>Indirekte Steuern</strong> &gt; <strong>Mehrwertsteuer</strong> &gt; <strong>Artikel-Mehrwertsteuergruppen</strong>). Wählen Sie für jede Artikel-Mehrwertsteuergruppe im Feld <strong>Berichtstyp</strong> einen Wert aus. Der Wert, den Sie auswählen, bestimmt die ESL-Betragsspalte, in der der Positionsbetrag enthalten ist.
<ul>
<li><strong>Leer</strong> – Der Positionsbetrag wird in die Spalte <strong>Nicht zugewiesener Wert</strong> eingeschlossen.</li>
<li><strong>Artikel</strong> – Der Positionsbetrag wird in die Spalte <strong>Artikelwert</strong> einbezogen.</li>
<li><strong>Service</strong> – Der Positionsbetrag wird in die Spalte <strong>Servicewert</strong> einbezogen.</li>
<li><strong>Investition</strong> – Der Positionsbetrag wird in die Spalte <strong>Investitionswert</strong> einbezogen. Diese Spalte ist nur für Belgien relevant.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Einrichten:</strong> ESL-Berichterstellungskonfigurationen</td>
<td>Importieren oder erstellen Sie elektronische Berichtskonfigurationen für die ESL. Informationen darüber, wie elektronische Berichterstellungskonfigurationen erstellt und verwaltet werden, finden Sie in der elektronischen Berichterstellungsdokumentation.</td>
</tr>
<tr class="odd">
<td><strong>Einrichten: </strong>Allgemeine Parameter</td>
<td>Richten Sie die ESL-Berichtsparameter auf der Seite <strong>Außenhandelsparameter</strong> ein (klicken Sie auf <strong>Steuer</strong> &gt; <strong>Einrichten</strong>&gt; <strong>Außenhandel</strong> &gt; <strong>Außenhandelsparameter</strong>). Geben Sie die folgenden Parameter an:
<ul>
<li>Registerkarte <strong>Zusammenfassende Meldung</strong>:
<ul>
<li><strong>Skonto melden</strong> – Aktivieren Sie dieses Kontrollkästchen, wenn ein Skonto im Wert enthalten sein soll, wenn eine Buchung in der ESL einbezogen ist.</li>
<li><strong>Einkäufe übertragen</strong> – Aktivieren Sie dieses Kontrollkästchen, um Einkäufe in der ESL einzubeziehen.</li>
<li><strong>Dateiformatzuordnung</strong> – Wählen Sie das elektronische Berichterstellungsformat aus, das verwendet werden soll, wenn eine elektronische Datei für die ESL generiert wird.</li>
<li><strong>Berichtformatzuordnung</strong> – Wählen Sie das elektronische Berichterstellungsformat aus, das verwendet werden soll, wenn ein Vorschaubericht für die ESL generiert wird.</li>
<li><strong>Rundungsregel</strong> – Geben Sie eine reelle Zahl für das Runden an. ESL-Beträge werden auf das Vielfache dieser Zahl gerundet.</li>
<li><strong>Rundungsmethode</strong> – Wählen Sie die Rundenmethode aus, die verwendet werden soll, wenn ESL-Beträge gerundet werden (<strong>Normal</strong>, <strong>Abrunden</strong> oder <strong>Aufrunden</strong>).</li>
<li><strong>Mindestwert verwenden</strong> – Aktivieren Sie dieses Kontrollkästchen, wenn Beträge, die kleiner sind als die <strong>Rundungsregel</strong>-Zahl, auf die <strong>Rundungsregel</strong>-Zahl gerundet werden sollen.</li>
<li><strong>Dezimalstellen</strong> – Geben Sie die Anzahl der Dezimalstellen an, die in ESL-Beträgen angezeigt werden sollen (in elektronischen Dateien und im <strong>ESL-Vorschau</strong>-Bericht.</li>
</ul></li>
<li><strong>Länder-/Regionsparameter</strong>-Registerkarte: Identifizieren Sie EU-Mitgliedsstaaten. Erstellen Sie für jeden EU-Mitgliedstaat einen Datensatz auf der Seite, und geben Sie die folgenden Informationen an:
<ul>
<li><strong>Land/Region</strong> – Wählen Sie ein Land/eine Region aus.</li>
<li><strong>Länder-/Regionsart</strong> – Wenn der <strong>Land/Region</strong>-Wert das Land/die Region ist, in dem/der Ihr Unternehmen erfasst ist, wählen Sie <strong>Inland</strong> aus. Wenn der <strong>Land/Region</strong>-Wert ein anderer EU-Mitgliedstaat ist als das Land/die Region, in dem/der Ihr Unternehmen erfasst ist, wählen Sie <strong>EU</strong> aus. Wenn der <strong>Land/Region</strong>-Wert kein EU-Mitgliedsstaat ist, wählen Sie <strong>Drittland/-region</strong> aus.</li>
</ul></li>
<li><strong>Nummernkreise</strong>-Registerkarte: Wählen Sie auf der Position, in der der <strong>Referenz</strong>-Wert <strong>Zusammenfassende Meldung</strong> entspricht, einen Nummernkreiscode aus.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Zugehörige Transaktionen</strong></td>
<td><ul>
<li>Registrieren eines Verkaufs an einen Kunden in einem anderen EU-Mitgliedsstaat.</li>
<li>Registrieren einer Freitextrechnung für einen Kunden in einem anderen EU-Mitgliedsstaat.</li>
<li>Registrieren einer Projektrechnung für einen Kunden in einem anderen EU-Mitgliedsstaat.</li>
<li>Registrieren einer Rechnung von einem Kreditor in einem anderen EU-Mitgliedsstaat.</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="working-with-the-esl"></a>Arbeiten mit der ESL
### <a name="collecting-information-about-intra-community-trade-transactions"></a>Sammeln von Informationen zu Innergemeinschaftshandelsbuchungen

Buchungen der folgenden Typen gelten als Innergemeinschaftshandelsbuchungen:

-   Verkaufsrechnungen
-   Freitextrechnungen
-   Projektrechnungen
-   Kreditorenrechnungen

Eine Buchung gilt als eine Innergemeinschaftshandelsbuchung, wenn die Lieferadresse der Buchung in einem Mitgliedsstaat der EU ist. Für solche Länder/Regionen sollte ein Datensatz in der Registerkarte **Länder-/Regionsparameter** der Seite **Außenhandelsparameter** vorhanden sein, und der **Länder-/Regionsart**-Wert sollte auf **EU** festgelegt sein. Innergemeinschaftshandelsbuchungen werden im Feld **Listencode** markiert. Mit diesem Feld können Sie auch allgemeine Innergemeinschaftshandelsbuchungen von Dreieckshandelbuchungen trennen. Sie können Informationen über innergemeinschaftliche Handelsbuchungen auf der Seite **EU-Verkaufsliste** erfassen (klicken Sie auf **Steuer** &gt; **Erklärung** &gt; **Außenhandel** &gt; **EU Verkaufslistet**) mithilfe der Funktion **Übertragung**. Mit dieser Funktion können Sie Buchungen mit Beträgen von verschiedenen Berichtstypen (d. h. Artikel oder Dienstleistungen) einschließen, gemäß der Artikel-Mehrwertsteuergruppen, die in Buchungspositionen angegeben werden. Sie können auch andere Filter anwenden, um die Buchungen zu definieren, die einbezogen werden sollen. Die **Übertragen**-Funktion erstellt einen Datensatz auf der **Zusammenfassende Meldung**-Seite für jede Innergemeinschaftshandelsbuchung, die einbezogen wird, und gibt eine Gegenparteikontonummer, ein Land/eine Region, eine Umsatzsteuernummer, eine Rechnungsnummer und ein Datum und die Gesamtbeträge von Positionen pro Berichtstyp an. Sie kopiert auch den **Listencode**-Wert aus der Buchung. Sie können den Listencode für eine Buchung auf der Seite **Zusammenfassende Meldung** manuell ändern. Die **Übertragen**-Funktion erstellt Datensätze, wobei der Wert **Berichtsstatus** auf **Enthalten** festgelegt wird. Sie können die Informationen prüfen, die auf der Seite **Zusammenfassende Meldung**erfasst werden, indem Sie die Funktion **Prüfen** verwenden.

### <a name="generating-the-eu-sales-list-report"></a>Erstellen der zusammenfassenden Meldung

Sie können eine **Zusammenfassende Meldung** generieren, indem Sie die Funktion **Berichterstellung**auf der Seite **Zusammenfassende Meldung**verwenden. Mit der Funktion können Sie einen Berichtszeitraum auswählen und Filter anwenden, um die ESL-Datensätze zu definieren, die einbezogen werden sollen. Darüber hinaus können Sie andere Parameter angeben, die in jedem Land/jeder Region spezifisch sind. Sie können auch wählen, einen Vorschaubericht, eine elektronische Datei oder beides zu generieren. Die **Berichterstellung**-Funktion verwendet die Berichts- und Dateiformateinstellungen, die auf der Seite **Außenhandelsparameter**angegeben sind. Im Allgemeinen besteht eine **Zusammenfassende Meldung** aus separaten Positionen, die die Gesamtbeträge der Lieferungen pro Gegenparteiland/-region, Umsatzsteuernummer und Berichtstyp auflisten (Dreieckshandelbuchungen werden eingeschlossen). Nachdem Sie eine **Zusammenfassende Meldung** für eine bestimmte Perioden generiert haben, können Sie die ESL-Datensätze markieren, die im Bericht enthalten sind, indem Sie den Wert **Berichtsstatus** auf **Berichtet** festlegen. Um diesen Status festzulegen, verwenden Sie die **Als berichtet markieren**-Funktion auf der Seite **Zusammenfassende Meldung**.

### <a name="closing-the-eu-sales-list-reporting-period"></a>Schließen des Zeitraums der zusammenfassenden Meldung

Wenn Sie den Berichterstellungsprozess für eine bestimmte Periode abgeschlossen haben (beispielsweise, wenn Steuerbehörden die **Zusammenfassende Meldung** angenommen haben), können Sie die ESL-Datensätze markieren, die im Bericht für die Periode enthalten sind, indem Sie den Wert **Berichtsstatus** auf **Geschlossen** festlegen. Um diesen Status festzulegen, verwenden Sie die **Als geschlossen markieren**-Funktion auf der Seite **Zusammenfassende Meldung**. Wenn Sie den Abschluss der Periode zurücksetzen, können Sie ESL-Datensätze markieren, indem Sie den Wert **Berichtsstatus** auf **Enthalten** festlegen. Diese Datensätze können erneut in einer **Zusammenfassenden Meldung** eingeschlossen werden. Um diesen Status festzulegen, verwenden Sie die **Als** **einbezogen markieren**-Funktion auf der Seite **Zusammenfassende Meldung**.




