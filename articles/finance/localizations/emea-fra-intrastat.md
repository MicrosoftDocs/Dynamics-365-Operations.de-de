---
title: Französisch Intrastat
description: Dieser Artikel enthält Informationen zur Intrastat-Berichterstattung in Frankreich.
author: anasyash
ms.date: 11/30/2022
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: ''
ms.openlocfilehash: 2076649c7fff9f47b9c1fda62a103168b19bb973
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831804"
---
# <a name="french-intrastat"></a>Französisch Intrastat

[!include[banner](../includes/banner.md)]

Unternehmen in Frankreich, die für die Mehrwertsteuer (MwSt.) registriert sind und mit anderen Ländern der Europäischen Union (EU) Handel treiben, müssen den Austausch von Waren und Dienstleistungen von und nach Frankreich anmelden. Die DEB bzw. Declaration d'exchanges de Biens (Erklärung zum Außenhandel mit Gütern) ist eine Kombination aus zusammenfassender Meldung und Intrastat-Bericht. Sie müssen diesen Bericht monatlich für alle innergemeinschaftlichen Warenverkäufe einreichen.

Der DEB-Bericht kann im elektronischen Dateiformat SAISUNIC 330 oder INTRACOM generiert werden.

Die folgende Tabelle zeigt die Felder, die in der französischen Intrastat-Meldung im SAISUNIC 330-Format enthalten sind. Die Tabelle gibt auch die Berichtsebenen jedes Felds an. Ein Feld kann die folgenden Berichtsebenen haben:

- **4** – Steuererklärung.
- **1** – Statistikantwort.
- **5** – Statistikantwort auf Lieferung und Steuererklärung und gemeinsames Ausfüllen.

| Feld                       | Berichtsstufen |
|-----------------------------|---------------|
| Referenzzeitraum         | 4, 1, 5       |
| Nummer der Erklärung       | 4, 1, 5       |
| Positionsnummer                 | 4, 1, 5       |
| ISO Ländercode (F)       | 4, 1, 5       |
| Ergänzungscode          | 4, 1, 5       |
| Sirenennummer                | 4, 1, 5       |
| MwST Debitorencode        | 4, 1, 5       |
| Richtungscode              | 4, 1, 5       |
| Buchungstyp            | 4, 1, 5       |
| Verpflichtungsstufe            | 4, 1, 5       |
| Warencode              | 1, 5          |
| National NGP                | 1, 5          |
| Land (Abteilung)         | 1, 5          |
| Buchungsdatum       | 1, 5          |
| Ursprungsland      | 1, 5          |
| Herkunftslandbericht - Import | 1, 5          |
| Der endgültige Bestimmungsort. - Exporte | 1, 5          |
| Rechnungswert               | 4, 1, 5       |
| Statistischer Wert           | 1, 5          |
| Nettogewicht                  | 1, 5          |
| Besondere Maßeinheit            | 1, 5          |
| Transportcode              | 1, 5          |

Die folgende Tabelle zeigt die Felder, die in der französischen Intrastat-Meldung im INTRACOM-Format enthalten sind. Die Tabelle gibt auch die Berichtsebenen jedes Felds an. Ein Feld kann die folgenden Berichtsebenen haben:

- **4** – Steuererklärung.
- **1** – Statistikantwort.
- **5** – Statistikantwort auf Lieferung und Steuererklärung und gemeinsames Ausfüllen.

| Feld                       | Berichtsstufen |
|-----------------------------|---------------|
| Richtungscode              | 4, 1, 5       |
| Nummer der Erklärung       | 4, 1, 5       |
| Anzahl Positionen              | 4, 1, 5       |
| Sirene                       | 4, 1, 5       |
| Land (Abteilung)         | 1, 5          |
| Transportcode              | 1, 5          |
| Ursprungsland           | 1, 5          |
| Buchungsdatum       | 1, 5          |
| Rechnungswert               | 4, 1, 5       |
| Lieferarten           | 1, 5          |
| Buchungstyp            | 4, 1, 5       |
| Verpflichtungsstufe            | 4, 1, 5       |
| Warencode              | 1, 5          |
| National NGP                | 1, 5          |
| Nettogewicht                  | 1, 5          |
| Statistischer Wert           | 1, 5          |
| Besondere Maßeinheit            | 1, 5          |
| Herkunftslandbericht - Import | 1, 5          |
| Der endgültige Bestimmungsort. - Exporte | 1, 5          |
| MwST Debitorencode        | 4, 1, 5       |
| Ergänzungscode          | 4, 1, 5       |
| Referenzzeitraum         | 4, 1, 5       |

