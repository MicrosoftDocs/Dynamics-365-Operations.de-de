---
title: Deutsche Intrastat
description: Dieser Artikel enthält Informationen zur Intrastat-Meldung in Deutschland.
author: AdamTrukawka
ms.date: 09/09/2021
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: ''
ms.openlocfilehash: ae978b28098d92d84415c29bbe76157144f862d8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269433"
---
# <a name="german-intrastat"></a>Deutsche Intrastat

[!include [banner](../includes/banner.md)]

Die **Intrastaz** Seite wird verwendet, um Informationen zum Handel zwischen EU-Ländern/Regionen generieren und melden. Die deutsche Intrastat-Meldung enthält meldepflichtige Informationen über den Warenverkehr. Der Bericht ist nach den Richtlinien der deutschen Behörden formatiert, die auf der Seite [6.2 Dateierklärungen im INSTAT/XML-Format](https://www-idev.destatis.de/idev/doc/intra_en/hilfe6_2.html) dargestellt sind.

Die folgende Tabelle zeigt die Felder, die in der deutschen Intrastat-Meldung enthalten sind.

| Felder | Versand | Empfang |
|-------------------------|-------------------------|-------------------------|
| Referenzzeitraum | X | X |
| Richtungscode | X | X |
| Währung der Intrastat-Meldung</br>**Hinweis:** Diese Währung entspricht der <em>Buchhaltungswährung</em>. | X | X |
| Warencode | X | X |
| Warenname | X | X |
| Code der zusätzlichen Einheit | X | X |
| Mitgliedstaat der Sendung/Lieferung | X | X |
| Nettomasse | X | X |
| Quantität in den zusätzlichen Einheiten | X | X |
| Ursprungsland |  | X |
| Rechnungsbetrag | X |  |
| Statistischer Wert | X | X |
| Art der Transaktionen | X | X |
| Transportmodus | X | X |
| Regionscode</br>**Hinweis:**</br><ul></br><li>Wenn das Herkunftsland oder die Herkunftsregion Deutschland ist und die Rechnung sich auf Versendungen bezieht, wird ein Intrastat-Code für das Herkunftsland angezeigt.</li></br><li>Wenn das Herkunftsland oder die Herkunftsregion nicht Deutschland ist und die Rechnung sich auf Versendungen bezieht, wird der Code **99** gezeigt.</li></br><li>Wenn sich die Rechnung auf Wareneingänge bezieht, wird ein Intrastat-Code für den Staat angezeigt.</li></br></ul> | X | X |
| Hafen-/Flughafen-/Binnenhafencode | X | X |
| Lieferbedingungen | X | X |


## <a name="set-up-intrastat"></a>Einrichten von Intrastat

1. Richten Sie die Unternehmenscodes ein.

    1. Gehen Sie zu **Organisationsverwaltung** > **Organisationen** > **Juristische Personen**.
    2. Geben Sie im Inforegister **Außenhandel und Logistik** im Abschnitt **Kennung** im Feld **DVR** die ID der Austauschvereinbarung ein. Diese ID wird im Bericht enthalten sein.
    3. Im Feld **MwSt.-Nummer – Export** geben Sie die Mehrwertsteuernummer (MwST.-Nummer) Ihres Unternehmens für den Export ein.
    4. Im Feld **MwSt.-Nummer – Import** geben Sie die Mehrwertsteuernummer (MwST.-Nummer) Ihres Unternehmens für den Import ein.
    5. Im Feld **Intrastat-Code** geben Sie den Intrastat-Code ein, der der juristischen Person zugeordnet ist.
    6. Geben Sie im **Steuerregistrierung**-Inforegister im Feld **Steuernummer** die Steuernummer für Ihr Unternehmen an.

    > [!NOTE]
    > Wenn Sie einen Intrastat-Bericht für verbundene Unternehmen erstellen, geben Sie im Feld **Steuernummer** die Steuernummer Ihrer Muttergesellschaft ein.

2. Laden Sie in [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) in der Bibliothek der freigegebenen Anlagen die neuesten Versionen der Konfigurationen für die elektronische Berichterstellung (EB) für die Intrastat-Meldung herunter.

    - Intrastat-Modell
    - Intrastat-Bericht
    - INSTAT-XML
    - INSTAT-XML (DE)

3. Außenhandelsparameter einrichten:

    1. Gehen Sie in Dynamics 365 Finance zu **Steuern** > **Einrichtung** > **Außenhandelsparameter**.
    2. Wählen Sie auf der Registerkarte **Intrastat** im Inforegister **Elektronische Berichterstattung** im Feld **Dateiformatzuordnung** **Intrastat-XML (DE)** aus.
    3. Im Feld **Berichtformatzuordnung** **Intrastatbericht** auswählen.
    4. Auf dem Inforegister **Warencodehierarchie** im Feld **Kategoriehierarchie** wählen Sie **Intrastat**.
    5. Wählen Sie im Feld **Art des Geschäfts** die Art des Geschäfts für Eigentumsübertragungen aus. Sie verwenden diesen Code für Transaktionen, die zu tatsächlichen oder geplanten Eigentumsübertragung gegen eine (finanzielle oder anderweitige) Entschädigung führen. Sie verwenden ihn auch für Korrekturen.
    6. Wählen Sie im Feld **Gutschrift** die Art des Geschäfts für die Warenrücksendung aus.
    7. Wählen Sie im Feld **Arbeitskraft** die Kontaktperson für den Intrastat-Bericht aus. Geben Sie alternativ auf der Registerkarte **Kontakt** in den Feldern **Name**, **Telefon**, **Fax**, **E-Mail** und **Internetadresse** Werte ein oder wählen Sie sie aus. Diese Felder sind im Bericht enthalten.
    8. Wählen Sie im Feld **Behörde** die Intrastat-Behörde aus.
    9. Gehen Sie zu **Steuer** > **Indirekte Steuern** > **Mehrwertsteuer** > **Mehrwertsteuerbehörden**, und geben Sie die folgenden Informationen für die Intrastat-Behörde ein, die Sie im vorherigen Schritt ausgewählt haben:

       - Nummer des Finanzamtes
       - Adresse
       - Kontaktinformationen

    10. Auf der Registerkarte **Länder-/Regionseigenschaften** führen Sie im Feld **Land/Region** alle Länder oder Regionen auf, mit denen Ihre Unternehmen Geschäfte macht. Für jedes Land oder jede Region wählen Sie im Feld **Land-/Regionsart** **EU** aus, damit das Land oder die Region in Ihrem Intrastat-Bericht erscheint.

4. Richten Sie Regionscodes ein.

    1. Gehen Sie zu **Organisationsverwaltung** > **Globales Adressbuch** > **Adressen** > **Adresseinstellungen**.
    2. Wählen Sie auf der Registerkarte **Bundesland/Kanton** im Feld **Land/Region** **DEU** und dann **Filter anwenden** aus.
    3. Wählen Sie im Raster das Bundesland aus. Geben Sie im Feld **Intrastat-Code** den einzigartigen Intrastat-Code ein.

5. Richten Sie die Ursprungsadresse für ein Produkt ein.

    1. Wechseln Sie zu **Produktinformationsverwaltung** > **Produkte** > **Freigegebene Produkte** aus.
    2. Wählen Sie im Raster das Produkt aus.
    3. Auf dem Inforegister **Außenhandel** wählen Sie im Abschnitt **Intrastat** im Feld **Ursprungsland** **DEU** aus.

6. Gehen Sie zu **Steuer** > **Einstellungen** > **Außenhandel** > **Komprimierung von Intrastat** und wählen Sie die Felder aus, die verglichen werden sollen, wenn Intrastat-Informationen zusammengefasst werden. Wählen Sie für das deutsche Intrastat die folgenden Felder aus:

    - Warencode
    - Land/Region
    - Berichtigung
    - Planungsrichtung
    - Lieferbedingungen
    - Rechnung
    - Herkunftsland/-region
    - Port
    - Land/Region des Absenders
    - Bundesland des Absenders
    - Statistikverfahren
    - Art des Geschäftes
    - Transport
    - Steuerbefreiungsnummer

### <a name="intrastat-transfer"></a>Intrastat-Übertragung

Auf der Seite **Intrastat** wählen Sie im Aktivitätsbereich **Übertragung** auswählen, um die Informationen über den innergemeinschaftlichen Handel aus Ihren Aufträgen, Freitextrechnungen, Bestellungen, Kreditorenrechnungen, Kreditorproduktzugänge **,** Projektrechnungen und Umlagerungsauftrag. Es werden nur Dokumente übermittelt, die ein EU-Land als Bestimmungsland oder -Region (bei Versendungen) haben.

Alternativ können Sie Transaktionen manuell eingeben, indem Sie **Neu** im Aktionsbereich auswählen.

### <a name="generate-an-intrastat-report"></a>Generieren eines Intrastat-Berichts

1. Wechseln Sie zu **Steuer** > **Meldungen** > **Außenhandel** > **Intrastat**.
2. Wählen Sie im Aktivitätsbereich **Ausgabe** > **Bericht**.
3. Im angezeigten Dialogfeld **Intrastat-Bericht** legen Sie die folgenden Felder fest.

    | Feld | Beschreibung |
    |-------------------------|-------------------------|
    | Anfangsdatum | Wählen Sie das Startdatum für den Bericht. |
    | Bis-Datum | Wählen Sie das Enddatum für den Bericht. |
    | Datei generieren | Legen Sie diese Option auf **Ja** fest, um eine .xml-Datei zu generieren. |
    | Dateiname | Lassen Sie dieses Feld leer. Der Dateiname wird automatisch generiert und besteht aus dem Wert des **&lt;Umschlag-ID&gt;** XML-Tag plus die Dateinamenerweiterung **.xml**.</br>Der Wert **&lt;Umschlag-ID&gt;** ist eine Verkettung der folgenden Elemente in dieser Reihenfolge:</br><ol type="1"></br><li>Dem Wert des **&lt;Austauschvereinbarungs-ID&gt;**-Tag</li></br><li>Einem Bindestrich (-)</li></br><li>Dem Wert des **&lt;Referenzzeitraum in JJJJMM&gt;**-Tag</li></br><li>Einem Bindestrich (-)</li></br><li>Dem Wert des **&lt;Umschlag/Datetime/Datum in JJJJMMTT&gt;**-Tag</li></br><li>Einem Bindestrich (-)</li></br><li>Dem Wert des **&lt;Umschlag/Datetime/Zeit in hhmm&gt;**-Tag</li></br></ol> |
    | Planungsrichtung | <ul></br><li>Wählen Sie **Eingang** für einen Bericht über innergemeinschaftliche Eingänge aus.</li></br><li>Wählen Sie **Versand** für einen Bericht über innergemeinschaftliche Versendungen aus.</li></br><li>Wählen Sie **Beide** für einen Bericht über innergemeinschaftliche Versendungen und Eingänge aus.</li></br></ul> |
    | Steuernummer | Geben Sie die Registrierungsnummer ein, die zur Generierung des Kennungscodes des Absenders verwendet werden soll, wenn die Nummer von der Steuernummer der juristischen Person abweicht. |


## <a name="example"></a>Beispiel

Dieses Beispiel zeigt, wie Sie Eingänge und Versendungen für Intrastat buchen. Sie verwenden die **DEMF** juristische Person verwenden.

1. Laden Sie in [LCS](https://lcs.dynamics.com/Logon/Index) in der Bibliothek der freigegebenen Anlagen die neuesten Versionen der folgenden EB-Konfigurationen für das Format der Intrastat-Meldung herunter:

    - Intrastat-Modell
    - Intrastat-Bericht
    - Intrastat-XML
    - Intrastat-XML (DE)

2. Erstellen Sie die Arten des Geschäfts.

    1. Wechseln Sie zu **Steuer** > **Einstellungen** > **Außenhandel** > **Art des Geschäfts**.
    2. Wählen Sie im Aktivitätsbereich **Neu** aus.
    3. Geben Sie im Feld **Art** **des Geschäfts** **21** ein.
    4. Geben Sie im Feld **Name** **Warenrücksendung** ein.
    5. Wählen Sie im Aktionsbereich **Speichern** aus.

3. Richten Sie die Kennungsnummer der Behörde ein.

    1. Gehen Sie zu **Steuer** > **Indirekte Steuern** > **Mehrwertsteuer** > **Mehrwertsteuerbehörden**.
    2. Wählen Sie in der Liste **TA** aus.
    3. Geben Sie im Feld **Finanzamtnummer** **123** ein.

4. Richten Sie Regionscodes ein.

    1. Gehen Sie zu **Organisationsverwaltung** > **Globales Adressbuch** > **Adressen** > **Adresseinstellungen**.
    2. Wählen Sie auf der Registerkarte **Bundesland/Kanton** im Feld **Land/Region** **DEU** und dann **Filter anwenden** aus.
    3. Wählen Sie im Raster **BE** und dann im Feld **Intrastat-Code** **11** ein.
    4. Wählen Sie im Aktionsbereich **Speichern** aus.

5. Richten Sie Außenhandelsparameter ein.

    1. Gehen Sie zu **Steuer** > **Einstellungen** > **Außenhandel** > **Außenhandelsparameter**.
    2. Auf der Registerkarte **Intrastat** wählen Sie auf dem Inforegister **Allgemein** im Feld **Art** **des Geschäfts** **11** aus.
    3. Wählen Sie im Feld **Gutschrift** **21** aus.
    4. Wählen Sie im Feld **Behörde** **TA** aus.
    5. Wählen Sie auf dem Inforegister **Elektronische Berichterstellung** im Feld **Dateiformatzuordnung** **INSTAT-XML (DE)** aus.
    6. Wählen Sie im Feld **Berichtformatzuordnung** **Intrastatbericht** aus.
    7. Gehen Sie sicher, dass Sie im Inforegister **Warencodehierarchie** im Feld **Kategoriehierarchie** **Intrastat** auswählen.
    8. Wählen Sie auf der Registerkarte **Länder-/Regionseigenschaften** **Neu** aus.
    9. Wählen Sie im Feld **Land/Region der Partei** **FRA** aus.
    10. Wählen Sie im Feld **Länder-/Regionsart** die Option **EU** aus.

6. Weisen Sie einem Produkt einen Warencode zu und legen Sie den Ursprung des Produkts fest. Die Felder **Warencode**, **Herkunftsland/-region** und **Herkunfts-Bundesland** werden auf Aufträgen und Bestellungen automatisch festgelegt, wenn Sie das Produkt auswählen.

    1. Wechseln Sie zu **Produktinformationsverwaltung** > **Produkte** > **Freigegebene Produkte** aus.
    2. Wählen Sie im Raster **D0001** aus.
    3. Auf dem Inforegister **Außenhandel** wählen Sie im Abschnitt **Intrastat** im Feld **Ware** **920 20 34** aus.
    4. Wählen Sie im Abschnitt **Herkunft** im Feld **Land/Region** **DEU** aus.
    5. Wählen Sie im Inforegister **Bestand verwalten** im Abschnitt **Gewichtsmessungen** im Feld **Nettogewicht** **12** ein.
    6. Wählen Sie im Aktionsbereich **Speichern** aus.

7. Ordnen Sie einem Liefermodus den Transport zu. Der Transportcode wird dann automatisch für Bestellungen gesetzt, wenn Sie den Liefermodus auswählen.

    1. Gehen Sie zu **Beschaffung** > **Einstellungen** > **Vertrieb** > **Liefermodus**.
    2. Wählen Sie in der Liste **10** aus.
    3. Wählen Sie auf dem Inforegister **Außenhandel** im Feld **Transport** die Option **01** aus.

8. Erstellen Sie einen Auftrag mit einem EU-Kunden.

    1. Gehen Sie zu **Debitoren** > **Aufträge** > **Alle Aufträge**.
    2. Wählen Sie im Aktivitätsbereich **Neu** aus.
    3. Wählen Sie im Dialogfeld **Auftrag erstellen** im Inforegister **Debitor** im Abschnitt **Debitor** im Feld **Debitorenkonto** **DE-012** aus.
    4. Wählen Sie im Inforegister **Allgemein** im Abschnitt **Lagerdimensionen** im Feld **Standort** **1**.
    5. Im Feld **Lagerort** wählen Sie **11** aus.
    6. Wählen Sie **OK** aus.
    7. Wählen Sie auf der Registerkarte **Kopfzeile** im Inforegister **Außenhandel** im Feld **Hafen** die Option **53** aus.
    8. Wählen Sie im Feld **Statistikverfahren** **31710** aus.
    9.  Wählen Sie in der Registerkarte **Positionen** im Inforegister **Auftragspositionen** im Feld **Artikelnummer** **D0001** aus. Geben Sie dann im Feld **Menge** den Wert **10** ein.
    10. Vergewissern Sie sicher, dass im Inforegister **Positionsdetails** in der Registerkarte **Außenhandel** die Felder **Art des Geschäfts**, **Transport**, **Ware** und **Herkunftsland/-region** automatisch gesetzt sind.
    11. Wählen Sie im Aktionsbereich **Speichern** aus.
    12. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Rechnung** im Abschnitt **Generieren** **Rechnung** aus.
    13. Im **Rechnung buchen** Dialogfeld, auf dem **Parameter** Inforegiser im **Parameter** Abschnitt, im **Menge** Feld, wählen Sie **Alle**.
    14. Klicken Sie auf **OK**, um die Rechnung zu buchen.

9.  Übertragen Sie die Transaktion in das Intrastat-Buch.-Blatt und überprüfen Sie das Ergebnis.

    1. Wechseln Sie zu **Steuer** > **Meldungen** > **Außenhandel** > **Intrastat**.
    2. Wählen Sie im Aktivitätsbereich **Übertragung**.
    3. Im **Intrastat (Übertragung)** Dialogfeld, im **Parameter** Abschnitt, legen Sie die **Kundenrechnung** Option auf **Ja** fest.
    4. Wählen Sie **Filter** aus.
    5. Wählen Sie im Dialogfeld **Intrastat-Filter** in der Registerkarte **Bereich** die erste Zeile aus und vergewissern Sie sich, dass das Feld **Feld** auf **Datum** gesetzt ist.
    6. Wählen Sie im Feld **Kriterien** das aktuelle Datum aus.
    7. Wählen Sie **OK** aus, um das Dialogfeld **Intrastat-Filter** zu schließen.
    8. Wählen Sie **OK**, um das Dialogfeld **Intrastat (Übertragung)** zu schließen und überprüfen Sie das Ergebnis. Die Position stellt den Auftrag dar, den Sie früher erstellt haben.

        ![Position, die den Auftrag auf der Intrastat-Seite darstellt](media/intrastat_deu_1.png)

10. Wählen Sie die Transaktionsposition aus, und wählen Sie dann die Registerkarte **Allgemein**, um weitere Details anzuzeigen.

    ![Auftragsdetails auf der Registerkarte „Allgemein“ der Intrastat-Seite](media/intrastat_deu_2.png)

11. Erstellen Sie eine Gutschrift mithilfe eines Auftrags.

    1. Gehen Sie zu **Debitoren** > **Aufträge** > **Alle Aufträge**.
    2. Wählen Sie im Aktivitätsbereich **Neu** aus.
    3. Wählen Sie im Dialogfeld **Auftrag erstellen** im Inforegister **Debitor** im Abschnitt **Debitor** im Feld **Debitorenkonto** **DE-012** aus.
    4. Wählen Sie im Inforegister **Allgemein** im Abschnitt **Lagerdimensionen** im Feld **Standort** **1**.
    5. Im Feld **Lagerort** wählen Sie **11** aus.
    6. Wählen Sie auf der Registerkarte **Kopfzeile** im Inforegister **Außenhandel** im Feld **Hafen** die Option **53** aus.
    7. Wählen Sie im Feld **Statistikverfahren** **31710** aus.
    8. Wählen Sie in der Registerkarte **Positionen** im Inforegister **Auftragspositionen** im Feld **Artikelnummer** **D0001** aus. Geben Sie dann im Feld **Menge** den Wert **-2** ein.
    9. Wählen Sie auf dem Inforegister **Positionsdetails** auf der Registerkarte **Außenhandel** im Feld **Art des Geschäfts** **21** aus.
    10. Stellen Sie sicher, dass die Felder **Transport**, **Ware** und **Herkunftsland/-region** automatisch gesetzt werden.
    11. Wählen Sie im Aktionsbereich **Speichern** aus.
    12. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Rechnung** im Abschnitt **Generieren** **Rechnung** aus.
    13. Im **Rechnung buchen** Dialogfeld, auf dem **Parameter** Inforegiser im **Parameter** Abschnitt, im **Menge** Feld, wählen Sie **Alle**.
    14. Klicken Sie auf **OK**, um die Rechnung zu buchen.

12. Übertragen Sie die Transaktion in das Intrastat-Buch.-Blatt und überprüfen Sie das Ergebnis.

    1. Wechseln Sie zu **Steuer** > **Meldungen** > **Außenhandel** > **Intrastat**.
    2. Wählen Sie im Aktivitätsbereich **Übertragung**.
    3. Im **Intrastat (Übertragung)** Dialogfeld, im **Parameter** Abschnitt, legen Sie die **Kundenrechnung** Option auf **Ja** fest.
    4. Wählen Sie **OK**, um das Dialogfeld **Intrastat (Übertragung)** zu schließen und überprüfen Sie das Ergebnis. Eine neue Position, in der das Feld **Richtung** auf **Eingänge** gesetzt wurde, wurde hinzugefügt.            
        Diese Position stellt die physische Warenrücksendung dar.

        ![Position für die physische Warenrücksendung auf der Intrastat-Seite](media/intrastat_deu_3.png)

13. Wählen Sie die Transaktionsposition aus, und wählen Sie dann die Registerkarte **Allgemein**, um weitere Details anzuzeigen.

    ![Details zur physischen Warenrücksendung auf der Registerkarte „Allgemein“ der Intrastat-Seite](media/intrastat_deu_4.png)

14. Erstellen Sie eine Korrektur mithilfe eines Auftrags:

    1. Gehen Sie zu **Debitoren** > **Aufträge** > **Alle Aufträge**.
    2. Wählen Sie im Aktivitätsbereich **Neu** aus.
    3. Wählen Sie im Dialogfeld **Auftrag erstellen** im Inforegister **Debitor** im Abschnitt **Debitor** im Feld **Debitorenkonto** **DE-012** aus.
    4. Wählen Sie im Inforegister **Allgemein** im Abschnitt **Lagerdimensionen** im Feld **Standort** **1**.
    5. Im Feld **Lagerort** wählen Sie **11** aus.
    6. Wählen Sie auf der Registerkarte **Kopfzeile** im Inforegister **Außenhandel** im Feld **Hafen** die Option **53** aus.
    7. Wählen Sie im Feld **Statistikverfahren** **31710** aus.
    8. Wählen Sie in der Registerkarte **Positionen** im Inforegister **Auftragspositionen** im Feld **Artikelnummer** **D0001** aus. Geben Sie dann im Feld **Menge** den Wert **-3** ein.
    9. Wählen Sie auf dem Inforegister **Positionsdetails** auf der Registerkarte **Außenhandel** im Feld **Art des Geschäfts** **11** aus.
    10. Stellen Sie sicher, dass die Felder **Transport**, **Ware** und **Herkunftsland/-region** automatisch gesetzt werden.
    11. Wählen Sie im Aktionsbereich **Speichern** aus.
    12. Stellen Sie sicher, dass das Feld **Art des Geschäfts** auf 11 gesetzt ist.
    13. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Rechnung** im Abschnitt **Generieren** **Rechnung** aus.
    14. Im **Rechnung buchen** Dialogfeld, auf dem **Parameter** Inforegiser im **Parameter** Abschnitt, im **Menge** Feld, wählen Sie **Alle**.
    15. Klicken Sie auf **OK**, um die Rechnung zu buchen.

15. Übertragen Sie die Transaktion in das Intrastat-Buch.-Blatt und überprüfen Sie das Ergebnis:

    1. Wechseln Sie zu **Steuer** > **Meldungen** > **Außenhandel** > **Intrastat**.
    2. Wählen Sie im Aktivitätsbereich **Übertragung**.
    3. Im **Intrastat (Übertragung)** Dialogfeld, im **Parameter** Abschnitt, legen Sie die **Kundenrechnung** Option auf **Ja** fest.
    4. Wählen Sie **OK**, um das Dialogfeld **Intrastat (Übertragung)** zu schließen und überprüfen Sie das Ergebnis. Eine neue Position mit einem Häkchen in der Spalte **Korrektur** wurde hinzugefügt.

        ![Position für die Korrektur auf der Intrastat-Seite](media/intrastat_deu_5.png)

16. Wählen Sie die Transaktionsposition aus, und wählen Sie dann die Registerkarte **Allgemein**, um weitere Details anzuzeigen.

    ![Details der Korrektur auf der Registerkarte „Allgemein“ der Intrastat-Seite](media/intrastat_deu_6.png)

17. Wählen Sie im Aktivitätsbereich **Ausgabe** > **Bericht**.
18. Im **Intrastat-Bericht** Dialogfeld, auf dem Inforegister **Parameter** im Abschnitt **Datum** wählen Sie im Abschnitt den Monat des von Ihnen erstellten Kundenauftrags aus.
19. Im Abschnitt **Exportoptionen** legen Sie die Option **Generieren** auf **Ja** fest.
20. Geben Sie im Feld **Dateiname** den erforderlichen Namen ein.
21. Wählen Sie **OK** aus und überprüfen Sie den generierten Bericht. Die folgende Tabelle zeigt die Werte in dem Beispielbericht.

    | **Name**                  | **Verkaufsrechnung**  |   **Berichtigung**   | **Gutschrift** |
    |---------------------------|--------------------|--------------------|-----------------|
    | declarationId             | 2021-07-D          | 2021-07-A          |                 |
    | referencePeriod           | 2021-07            | 2021-07            |                 |
    | PSIId                     | 11203/118/12345000 | 11203/118/12345000 |                 |
    | functionCode              | O                  | O                  |                 |
    | flowCode                  | S                  | K                  |                 |
    | CurrencyCode              | EUR                | EUR                |                 |
    | itemNumber                | 0000362            | 0000362            | 0000361         |
    | CN8Code                   | 9202034            | 9202034            | 9202034         |
    | goodsDescription          | Lautsprecher            | Lautsprecher            | Lautsprecher         |
    | MSConsDestCode            | FR                 | FR                 | FR              |
    | countryOfOriginCode       | \-                 | \-                 | DE              |
    | netMass                   | 120                | -36                | 24              |
    | invoicedAmount            | 3290               | -987               | \-              |
    | StatisticalValue          | 3290               | -987               | 658             |
    | natureOfTransactionACode  | 1                  | 1                  | 2               |
    | natureOfTransactionBCode  | 1                  | 1                  | 1               |
    | modeOfTransportCode       | 01                 | 01                 | 01              |
    | regionCode                | 11                 | 11                 | 11              |
    | portAirportInlandportCode | 53                 | 53                 | 53              |

