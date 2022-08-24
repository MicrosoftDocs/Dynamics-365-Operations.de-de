---
title: Intrastat (Schweden)
description: Dieser Artikel enthält Informationen zur Intrastat-Meldung in Schweden.
author: AdamTrukawka
ms.date: 08/24/2021
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: ''
ms.openlocfilehash: e13076a6b8f18374c012a5b56f13e752010256b8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279230"
---
# <a name="swedish-intrastat"></a>Schwedisches Intrastat

[!include[banner](../includes/banner.md)]

Die **Intrastaz** Seite wird verwendet, um Informationen zum Handel zwischen EU-Ländern/Regionen generieren und melden. Die schwedische Intrastat-Meldung enthält Informationen über die Inzahlungnahme von Waren zur Meldung.

Die folgenden Felder sind in der schwedischen Intrastat-Meldung enthalten:

   - Partnerland ISO-Code
   - Art des Geschäftes
   - Warencode
   - Zusätzliche Einheit
   - Gewicht
   - Rechnungsbetrag

## <a name="set-up-intrastat"></a>Einrichten von Intrastat

Importieren Sie die neueste Version der folgenden Konfigurationen für elektronische Meldungen (ER):

   - Intrastat-Modell
   - Intrastat-Bericht
   - Intrastat (SE)

Weitere Informationen finden Sie unter [Herunterladen von ER-Konfigurationen aus dem Global Repository des Konfigurationsdienstes](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md).

## <a name="set-up-foreign-trade-parameters"></a>Außenhandelsparameter einrichten

1. Gehen Sie in Microsoft Dynamics 365 Finance zu **Steuern** > **Einrichtung** > **Außenhandelsparameter**.
2. Auf der Registerkarte **Intrastat**, auf dem Inforegister **Elektronisches Berichtswesen**, im Feld **Dateiformatzuordnung** wählen Sie **Intrastat (SE)**.
3. Im Feld **Berichtformatzuordnung** **Intrastatbericht** auswählen.
4. Auf dem Inforegister **Warencodehierarchie** im Feld **Kategoriehierarchie** wählen Sie **Intrastat**.
5. Wählen Sie im Feld **Art des Geschäfts** die Art des Geschäfts für Eigentumsübertragungen aus. Sie verwenden diesen Code für Transaktionen, die tatsächliche oder geplante Eigentumsübertragungen gegen Vergütung (finanziell oder anderweitig) zur Folge haben. Sie verwenden ihn auch für Korrekturen. Unternehmen in Schweden verwenden einstellige Transaktionscodes.
6. Wählen Sie im Feld **Gutschrift** die Art des Geschäfts für die Warenrücksendung aus.
7. Auf der Registerkarte **Länder-/Regionseigenschaften** führen Sie im Feld **Land/Region** alle Länder oder Regionen auf, mit denen Ihre Unternehmen Geschäfte macht. Für jedes Land, das Teil der EU ist, wählen Sie im Feld **Land/Regionstyp** die Option **EU**, damit das Land in Ihrem Intrastat-Bericht erscheint.

## <a name="set-up-the-product-parameters-for-the-intrastat-declaration"></a>Legen Sie die Produktparameter für die Intrastat-Meldung fest

1. Wechseln Sie zu **Produktinformationsverwaltung** > **Produkte** > **Freigegebene Produkte** aus.
2. Wählen Sie im Raster ein Produkt aus.
3. Auf der Registerkarte **Außenhandel** Inforegister, im Abschnitt **Intrastat**, im Feld **Ware**, wählen Sie die Warennummer.
4. Auf der Registerkarte **Lagerbestand verwalten** Inforegister, im Feld **Nettogewicht**, geben Sie das Gewicht des Produkts in Kilogramm ein.
5. Gehen Sie zu **Steuer** > **Einstellungen** > **Außenhandel** > **Komprimierung von Intrastat** und wählen Sie die Felder aus, die verglichen werden sollen, wenn Intrastat-Informationen zusammengefasst werden. Wählen Sie für Schwedisch Intrastat die folgenden Felder aus:

    - Warencode
    - Art des Geschäftes
    - Planungsrichtung
    - Land/Region
    - Berichtigung
    - Rechnung

## <a name="intrastat-transfer"></a>Intrastat-Übertragung

Auf der Seite **Intrastat** im Aktivitätsbereich können Sie **Überweisen** auswählen, um die Informationen über den innergemeinschaftlichen Handel aus Ihren Verkaufsaufträgen, Freitextrechnungen, Bestellungen, Lieferantenrechnungen, Lieferantenprodukteingängen, Projektrechnungen und Transferaufträgen automatisch zu übertragen. Es werden nur Dokumente übermittelt, die ein EU-Land als Bestimmungsland oder -Region (bei Versendungen) haben.

