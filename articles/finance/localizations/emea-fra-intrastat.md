---
title: Französisch Intrastat
description: Dieses Thema enthält Informationen zur Intrastat-Berichterstattung in Frankreich.
author: andosip
ms.date: 07/9/2021
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: v-aosipov
ms.search.validFrom: ''
ms.openlocfilehash: d38169d73caf93a0f81e832293916c9e54855a1848fe6ab409a670a4bf707b7c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6713135"
---
# <a name="french-intrastat"></a>Französisch Intrastat

[!include[banner](../includes/banner.md)]

Unternehmen in Frankreich, die für die Mehrwertsteuer (MwSt.) registriert sind und mit anderen Ländern der Europäischen Union (EU) Handel treiben, müssen den Austausch von Waren und Dienstleistungen von und nach Frankreich anmelden. Die DEB bzw. Declaration d'exchanges de Biens (Erklärung zum Außenhandel mit Gütern) ist eine Kombination aus zusammenfassender Meldung und Intrastat-Bericht. Sie müssen diesen Bericht monatlich für alle innergemeinschaftlichen Warenverkäufe einreichen.

Der DEB-Bericht kann im elektronischen Dateiformat SAISUNIC 330 oder INTRACOM generiert werden.

Die folgende Tabelle zeigt die Felder, die in der französischen Intrastat-Meldung im SAISUNIC 330-Format enthalten sind.

| **Feld**                   | **Berichtsstufe**   |              |
|-----------------------------|--------------------|--------------|
|                             | **4 (Vereinfacht)** | **1 (Full)** |
| Referenzzeitraum         | X                  | X            |
| Nummer der Erklärung       | X                  | X            |
| Positionsnummer                 | X                  | X            |
| ISO Ländercode (F)       | X                  | X            |
| Ergänzungscode          | X                  | X            |
| Sirenennummer                | X                  | X            |
| MwST Debitorencode        | X                  | X            |
| Richtungscode              | X                  | X            |
| Buchungstyp            | X                  | X            |
| Verpflichtungsstufe            | X                  | X            |
| Warencode              |                    | X            |
| National NGP                |                    | X            |
| Land (Abteilung)         |                    | X            |
| Buchungsdatum       |                    | X            |
| Ursprungsland      |                    | X            |
| Herkunftslandbericht - Import |                    | X            |
| Der endgültige Bestimmungsort. - Exporte |                    | X            |
| Rechnungswert               | X                  | X            |
| Statistischer Wert           |                    | X            |
| Nettogewicht                  |                    | X            |
| Besondere Maßeinheit            |                    | X            |
| Transportcode              |                    | X            |

Die folgende Tabelle zeigt die Felder, die in der französischen Intrastat-Meldung im INTRACOM-Format enthalten sind.

| **Feld**                   | **Berichtsstufe**   |              |
|-----------------------------|--------------------|--------------|
|                             | **4 (Vereinfacht)** | **1 (Full)** |
| Code                        | X                  | X            |
| Nummer der Erklärung       | X                  | X            |
| Anzahl Positionen              | X                  | X            |
| Sirene                       | X                  | X            |
| Land (Abteilung)         |                    | X            |
| Transportcode              |                    | X            |
| Ursprungsland           |                    | X            |
| Buchungsdatum       |                    | X            |
| Rechnungswert               | X                  | X            |
| Lieferarten           |                    | X            |
| Buchungstyp            | X                  | X            |
| Verpflichtungsstufe            | X                  | X            |
| Warencode              |                    | X            |
| National NGP                |                    | X            |
| Nettogewicht                  |                    | X            |
| Statistischer Wert           |                    | X            |
| Besondere Maßeinheit            |                    | X            |
| Herkunftslandbericht - Import |                    | X            |
| Der endgültige Bestimmungsort. - Exporte |                    | X            |
| MwST Debitorencode        | X                  | X            |
| Ergänzungscode          | X                  | X            |
| Referenzzeitraum         | X                  | X            |

### <a name="set-up-intrastat"></a>Einrichten von Intrastat

1.  In  [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index), in der Bibliothek der freigegebenen Anlagen laden Sie die neuesten Versionen der Konfigurationen für die elektronische Berichterstattung (ER) für das Format der Intrastaterklärung herunter:

-   Intrastat-Modell