## <a name="set-up-intrastat"></a>Einrichten von Intrastat

- Laden Sie in [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/Logon/Index) in der Bibliothek der freigegebenen Anlagen die neuesten Versionen der Konfigurationen für die elektronische Berichterstellung (EB) für die Intrastat-Meldung herunter.

    - Intrastat-Modell
    - Intrastat-Bericht
    - Intrastat INTRACOM (FR)
    - Intrastat SAISUNIC (FR)

    Weitere Informationen finden Sie unter [Elektronische Berichtskonfigurationen aus Lifecycle Services herunterladen](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

### <a name="set-up-vat-ids"></a>Einrichten der MwSt Kennungen

#### <a name="set-up-vat-codes-for-your-company"></a>Einrichten von MwSt.-Codes für Ihr Unternehmen

1. Gehen Sie zu **Steuer** \> **Einstellungen** \> **Mehrwertsteuer** \> **USt-IdNr.**.
2. Wählen Sie im Aktivitätsbereich **Neu** aus.
3. Wählen Sie im Feld **Land/Region** **FRA** aus.
4. Im Feld **Steuerbefreiungsnummer** geben Sie die Mehrwertsteuernummer (MwST.-Nummer) Ihres Unternehmens ein.
5. Gehen Sie zu **Organisationsverwaltung** \> **Organisationen** \> **Juristische Personen**, und wählen Sie Ihr Unternehmen aus.
6. Auf dem Inforegister **Außenhandel und Logistik** im **Intrastat** Abschnitt, legen Sie die **Export der Umsatzsteuer-Identifikationsnummer** und **Einfuhrumsatzsteuer-Identifikationsnummer** Felder fest für den Code, den Sie in Schritt 4 erstellt haben.
7. Geben Sie im **Steuerregistrierung**-Inforegister im Feld **Steuernummer** die Steuernummer für Ihr Unternehmen an.

#### <a name="set-up-the-vat-ids-for-trading-partners"></a>USt-IdNr. für Handelspartner einrichten

##### <a name="create-a-registration-type-for-the-company-code"></a>Eine Registrierungsart für den Unternehmenscode erstellen

Sie müssen Umsatzsteuer-ID-Registrierungstypen für alle Länder oder Regionen erstellen, mit denen Ihr Unternehmen Geschäfte tätigt.

1. Navigieren Sie zu **Organisationsverwaltung** \> **Globales Adressbuch** \> **Erfassungstypen** \> **Erfassungstypen**.
2. Wählen Sie im Aktivitätsbereich die Option **Neu** aus, um einen Registrierungstyp für die USt-IdNr. zu erstellen.
3. Geben Sie im Dialogfeld **Details zu Registrierungstypen eingeben** im Feld **Name** einen Namen für den neuen Registrierungstyp ein. Geben Sie beispielsweise **USt-IdNr.** ein.
4. Geben Sie im Feld **Land/Region** das Land oder die Region des Handelspartners ein.
5. Wählen Sie **Erstellen** aus.

##### <a name="match-the-registration-type-with-a-registration-category"></a>Die Registrierungstyp mit einer Registrierungskategorie zuordnen

1. Navigieren zur **Organisationsverwaltung** \> **Globales Adressbuch** \> **Registrierungstypen** \> **Registration categories**.
2. Wählen Sie im Aktivitätsbereich **Neu** aus, um eine Verknüpfung zwischen eines Registrierungstypen und einer Registrierungskategorie zu erstellen.
3. Wählen Sie für den Registrierungstyp für die USt-IdNr. die Registrierungskategorie **USt-IdNr.**.
4. Wiederholen Sie die Schritte 2 und 3 für die anderen Registrierungstypen, die Sie für die Länder oder Regionen erstellt haben, mit denen Ihr Unternehmen Geschäfte tätigt.

##### <a name="set-up-the-vat-number-of-a-trading-partner"></a>Richten Sie die Umsatzsteuer-Identifikationsnummer eines Handelspartners ein

1. Wechseln Sie zu **Debitoren** \> **Debitoren** \> **Alle Debitoren**.
2. Wählen Sie im Raster einen Kunden aus.
3. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Debitor** in der Gruppe **Registrierung** auf **Registrierungs-ID**.
4. Wählen Sie auf dem FastTab **Registrierungs-ID** die Option **Hinzufügen** aus, um eine Registrierungs-ID zu erstellen.
5. Wählen Sie im Feld **Registrierungstyp** den Registrierungstypen aus, den Sie für den Unternehmenscode erstellt haben.
6. Geben Sie in das Feld **Registrierungsnummer** die MwSt.-Nummer des Unternehmens ein.
7. Wählen Sie im Aktivitätsbereich **Speichern**, und schließen Sie dann die Seite.

Weitere Informationen finden Sie unter [Registrierungs-IDs](emea-registration-ids.md).

### <a name="set-up-foreign-trade-parameters"></a>Außenhandelsparameter einrichten

1. Navigieren Sie zu **Steuer** \> **Einstellungen** \> **Außenhandel** \> **Außenhandelsparameter**.
2. Auf der **Intrastat** Registerkarte, auf dem Inforegistter **Elektronische Berichterstattung** im Feld **Dateiformatzuordnung** wählen Sie **Intrastat INTRACOM (FR)** oder **Intrastat SAISUNIC (FR)**.
3. Im Feld **Berichtformatzuordnung** **Intrastatbericht** auswählen.
4. Auf dem Inforegister **Warencodehierarchie** im Feld **Kategoriehierarchie** wählen Sie **Intrastat**.
5. Auf dem Inforegister **Allgemein** im Feld **Transaktions-Code** wählen Sie im Feld den Code aus, der für die Warenübertragung verwendet wird.
6. Im Feld **Gutschrift** wählen Sie im Feld den Code aus, der für die Warenrücksendung verwendet wird.
7. Wählen Sie im Feld **Arbeitskraft** den Namen der Kontaktperson für den Intrastat-Bericht aus.
8. Fügen Sie auf der Registerkarte **Kontakt** Informationen zur Kontaktperson hinzu:

    - Geben Sie im Feld **Telefon** die Telefonnummer des Ansprechpartners ein.
    - Geben Sie im Feld **Fax** die Faxnummer des Ansprechpartners ein.

9. Auf der Registerkarte **Länder-/Regionseigenschaften** führen Sie im Feld **Land/Region** alle Länder oder Regionen auf, mit denen Ihre Unternehmen Geschäfte macht. Wählen Sie für jedes Land, das Teil der EU ist, im Feld **Länder-/Regionsart** die Option **EU**, damit das Land in Ihrem Intrastat-Bericht erscheint. Wählen Sie für Frankreich im Feld **Länder-/Regionsart** die Option **Inland** aus.

### <a name="set-up-compression-of-intrastat"></a>Komprimierung von Intrastat einrichten

- Gehen Sie zu **Steuer** \> **Installieren** \> **Außenhandel** \> **Kompression von Intrastat**, und wählen Sie die Felder aus, die verglichen werden sollen, wenn Intrastat-Informationen zusammengefasst werden. Wählen Sie für das französische Intrastat die folgenden Felder aus:
 
    - Intrastat-Statistikverfahren
    - Herkunftsland/-region
    - Transport
    - Berichtigung
    - Land/Region
    - Landkreis für Ursprung/Ziel
    - Planungsrichtung
    - Land/Region des Absenders
    - Art des Geschäftes
    - Warencode

### <a name="set-up-product-parameters-for-the-intrastat-declaration"></a>Die Produktparameter für die Intrastat-Meldung festlegen

1. Wechseln Sie zu **Produktinformationsverwaltung** \> **Produkte** \> **Freigegebene Produkte**.
2. Wählen Sie im Raster ein Produkt aus.
3. Auf der Registerkarte **Außenhandel** Inforegister, im Abschnitt **Intrastat**, im Feld **Ware**, wählen Sie die Warennummer. Der Name der Ware wird im Feld **Beschreibung der Waren** im Intrastat-Bericht eingetragen.
4. Wählen Sie im Abschnitt **Ursprung** im Feld **Land/Region** das Ursprungsland oder die Ursprungsregion des Produkts aus.
5. Auf der Registerkarte **Lagerbestand verwalten** Inforegister, im Feld **Nettogewicht**, geben Sie das Gewicht des Produkts in Kilogramm ein.

### <a name="ngp-codes"></a>NGP-Codes

Im DEB-Bericht besteht die Kodifizierung von Produkten aus folgenden Elementen:

- Der achtstellige CN8-Code, der die zolltarifliche und statistische Nomenklatur der EU darstellt.
- Falls zutreffend, der einstellige nationale Artikelcode der Nomenclature Générale des Produits (NGP).

Im Jahr 2022 gilt der NGP nur für drei Arten von Produkten:

- Einige Produkte von Kühen, Schafen und Ziegen
- Militärische Ausrüstung
- Französische Weine

Sie müssen die NGP-Codes einrichten und sie verwandten Produkten zuweisen. Das **NGP** Feld wird dann automatisch auf der Seite **Intrastat-Journal** festgelegt.

#### <a name="set-up-an-ngp-code"></a>Richten Sie einen NGP-Code ein

1. Wechseln Sie zu **Steuer** \> **Einstellungen** \> **Außenhandel** \> **NGP-Codes**.
2. Wählen Sie im Aktivitätsbereich **Neu** aus.
3. Im **NGP** geben Sie einen einstelligen Code ein.
4. Geben Sie im Feld **Beschreibung** einen Beschreibung für den Code ein.

#### <a name="assign-an-ngp-code-to-a-product"></a>Zuweisen eines NGP-Codes zu einem Produkt

1. Wechseln Sie zu **Produktinformationsverwaltung** \> **Produkte** \> **Freigegebene Produkte**.
2. Wählen Sie im Raster ein Produkt aus.
3. Auf dem Inforegister **Außenhandel** im **Intrastat** Abschnitt, im Feld **NGP** wählen Sie den entsprechenden NGP-Code aus.

### <a name="set-up-warehouse-parameters-for-the-intrastat-declaration"></a>Die Lagerortparameter für die Intrastat-Meldung festlegen

1. Wechseln Sie zu **Lagerortverwaltung** \> **Einstellungen** \> **Lagerort** \> **Lagerorte**.
2. Wählen Sie ein Lager aus und wählen Sie dann auf dem Inforegister **Adressen** die Option **Hinzufügen** oder **Bearbeiten**.
3. Wählen Sie im Dialogfeld **Stadt** die Stadt des Lagerorts aus. Der Bundesstaat oder die Provinz der Stadt wird als Landkreis für Ihren DEB-Bericht verwendet.

### <a name="set-up-the-transport-method"></a>Die Transportmethode festlegen

1. Gehen Sie zu **Steuer** \> **Einrichutng** \> **Außenhandel** \> **Transportmethode**.
2. Wählen Sie im Aktivitätsbereich **Neu** aus.
3. Geben Sie im Feld **Transport** einen eindeutigen Wert ein. Französische Unternehmen verwenden einstellige Transportcodes.

### <a name="intrastat-journal"></a>Intrastat-Erfassungsfeld

Gehen Sie zu **Steuer** \> **Erklärungen** \> **Außenhandel** \> **Intrastat**, um Ihre Transaktionen zu verwalten, die für den Außenhandel mit EU-Ländern gelten. Weitere Informationen finden Sie unter [Intrastat Übersicht](emea-intrastat.md).

Die Spalte **NGP** ist spezifisch für Frankreich und zeigt den NGP-Code für das Produkt. Wenn der NGP nicht auf ein Produkt anwendbar ist, wir **0** (Null) angezeigt. Um den NGP-Code anzupassen, wählen Sie die Transaktion aus und dann auf der **Allgemein** Registerkarte, im **Codes** Abschnitt unter **NGP** wählen Sie im Feld den erforderlichen NGP-Code aus.

#### <a name="intrastat-transfer"></a>Intrastat-Übertragung

Auf der Seite **Intrastat** im Aktivitätsbereich können Sie **Überweisen** auswählen, um die Informationen über den innergemeinschaftlichen Handel aus Ihren Verkaufsaufträgen, Freitextrechnungen, Bestellungen, Lieferantenrechnungen, Lieferantenprodukteingängen, Projektrechnungen und Transferaufträgen automatisch zu übertragen. Es werden nur Dokumente übermittelt, die ein EU-Land als Bestimmungsland oder -Region (bei Versendungen) haben.

Da der DEB-Bericht eine Kombination aus der EU-Verkaufsliste und dem Intrastat-Bericht ist, enthält er auch *Dreiecks*-Transaktionen, bei denen eine direkte Lieferung von einem EU-Land (Partei A) in ein anderes EU-Land (Partei C) erfolgt und sich eine französische juristische Person (Partei B) mitten im Dreiecksgeschäft befindet.

#### <a name="generate-a-deb-intrastat-report"></a>Generieren eines DEB (Intrastat)-Berichts

1. Wechseln Sie zu **Steuer** \> **Meldungen** \> **Außenhandel** \> **Intrastat**.
2. Wählen Sie im Aktivitätsbereich **Ausgabe** \> **Bericht**.
3. Im angezeigten Dialogfeld **Intrastat-Bericht** legen Sie die folgenden Felder fest.

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

4. Wählen Sie **OK** aus, um das Dialogfeld **Intrastat-Bericht** zu schließen.
5. Im Dialogfeld **Elektronische Berichtsparameter** auf der Registerkarte **Parameter** im **Berichtsebene** wählen Sie die Berichtsebene aus. Die Berichtebene kann **1 - Statistikantwort**, **4 - Steuererklärung**, oder **5 - Statistikantwort auf Lieferung und Steuererklärung**.

## <a name="example"></a>Beispiel:

Das folgende Beispiel zeigt, wie Sie französisches Intrastat einrichten und den DEB-Bericht erstellen. Sie verwenden die **DEMF** juristische Person verwenden.

### <a name="preliminary-setup"></a>Vorläufige Einstellungen

1. In [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/Logon/Index), in der Bibliothek der freigegebenen Anlagen laden Sie die neuesten Versionen der Konfigurationen für die elektronische Berichterstattung (EB) für das Format der Intrastaterklärung herunter:

    - Intrastat-Modell
    - Intrastat-Bericht
    - Intrastat INTRACOM (FR)

2. Produktimporthierareinrichten:

    1. Wechseln Sie zu **Produktinformationsverwaltung** \> **Einrichtung** \> **Kategorien und Attribute** \> **Kategoriehierarchie**.
    2. Wählen Sie im Raster **Intrastat** aus.
    3. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Kategoriehierarchie** in der Gruppe **Verwalten** auf **Bearbeiten**.
    4. Klicken Sie im Aktivitätsbereich auf **Neuer Kategorieknoten**.
    5. Geben Sie im Feld **Name** **Autres Libournais** ein.
    6. Geben Sie im Feld **Code** **2204 21 42** ein.
    7. Wählen Sie im Aktionsbereich **Speichern** aus.

### <a name="set-up-vat-ids"></a>Einrichten der MwSt Kennungen

#### <a name="set-up-vat-codes-for-your-company"></a>Einrichten von MwSt.-Codes für Ihr Unternehmen

1. Gehen Sie zu **Steuer** \> **Einstellungen** \> **Mehrwertsteuer** \> **USt-IdNr.**.
2. Wählen Sie im Aktivitätsbereich **Neu** aus.
3. Wählen Sie im Feld **Land/Region** **FRA** aus.
4. Geben Sie im Feld **Steuerbefreiungsnummer** **MS123456** ein.
5. Gehen Sie zu **Organisationsverwaltung** \> **Organisation** \> **Juristische Entitäten**, und wählen Sie **DEMF**.
6. Auf dem Inforegister **Außenhandel und Logistik** im **Intrastat** Abschnitt, legen Sie die **Export der Umsatzsteuer-Identifikationsnummer** und **Einfuhrumsatzsteuer-Identifikationsnummer** Felder fest für den Code, den Sie in Schritt 4 erstellt haben.
7. Geben Sie im Inforegister **Steuerregistrierung** im Feld **Steuerregistrierungsnummer** **123456789** ein.

#### <a name="set-up-the-vat-ids-for-trading-partners"></a>USt-IdNr. für Handelspartner einrichten

##### <a name="create-a-registration-type-for-the-company-code"></a>Eine Registrierungsart für den Unternehmenscode erstellen

1. Navigieren Sie zu **Organisationsverwaltung** \> **Globales Adressbuch** \> **Erfassungstypen** \> **Erfassungstypen**.
2. Wählen Sie im Aktivitätsbereich die Option **Neu** aus, um einen Registrierungstyp für die USt-IdNr. zu erstellen.
3. Geben Sie im Dialogfeld **Details zu Registrierungstypen eingeben** im Feld **Name** **USt-IdNr.** ein.
4. Wählen Sie im Feld **Land/Region** **DEU** aus.
5. Wählen Sie **Erstellen** aus.

##### <a name="match-the-registration-type-with-a-registration-category"></a>Die Registrierungstyp mit einer Registrierungskategorie zuordnen

1. Navigieren zur **Organisationsverwaltung** \> **Globales Adressbuch** \> **Registrierungstypen** \> **Registration categories**.
2. Wählen Sie im Aktivitätsbereich **Neu** aus, um eine Verknüpfung zwischen des Registrierungstypen und der Registrierungskategorie zu erstellen.
3. Wählen Sie für den Registrierungstyp **USt-IdNr.** des Landes **DEU** die Registrierungskategorie **USt-IdNr.**.

##### <a name="set-up-the-customers-vat-registration-number"></a>MwSt. Registrierungsnummer des Debitors einrichten

1. Wechseln Sie zu **Debitoren** \> **Debitoren** \> **Alle Debitoren**.
2. Wählen Sie im Raster **DE-016** aus.
3. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Debitor** in der Gruppe **Registrierung** auf **Registrierungs-ID**.
4. Wählen Sie auf dem FastTab **Registrierungs-ID** die Option **Hinzufügen** aus, um eine Registrierungs-ID zu erstellen.
5. Wählen Sie im Feld **Registrierungstyp** **USt-IdNr.** aus.
6. Geben Sie in das Feld **Registrierungsnummer** **DE9012** ein.
7. Wählen Sie im Aktivitätsbereich **Speichern**, und schließen Sie dann die Seite.
8. Wählen Sie im **Rechnung und Lieferung**-Inforegister im Feld **Mehrwertsteuer** die **Umsatzsteuernummer** ausn und wählen Sie **DE9012**.

### <a name="set-up-foreign-trade-parameters"></a>Außenhandelsparameter einrichten

1. Navigieren Sie zu **Steuer** \> **Einstellungen** \> **Außenhandel** \> **Außenhandelsparameter**.
2. Auf der **Intrastat** Registerkarte, auf dem Inforegister **Allgemein** im **Transaktions-Code** Feld, wählen Sie **11**.
3. Auf dem Inforegister **Elektronische Berichterstattung** im **Dateiformatzuordnung** Feld, wählen Sie **Intrastat INTRACOM (FR)**.
4. Im Feld **Berichtformatzuordnung** **Intrastatbericht** auswählen.
5. Auf dem Inforegister **Warencodehierarchie** im Feld **Kategoriehierarchie** wählen Sie **Intrastat**.
6. Wählen Sie im Feld **Arbeitskraft** einen Datensatz aus.
7. Geben Sie in der Registerkarte **Kontakt** im Feld **Telefon** die Telefonnummer des Kontakts ein
8. Geben Sie im Feld **Fax** die Faxnummer des Kontakts ein.

### <a name="create-ngp-code"></a>Erstellen eines NGP-Codes

1. Wechseln Sie zu **Steuer** \> **Einstellungen** \> **Außenhandel** \> **NGP-Codes**.
2. Wählen Sie im Aktivitätsbereich **Neu** aus.
3. Geben Sie im Feld **NGP** den Wert **8** ein.
4. Geben Sie im Feld **Name eine Beschreibung** **NGP 8** ein.
5. Wählen Sie im Aktionsbereich **Speichern** aus.

### <a name="set-up-product-information"></a>Produktinformation festlegen

1. Wechseln Sie zu **Produktinformationsverwaltung** \> **Produkte** \> **Freigegebene Produkte**.
2. Wählen Sie im Raster **D0001** aus.
3. Auf der Seite **Außenhandel** Inforegister, im Abschnitt **Intrastat**, im Feld **NGP**, wählen Sie **8**.
4. Geben Sie im Feld **Ware** ein und wählen Sie **2204 21 42**.
5. Wählen Sie im Abschnitt **Herkunft** im Feld **Land/Region** **FRA** aus.
6. Wählen Sie im Inforegister **Bestand verwalten** im Abschnitt **Gewichtsmessungen** im Feld **Nettogewicht** **2** ein.
7. Wählen Sie im Aktivitätsbereich **Speichern**, und schließen Sie dann die Seite.
8. Wählen Sie im Raster **D0003** aus.
9. Auf dem Inforegister **Außenhandel** wählen Sie im Abschnitt **Intrastat** im Feld **Ware** **100 200 30** aus.
10. Wählen Sie im Abschnitt **Herkunft** im Feld **Land/Region** **DEU** aus.
11. Wählen Sie im Inforegister **Bestand verwalten** im Abschnitt **Gewichtsmessungen** im Feld **Nettogewicht** **5** ein.
12. Wählen Sie im Aktionsbereich **Speichern** aus.

### <a name="set-up-regime-codes"></a>Richten Sie Regime-Codes ein.

1. Wechseln Sie zu **Steuer** \> **Einstellungen** \> **Außenhandel** \> **Statistikverfahren**.
2. Wählen Sie im Aktivitätsbereich **Neu** aus.
3. Geben Sie im Feld **Statistikverfahren** **21** ein.
4. Geben Sie in das Feld **Text 1** **Regime-Code 21** ein.

### <a name="change-the-site-address"></a>Ändern Sie die Standortadresse

1. Wechseln Sie zu **Lagerortverwaltung** \> **Einstellungen** \> **Lagerort** \> **Sites**.
2. Wählen Sie im Raster **1** aus.
3. Wählen Sie auf der Inforegisterkarte **Adressen** die Option **Bearbeiten**.
4. Wählen Sie im Dialogfeld **Adresse bearbeiten** im Feld **Land/Region** die Option **FRA**.
5. Wählen Sie **OK** aus.
6. Gehen Sie zu **Warehouse Management** \> **Installieren** \> **Lagerhaus** \> **Lager**, und wählen Sie ein Lager aus.
7. Wählen Sie auf dem Inforegister **Adressen** die Option **Hinzufügen**.
8. Wählen Sie im Dialogfeld **Neue Adresse** im Feld **Land/Region** die Option **FRA**.
9. Wählen Sie im Feld **Stadt** **Bordeaux**.
10. Klicken Sie auf **OK**, um das Dialogfeld zu schließen.

### <a name="set-up-a-transport-method"></a>Eine Transportmethode festlegen

1. Gehen Sie zu **Steuer** \> **Einrichutng** \> **Außenhandel** \> **Transportmethode**.
2. Wählen Sie im Aktivitätsbereich **Neu** aus.
3. Geben Sie im Feld **Transport** den Wert **3** ein.
4. Geben Sie im Feld **Beschreibung** **Straßentransport** ein.

### <a name="assign-a-transport-mode-to-a-mode-of-delivery"></a>Ordnen Sie einem Liefermodus eine Transportart zu.

1. Gehen Sie zu **Beschaffung** \> **Einstellungen** \> **Vertrieb** \> **Liefermodus**.
2. Wählen Sie im Raster **50** aus.
3. Wählen Sie auf dem Inforegister **Außenhandel** im Feld **Transport** die Option **3** aus.

### <a name="create-a-sales-order-with-an-eu-customer-that-includes-the-new-product"></a>Erstellen Sie einen Kundenauftrag mit einem EU-Kunden, der das neue Produkt enthält

1. Wechseln Sie zu **Debitoren** \> **Aufträge** \> **Alle Aufträge**.
2. Wählen Sie im Aktivitätsbereich **Neu** aus.
3. Im Dialogfeld **Verkaufsauftrag erstellen** im Abschnitt **Kunde** im Feld **Kundenkonto** wählen Sie **DE-016**.
4. Im **Adresse** Abschnitt, im Feld **Lieferadresse** wählen Sie das Pluszeichen (**+**), um eine Adresse zu erstellen.
5. Geben Sie im **Neue Adresse**-Dialogfeld im Feld **Name Funktionsbeschreibung** **Deutschland** ein.
6. Wählen Sie im Feld **Land/Region** **DEU** aus.
7. Wählen Sie **OK** aus.
8. Wählen Sie im Dialogfeld  **Neuen Auftrag erstellen** und dann **OK** aus.
9. Im Inforegister **Verkaufspositionen** im Feld **Artikelnummer** wählen Sie **0001**.
10. Wählen Sie auf dem Inforegister **Positionsdetails** auf der Registerkarte **Außenhandel** im Feld **Statistikverfahren** **21** aus.
11. Wählen Sie im Feld **Herkunftslandkreis** **AL**.
12. Wählen Sie im Aktionsbereich **Speichern** aus.
13. Auf der Registerkarte **Kopfzeile** im Inforegister **Lieferung** im Feld **Lieferart** stellen Sie sicher, dass **50** ausgewählt ist.
14. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Rechnung** in der Gruppe **Generieren** **Rechnung** aus.
15. Im **Rechnung buchen** Dialogfeld, auf dem **Parameter** Inforegiser im **Parameter** Abschnitt, im **Menge** Feld, wählen Sie **Alle**. Wählen Sie **OK** um die Rechnung zu buchen.

### <a name="transfer-the-transaction-to-the-intrastat-journal-and-review-the-result"></a>Übertragen Sie die Transaktion in das Intrastat-Buch.-Blatt und überprüfen Sie das Ergebnis

1. Wechseln Sie zu **Steuer** \> **Meldungen** \> **Außenhandel** \> **Intrastat**.
2. Wählen Sie im Aktivitätsbereich **Übertragung**.
3. Im **Intrastat (Übertragung)** Dialogfeld, im **Parameter** Abschnitt, legen Sie die **Kundenrechnung** Option auf **Ja** fest. Wählen Sie dann **OK** aus.
4. Transaktionen nach **Datum** Feld sortieren. Die oberste Transaktion ist die Ergebnistransaktion.

    ![Position, die den Auftrag auf der Intrastat-Seite darstellt.](media/intrastat_fr_1.png)

5. Wählen Sie die Transaktionsposition aus, und wählen Sie dann die Registerkarte **Allgemein**, um weitere Details anzuzeigen.

    ![Auftragsdetails auf der Registerkarte „Allgemein“ der Intrastat-Seite.](media/intrastat_fr_2.png)

6. Wählen Sie im Aktivitätsbereich **Ausgabe** \> **Bericht**.
7. Im **Intrastat-Bericht** Dialogfeld, auf dem Inforegister **Parameter** im Abschnitt **Datum** wählen Sie im Abschnitt den Monat des von Ihnen erstellten Kundenauftrags aus.
8. Im Abschnitt **Exportoptionen** legen Sie die **Datei generieren** Option auf **Ja** fest.
9. Geben Sie im Feld **Dateiname** den erforderlichen Namen ein.
10. Wählen Sie **OK** aus, um das Dialogfeld **Intrastat-Bericht** zu schließen.
11. Im Dialogfeld **Elektronische Berichtsparameter** im Inforegister **Parametes** im Feld **Berichtsebene** wählen Sie **5 - Statistikantwort auf Lieferung und Steuererklärung**, und den Bericht prüfen.

    ![Intrastat-Intracom-Bericht über Sendungen.](media/intrastat_fr_3.png)

12. Prüfen Sie den generierten Excel-Bericht.

    ![Intrastat-Bericht über Sendungen.](media/intrastat_fr_4.png)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