Alternativ können Sie Transaktionen manuell eingeben, indem Sie **Neu** im Aktionsbereich auswählen.

### <a name="generate-an-intrastat-report"></a>Generieren eines Intrastat-Berichts

1. Wechseln Sie zu **Steuer** > **Meldungen** > **Außenhandel** > **Intrastat**.
2. Wählen Sie im Aktivitätsbereich **Ausgabe** > **Bericht**.
3. Im angezeigten Dialogfeld **Intrastat-Bericht** legen Sie die folgenden Felder fest.

    | Feld            | Beschreibung                                                                                                                         |
    |------------------|-------------------------------------------------------------------------------------------------------------------------------------|
    | Anfangsdatum        | Wählen Sie das Startdatum für den Bericht.                                                                                               |
    | Bis-Datum          | Wählen Sie das Enddatum für den Bericht.                                                                                                 |
    | Datei generieren    | Legen Sie diese Option auf **Ja** fest, um eine .txt-Datei für Ihren Intrastat-Bericht zu erzeugen.                                                       |
    | Dateiname        | Geben Sie den Namen der .txt-Datei ein.                                                                                                    |
    | Bericht generieren  | Legen Sie diese Option auf **Ja** fest, um eine .xlsx-Datei für Ihren Intrastat-Bericht zu generieren.                                                     |
    | Berichtdateiname | Geben Sie den Namen der .xlsx-Datei ein.                                                                                                   |
    | Planungsrichtung        | **Eingang** für einen Bericht über die innergemeinschaftlichen Eingänge auswählen. **Versand** für einen Bericht über innergemeinschaftliche Versendungen auswählen. |

4. Wählen Sie **OK**, und überprüfen Sie die generierten Berichte.

## <a name="example"></a>Beispiel

Dieses Beispiel zeigt, wie Sie Eingänge und Versendungen für Intrastat buchen. Sie verwenden die **DEMF** juristische Person verwenden.

### <a name="preliminary-setup"></a>Vorläufige Einstellungen

1. Gehen Sie zu **Organisationsverwaltung** > **Organisation** > **Juristische Entitäten**, und wählen Sie die juristische Entität **DEMF**.
2. Wählen Sie auf der Inforegister-Registerkarte **Adressen** die Option **Bearbeiten** und dann im Feld **Land/Region** die Option **SWE (Schweden)**.
3. Importieren Sie die neueste Version der folgenden ER-Konfigurationen:

    - Intrastat-Modell
    - Intrastat-Bericht
    - Intrastat (SE)

### <a name="create-transaction-codes"></a>Erstellen Sie Transaktionscodes

1. Wechseln Sie zu **Steuer** > **Einstellungen** > **Außenhandel** > **Art des Geschäfts**.
2. Wählen Sie im Aktivitätsbereich **Neu** aus.
3. Geben Sie im Feld **Art** **des Geschäfts** **1** ein.
4. Geben Sie in das Feld **Name** **Normale Transaktionen** ein
5. Wählen Sie im Aktionsbereich **Speichern** aus.

### <a name="set-up-foreign-trade-parameters"></a>Außenhandelsparameter einrichten

1. Gehen Sie zu **Steuer** > **Einstellungen** > **Außenhandel** > **Außenhandelsparameter**.
2. Auf der Registerkarte **Intrastat** wählen Sie auf dem Inforegister **Allgemein** im Feld **Art** **des Geschäfts** **1** aus.
3. Wählen Sie auf der Registerkarte **Elektronisches Berichtswesen** Inforegister, im Feld **Dateiformatzuordnung**, **Intrastat (SE)**.
4. Wählen Sie im Feld **Berichtformatzuordnung** **Intrastatbericht** aus.
5. Gehen Sie sicher, dass Sie im Inforegister **Warencodehierarchie** im Feld **Kategoriehierarchie** **Intrastat** auswählen.
6. Wählen Sie auf der Registerkarte **Länder-/Regionseigenschaften** **Neu** aus.
7. Wählen Sie im Feld **Land/Region der Partei** **SWE** aus.
8. Wählen Sie im Feld **Land/Regionstyp** die Option **Inland**.
9. Wählen Sie im Feld **Partei Land/Region** die Option **DEU** und dann im Feld **Land/Regionstyp** die Option **EU**.

### <a name="set-up-product-information"></a>Produktinformation festlegen

1. Gehen Sie zu **Produktinformationsverwaltung** > **Produkte** > **Veröffentlichte Produkte**.
2. Wählen Sie im Raster **D0001** aus.
3. Auf dem Inforegister **Außenhandel** wählen Sie im Abschnitt **Intrastat** im Feld **Ware** **100 200 30** aus.
4. Wählen Sie im Inforegister **Bestand verwalten** im Abschnitt **Gewichtsmessungen** im Feld **Nettogewicht** **5** ein.
5. Wählen Sie im Aktionsbereich **Speichern** aus.