-   Intrastat-Bericht

-   Intrastat INTRACOM (FR)

-   Intrastat SAISUNIC (FR)

Weitere Informationen finden Sie unter [Elektronische Berichtskonfigurationen aus Lifecycle Services herunterladen](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

2.  Wechseln Sie IN Dynamics 365 Finance zu **Steuer** &gt; **Einstellungen** &gt; **Außenhandel** &gt; **Außenhandelsparameter**.

    1.  Auf der **Intrastat** Registerkarte, auf dem Inforegistter **Elektronische Berichterstattung** im Feld **Dateiformatzuordnung** wählen Sie **Intrastat INTRACOM (FR)** oder **Intrastat SAISUNIC (FR)**.

    2.  Im Feld **Berichtformatzuordnung** **Intrastatbericht** auswählen.

    3.  Auf dem Inforegister **Warencodehierarchie** im Feld **Kategoriehierarchie** wählen Sie **Intrastat**.

    4.  Auf dem Inforegister **Allgemein** im Feld **Transaktions-Code** wählen Sie im Feld den Code aus, der für die Warenübertragung verwendet wird.

    5.  Im Feld **Gutschrift** wählen Sie im Feld den Code aus, der für die Warenrücksendung verwendet wird.

    6.  Im Feld **Verpflichtungsstufe für den Export** geben Sie im Feld den Detaillierungsgrad für den Exportbericht ein. Die ausgewählte Ebene wirkt sich auf die Zeilen aus, die im Bericht angezeigt werden. Weitere Informationen finden Sie in der Tabelle am Anfang dieses Themas.

3.  Gehen Sie zu **Organisationsverwaltung** &gt; **Organisationen** &gt; **Juristische Personen**, wählen Sie Ihr Unternehmen aus und führen Sie dann diese Schritte aus:

    1.  Auf dem Inforegister **Registrierungsnummern** im Feld **NAF-Code** geben Sie Ihren NAF-Code ein. Weitere Informationen finden Sie unter [FR-00003 NAF-Codes und SIRET-Nummern](tasks/fr-00003-naf-codes-siret-numbers.md).

    2.  Auf dem Inforegister **Außenhandel und Logistik** im **Intrastat** Abschnitt, legen Sie die **Export der Umsatzsteuer-Identifikationsnummer** und **Einfuhrumsatzsteuer-Identifikationsnummer** Felder fest.

    3.  Geben Sie im **Steuerregistrierung**-Inforegister im Feld **Steuernummer** die Steuernummer für Ihr Unternehmen an.

4.  Um NAF-Codes und Steuerbefreiungsnummern für Kunden anzugeben, gehen Sie zu **Debitoren** &gt; **Kunden** &gt; **Alle Kunden**, und befolgen Sie diese Schritte:

    1.  Wählen Sie einen Debitor aus.

    2.  Wählen Sie im **Rechnung und Lieferung**-Inforegister im Feld **Mehrwertsteuer** die **Umsatzsteuernummer** aus und wählen Sie Alle.

    3.  Im Inforegister **Vertriebsdemografie** im Feld **Französischer Siret** geben Sie die Siret-Nummer des Unternehmens ein.

    4.  Geben Sie im Feld **NAF-Dode** den NAF-Code des Unternehmens ein.

    5.  Wiederholen Sie diese Schritte für andere Kunden.

5.  Um NAF-Codes und Steuerbefreiungsnummern für Kunden anzugeben, gehen Sie zu **Kreditoren** &gt; **Lieferanten** &gt; **Alle Lieferanten**, und befolgen Sie diese Schritte:

    1.  Wählen Sie einen Kreditor aus.

    2.  Wählen Sie im **Rechnung und Lieferung**-Inforegister im Feld **Mehrwertsteuer** die **Umsatzsteuernummer des Lieferanten** aus.

    3.  Im Inforegister **Einkaufsdemografie** im Feld **Französischer Siret** geben Sie die Siret-Nummer des Unternehmens ein.

    4.  Geben Sie im Feld **NAF-Dode** den NAF-Code des Unternehmens ein.

    5.  Wiederholen Sie diese Schritte für andere Lieferanten.

6.  Gehen Sie zu **Steuer** &gt; **Installieren** &gt; **Außenhandel** &gt; **Kompression von Intrastat**, und wählen Sie die Felder aus, die verglichen werden sollen, wenn Intrastat-Informationen zusammengefasst werden. Wählen Sie für französisches Intrastat **Statistikverfahren**, **Herkunftsland**, **Herkunftsland/-Region**, **Lieferbedingungen**, **Transport**, **Korrektur**, **Land/Region**, **Herkunfts-/Bestimmungsland**, **Richtung**, **Land/Region des Absenders**, **Staat des Absenders**, **Zustand**, **Transaktions-Code**, und **Ware**.

7.  Gehen Sie zu **Warehouse Management** &gt; **Installieren** &gt; **Lagerhaus** &gt; **Lager**, wählen Sie ein Lager aus und führen Sie dann diese Schritte aus:

    1.  Wählen Sie im Inforegister **Adressen** **Hinzufügen** oder **Bearbeiten** aus.

    2.  Wählen Sie im Dialogfeld **Stadt** die Stadt des Lagerorts aus. Der Bundesstaat der Stadt wird als Landkreis für Ihren DEB-Bericht verwendet.

### <a name="ngp-codes"></a>NGP-Codes

Im DEB-Bericht besteht die Kodifizierung von Produkten aus folgenden Elementen:

1.  Der achtstellige CN8-Code, der die zolltarifliche und statistische Nomenklatur der EU darstellt.

2.  Falls zutreffend, der einstellige nationale Artikelcode der Nomenclature Générale des Produits (NGP).

Im Jahr 2021 gilt der NGP nur für drei Arten von Produkten:

-   Einige Produkte von Kühen, Schafen und Ziegen

-   Militärische Ausrüstung

-   Französische Weine

Sie müssen die NGP-Codes einrichten und sie verwandten Produkten zuweisen. Das **NGP** Feld wird dann automatisch auf der Seite **Intrastat-Journal** festgelegt.

#### <a name="set-up-an-ngp-code"></a>Richten Sie einen NGP-Code ein

1.  Wechseln Sie zu **Steuer** &gt; **Einstellungen** &gt; **Außenhandel** &gt; **NGP-Codes**.

2.  Wählen Sie im Aktivitätsbereich **Neu**, um einen NGP-Code zu erstellen.

3.  Im **NGP** geben Sie einen einstelligen Code ein.

4.  Geben Sie im Feld **Beschreibung** einen Beschreibung für den Code ein.

#### <a name="assign-an-ngp-code-to-a-product"></a>Zuweisen eines NGP-Codes zu einem Produkt

1.  Wechseln Sie zu **Produktinformationsverwaltung** &gt; **Produkte** &gt; **Freigegebene Produkte**.

2.  Wählen Sie im Raster ein Produkt aus.

3.  Auf dem Inforegister **Außenhandel** im **Intrastat** Abschnitt, im Feld **NGP** wählen Sie den entsprechenden NGP-Code aus.

## <a name="intrastat-journal"></a>Intrastat-Erfassungsfeld

Gehen Sie zu **Steuer** &gt; **Erklärungen** &gt; **Außenhandel** **Handel** &gt; **Intrastat**, um Ihre Transaktionen zu verwalten, die für den Außenhandel mit EU-Ländern gelten. Weitere Informationen finden Sie unter [Intrastat Übersicht](emea-intrastat.md).

Die  Spalte **NGP** ist spezifisch für Frankreich. Sie zeigt den NGP-Code für das Produkt. Wenn der NGP nicht auf ein Produkt anwendbar ist, wir **0** (Null) angezeigt. Sie können den NGP-Code anpassen. Wählen Sie die Transaktion aus und dann auf der **Allgemein** Registerkarte, im **Codes** Abschnitt unter **NGP** wählen Sie im Feld den erforderlichen NGP-Code aus.

### <a name="intrastat-transfer"></a>Intrastat-Übertragung

Auf der Seite **Intrastat** im Aktivitätsbereich können Sie **Überweisen** auswählen, um die Informationen über den innergemeinschaftlichen Handel aus Ihren Verkaufsaufträgen, Freitextrechnungen, Bestellungen, Lieferantenrechnungen, Lieferantenprodukteingängen, Projektrechnungen und Transferaufträgen automatisch zu übertragen. Es werden nur Dokumente übermittelt, die ein EU-Land als Bestimmungsland oder -Region (bei Versendungen) haben.

Da der DEB-Bericht eine Kombination aus der EU-Verkaufsliste und dem Intrastat-Bericht ist, enthält er auch *Dreiecks*-Transaktionen, bei denen eine direkte Lieferung von einem EU-Land (Partei A) in ein anderes EU-Land (Partei C) erfolgt und sich eine französische juristische Person (Partei B) mitten im Dreiecksgeschäft befindet.

### <a name="generate-a-deb-intrastat-report"></a>Generieren eines DEB (Intrastat)-Berichts

1.  Wechseln Sie zu **Steuer** &gt; **Meldungen** &gt; **Außenhandel** &gt; **Intrastat**.

2.  Wählen Sie im Aktivitätsbereich **Ausgabe** &gt; **Bericht**.

3.  Im angezeigten Dialogfeld **Intrastat-Bericht** legen Sie die folgenden Felder fest.

| Feld            | Beschreibung                                                                                                                         |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| Anfangsdatum        | Wählen Sie das Startdatum für den Bericht.                                                                                               |
| Bis-Datum          | Wählen Sie das Enddatum für den Bericht.                                                                                                 |
| Datei generieren    | Legen Sie diese Option auf **Ja** fest, um eine .txt Datei zu generieren.                                                                                 |
| Dateiname        | Geben Sie den Namen der .txt-Datei für Ihren Intrastat-Bericht ein.                                                                          |
| Bericht generieren  | Legen Sie diese Option auf **Ja** fest, um eine .xml-Datei zu generieren.                                                                                |
| Berichtdateiname | Geben Sie die erforderlichen Namen ein.                                                                                                            |
| Nur Korrekturen | Legen Sie diese Option auf **Ja** fest, um nur Korrekturen zu melden. Wenn Sie **Nein** festlegen, werden sowohl normale Transaktionen als auch Korrekturen gemeldet.         |
| Planungsrichtung        | **Eingang** für einen Bericht über die innergemeinschaftlichen Eingänge auswählen. **Versand** für einen Bericht über innergemeinschaftliche Versendungen auswählen. |

## <a name="example"></a>Beispiel

Das folgende Beispiel zeigt, wie Sie NGP-Codes einrichten und damit arbeiten. Sie verwenden die **DEMF** juristische Person verwenden.

1.  In  [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index), in der Bibliothek der freigegebenen Anlagen laden Sie die neuesten Versionen der Konfigurationen für die elektronische Berichterstattung (EB) für das Format der Intrastaterklärung herunter:

-   Intrastat-Modell

-   Intrastat-Bericht

-   Intrastat INTRACOM (FR)

2.  Richten Sie in Finance einen Transaktionscode ein:

    1.  Wechseln Sie zu **Steuer** &gt; **Einstellungen** &gt; **Außenhandel** &gt; **Transaktionscodes**.

    2.  Wählen Sie im Aktivitätsbereich **Neu** aus.

    3.  Geben Sie im Feld **Transaktionscode** **11** ein.

    4.  Geben Sie im Feld **Name** **Kauf oder Verkauf ein** ein.

    5.  Wählen Sie im Aktionsbereich **Speichern** aus.

3.  Produktimporthierareinrichten:

    1.  Wechseln Sie zu **Produktinformationsverwaltung** &gt; **Einrichtung** &gt; **Kategorien und Attribute** &gt; **Kategoriehierarchie**.

    2.  Wählen Sie im Raster **Intrastat** aus. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Kategoriehierarchie** in der Gruppe **Verwalten** auf **Bearbeiten**.

    3.  Klicken Sie im Aktivitätsbereich auf **Neuer Kategorieknoten**.

    4.  Geben Sie im Feld **Name** **Autres Libournais** ein.

    5.  Geben Sie im Feld **Code** **2204 21 42** ein

    6.  Wählen Sie im Aktionsbereich **Speichern** aus.

4.  Wechseln Sie zu **Steuer** &gt; **Einstellungen** &gt; **Außenhandel** &gt; **Außenhandelsparameter** und folgen Sie diesen Schritten:.

    1.  Auf der **Intrastat** Registerkarte, auf dem Inforegister **Allgemein** im **Transaktions-Code** Feld, wählen Sie **11**.

    2.  Auf dem Inforegister **Elektronische Berichterstattung** im **Dateiformatzuordnung** Feld, wählen Sie **Intrastat INTRACOM (FR)**.

    3.  Im Feld **Berichtformatzuordnung** **Intrastatbericht** auswählen.

    4.  Auf dem Inforegister **Warencodehierarchie** im Feld **Kategoriehierarchie** wählen Sie **Intrastat**.

5.  Richten Sie einen NGP-Code ein:

    1.  Wechseln Sie zu **Steuer** &gt; **Einstellungen** &gt; **Außenhandel** &gt; **NGP-Codes**.

    2.  Wählen Sie im Aktivitätsbereich **Neu** aus.

    3.  Geben Sie im Feld **NGP** den Wert **8** ein.

    4.  Geben Sie im Feld **Name eine Beschreibung** **NGP 8** ein.

    5.  Wählen Sie im Aktionsbereich **Speichern** aus.

6.  Zuweisen eines NGP-Codes zu einem Produkt:

    1.  Wechseln Sie zu **Produktinformationsverwaltung** &gt; **Produkte** &gt; **Freigegebene Produkte**.

    2.  Wählen Sie im Raster **0001** aus.

    3.  Wählen Sie auf dem Inforegister **Außenhandel** im Feld **NGP** die Option **8** aus.

    4.  Geben Sie im Feld **Ware** ein und wählen Sie **2204 21 42**.

    5.  Wählen Sie im Aktionsbereich **Speichern** aus.

7.  Erstellen Sie einen Kundenauftrag, der das neue Produkt enthält:

    1.  Wechseln Sie zu **Debitoren** &gt; **Aufträge** &gt; **Alle Aufträge**.

    2.  Wählen Sie im Aktivitätsbereich **Neu** aus.

    3.  Im Dialogfeld **Erstellen** **Verkauf** **Auftraag** im Abschnitt **Kundebereich** im Feld **Kunde** **Konto** wählen Sie **100001**.

    4.  Im **Adresse** Abschnitt, im Feld **Lieferadresse** wählen Sie das Pluszeichen (**+**), um eine Adresse zu erstellen.

    5.  Geben Sie im **Neue Adresse**-Dialogfeld im Feld **Name Funktionsbeschreibung** **Deutschland** ein.

    6.  Wählen Sie im Feld **Land/Region** **DEU** aus.

    7.  Wählen Sie **OK** aus.

    8.  Wählen Sie im Dialogfeld  **Neuen Auftrag erstellen** und dann **OK** aus.

    9.  Im Inforegister **Verkauf** im Feld **Auftragszeile** wählen Sie **Artikelnummer** **0001**.

    10. Wählen Sie im Aktionsbereich **Speichern** aus.

    11. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Rechnung** in der Gruppe **Generieren** **Rechnung** aus.

    12. Im **Rechnung buchen** Dialogfeld, auf dem **Parameter** Inforegiser im **Parameter** Abschnitt, im **Menge** Feld, wählen Sie **Alle**. Wählen Sie **OK** um die Rechnung zu buchen.

8.  Erstellen des DEB-Berichts:

    1.  Wechseln Sie zu **Steuer** &gt; **Meldungen** &gt; **Außenhandel** &gt; **Intrastat**:

    2.  Klicken Sie im Aktivitätsbereich. wählen Sie **Übertragen** aus.

    3.  Im **Intrastat (Übertragung)** Dialogfeld, im **Parameter** Abschnitt, legen Sie die **Kundenrechnung** Option auf **Ja** fest. Wählen Sie dann **OK** aus.

    4.  Transaktionen nach **Datum** Feld sortieren. Die oberste Transaktion ist die Ergebnistransaktion. Das Feld **NGP** wird automatisch festgelegt.

    5.  Wählen Sie im Aktivitätsbereich **Ausgabe** &gt; **Bericht**.

    6.  Im **Intrastat-Bericht** Dialogfeld, auf dem Inforegister **Parameter** im Abschnitt **Datum** wählen Sie im Abschnitt den Monat des von Ihnen erstellten Kundenauftrags aus.

    7.  Im Abschnitt **Exportoptionen** legen Sie die **Datei generieren** Option auf **Ja** fest.

    8.  Geben Sie im Feld **Dateiname** den erforderlichen Namen ein.

    9.  **OK** wählen und den Bericht überprüfen.