### <a name="change-the-site-address"></a>Ändern Sie die Standortadresse

1. Gehen Sie zu **Lagerortverwaltung** > **Einrichtung** > **Lager** > **Standorte**.
2. Wählen Sie im Raster **1** aus.
3. Wählen Sie auf der Inforegisterkarte **Adressen** die Option **Bearbeiten**.
4. Wählen Sie im Dialogfeld **Adresse bearbeiten** im Feld **Land/Region** die Option **SWE**.
5. Wählen Sie **OK** aus.

### <a name="create-a-sales-order-with-an-eu-customer"></a>Erzeugen eines Verkaufsauftrags mit einem EU-Kunden

1. Gehen Sie zu **Debitoren** > **Aufträge** > **Alle Aufträge**.
2. Wählen Sie im Aktivitätsbereich **Neu** aus.
3. Wählen Sie im Dialogfeld **Auftrag erstellen** im Inforegister **Debitor** im Abschnitt **Debitor** im Feld **Debitorenkonto** **DE-015** aus.
4. Wählen Sie im Inforegister **Allgemein** im Abschnitt **Lagerdimensionen** im Feld **Standort** **1**.
5. Im Feld **Lagerort** wählen Sie **11** aus.
6. Wählen Sie **OK** aus.
7. Wählen Sie auf der Registerkarte **Zeilen**, auf dem Inforegister **Kundenauftragszeilen**, im Feld **Positionsnummer**, **D0001**. Geben Sie dann im Feld **Menge** den Wert **10** ein.
8. Stellen Sie auf der Registerkarte **Zeilendetails** Inforegister, auf der Registerkarte **Auslandshandel** sicher, dass die Felder **Transaktionscode** und **Ware** automatisch festgelegt sind.
9. Wählen Sie im Aktionsbereich **Speichern** aus.
10. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Rechnung** im Abschnitt **Generieren** **Rechnung** aus.
11. Im **Rechnung buchen** Dialogfeld, auf dem **Parameter** Inforegiser im **Parameter** Abschnitt, im **Menge** Feld, wählen Sie **Alle**.
12. Klicken Sie auf **OK**, um die Rechnung zu buchen.

### <a name="transfer-the-transaction-to-the-intrastat-journal-and-review-the-result"></a>Übertragen Sie die Transaktion in das Intrastat-Buch.-Blatt und überprüfen Sie das Ergebnis

1. Wechseln Sie zu **Steuer** > **Meldungen** > **Außenhandel** > **Intrastat**.
2. Wählen Sie im Aktivitätsbereich **Übertragung**.
3. Im **Intrastat (Übertragung)** Dialogfeld, im **Parameter** Abschnitt, legen Sie die **Kundenrechnung** Option auf **Ja** fest.
4. Wählen Sie **Filter** aus.
5. Wählen Sie im Dialogfeld **Intrastat-Filter** in der Registerkarte **Bereich** die erste Zeile aus und vergewissern Sie sich, dass das Feld **Feld** auf **Datum** gesetzt ist.
6. Wählen Sie im Feld **Kriterien** das aktuelle Datum aus.
7. Wählen Sie **OK** aus, um das Dialogfeld **Intrastat-Filter** zu schließen.
8. Wählen Sie **OK**, um das Dialogfeld **Intrastat (Übertragung)** zu schließen und überprüfen Sie das Ergebnis. Die Position stellt den Auftrag dar, den Sie früher erstellt haben.

    ![Intrastat-Journalzeilen für Verkaufsaufträge](media/swe_intrastat_journal_sales_order.png)

9. Wählen Sie die Transaktionsposition aus, und wählen Sie dann die Registerkarte **Allgemein**, um weitere Details anzuzeigen.

    ![Details der Intrastat-Journalzeilen für den Verkaufsauftrag](media/swe_intrastat_journal_sales_order_line_details.png)

10. Wählen Sie im Aktivitätsbereich **Ausgabe** > **Bericht**.
11. Im **Intrastat-Bericht** Dialogfeld, auf dem Inforegister **Parameter** im Abschnitt **Datum** wählen Sie im Abschnitt den Monat des von Ihnen erstellten Kundenauftrags aus.
12. Im Abschnitt **Exportoptionen** legen Sie die Option **Generieren** auf **Ja** fest. Geben Sie dann im Feld **Dateiname** den gewünschten Namen ein.
13. Legen Sie die Option **Bericht generieren** auf **Ja** fest. Geben Sie dann in das Feld **Berichtsdateiname** den gewünschten Namen ein.
14. Wählen Sie im Feld **Richtung** die Option **Versand**.
15. Wählen Sie **OK** und prüfen Sie den erzeugten Bericht im .txt-Format. Die folgende Tabelle zeigt die Werte in dem Beispielbericht.

    | Partnerland ISO-Code | Art des Geschäftes | Warencode | Zusätzliche Einheit | Gewicht | Rechnungsbetrag |
    |--------------------------|------------------|----------------|-----------------|--------|----------------|
    | IT                       | 1                | 10020030       | 0               | 50     | 3290           |

16. Prüfen Sie den erzeugten Bericht im Excel-Format.

    ![Intrastat-Bericht](media/swe_intrastat_report_for_dispatches.png)

### <a name="create-a-purchase-order"></a>Eine Bestellung erstellen

1. Gehen Sie zu **Kreditoren** > **Bestellungen** > **Alle Bestellungen**.
2. Wählen Sie im Aktivitätsbereich **Neu** aus.
3. Wählen Sie im Dialogfeld **Bestellung erstellen** im Feld **Kreditorenkonto** **DE-001**.
4. Wählen Sie **OK** aus.
5. Stellen Sie auf der Registerkarte **Kopfzeile** im Inforegister **Ausland** **Transaktion** sicher, dass das Feld **Transaktionscode** auf **1** festgelegt ist.
6. Wählen Sie auf der Registerkarte **Zeilen** auf dem Inforegister **Bestellzeilen** im Feld **Positionsnummer** den Wert **D0001**. Geben Sie dann im Feld **Menge** den Wert **6** ein.
7. Wählen Sie im Aktionsbereich, auf der Registerkarte **Kauf**, in der Gruppe **Aktionen** den Eintrag **Bestätigen**.
8. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Rechnung** in der Gruppe **Generieren** **Rechnung** aus.
9. Wählen Sie im Aktionsbereich **Standard von**. Wählen Sie im Feld **Vorgabe Menge für Zeilen** die Option **Bestellte Menge**. Wählen Sie dann **OK** aus.
10. Auf dem Inforegister **Kreditor Rechnungskopf**, im Abschnitt **Rechnungsidentifikation**, im Feld **Nummer** geben Sie **0001** ein.
11. Wählen Sie im Aktionsbereich **Buchen**, um die Rechnung zu buchen.

### <a name="create-an-intrastat-declaration-for-arrivals"></a>Erzeugen einer Intrastat-Meldung für Eingänge

1. Wechseln Sie zu **Steuer** > **Meldungen** > **Außenhandel** > **Intrastat**.
2. Wählen Sie im Aktivitätsbereich **Übertragung**.
3. Legen Sie im Dialogfeld **Intrastat (Übertragung)** die Option **Kreditor-Rechnung** auf **Ja** fest.
4. Wählen Sie **OK**, um die Transaktionen zu übertragen, und überprüfen Sie das Intrastat-Buch.-Blatt.

    ![Intrastat-Journal für Bestellung](media/swe_intrastat_journal_purchase_order.png)

5. Überprüfen Sie die Registerkarte **Allgemein** für die Bestellung.

    ![Details zur Intrastat-Buchungsblattzeile für die Bestellung](media/swe_intrastat_journal_purchase_order_line_details.png)

6. Wählen Sie im Aktivitätsbereich **Ausgabe** > **Bericht**.
7. Im **Intrastat-Bericht** Dialogfeld, auf dem Inforegister **Parameter** im Abschnitt **Datum** wählen Sie im Abschnitt den Monat des von Ihnen erstellten Kundenauftrags aus.
8. Im Abschnitt **Exportoptionen** legen Sie die Option **Generieren** auf **Ja** fest. Geben Sie dann im Feld **Dateiname** den gewünschten Namen ein.
9. Legen Sie die Option **Bericht generieren** auf **Ja** fest. Geben Sie dann in das Feld **Berichtsdateiname** den gewünschten Namen ein.
10. Wählen Sie im Feld **Richtung** die Option **Eingänge**.
11. Wählen Sie **OK** und prüfen Sie den erzeugten Bericht im .txt-Format. Die folgende Tabelle zeigt die Werte in dem Beispielbericht.

    | Partnerland ISO-Code | Art des Geschäftes | Warencode | Zusätzliche Einheit | Gewicht | Rechnungsbetrag |
    |--------------------------|------------------|----------------|-----------------|--------|----------------|
    | IT                       | 1                | 10020030       | 0               | 30     | 1714           |

12. Prüfen Sie den erzeugten Bericht im Excel-Format.

    ![Intrastat-Ankunftsbericht](media/swe_intrastat_arrivals_report.png)
