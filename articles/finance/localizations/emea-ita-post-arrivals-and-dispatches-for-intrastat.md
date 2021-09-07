---
title: POST Eingänge und Versendungen für Intrastat buchen
description: In diesem Thema finden Sie ein Beispiel, das zeigt, wie Sie Eingänge und Versendungen für Intrastat buchen.
author: andosip
ms.date: 8/23/2021
ms.topic: article
audience: Application User
ms.reviewer: kfender
ms.search.region: Global
ms.author: v-aosipov
ms.search.validFrom: ''
ms.openlocfilehash: f7bd1811fd0e580a6b6655244c689268915d320e
ms.sourcegitcommit: 72a82e9aeabbdecf57e1aee72975c63eba75143a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/24/2021
ms.locfileid: "7414786"
---
# <a name="post-arrivals-and-dispatches-for-intrastat"></a>POST Eingänge und Versendungen für Intrastat buchen

[!include [banner](../includes/banner.md)]

In diesem Thema finden Sie ein Beispiel, das zeigt, wie Sie Eingänge und Versendungen für Intrastat buchen. Das Beispiel verwendet die juristische Entität **ITCO**.

## <a name="setup"></a>Einrichtung

1. Importieren Sie die neueste Version der folgenden Konfigurationen für elektronische Meldungen (ER):

    - Intrastat-Modell
    - Intrastat-Bericht
    - Intrastat (IT)

    Weitere Details finden Sie unter [Download von ER-Konfigurationen aus dem Global Repository des Konfigurationsdienstes](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md).

2. Definieren Sie in Microsoft Dynamics 365 Finance die folgenden Sequenzen als fortlaufend: **Gene\_397**, **Acco\_16403**, **Gene\_407**, und **PUR\_EU**.

    1. Gehen Sie zu **Organisationsverwaltung** > **Nummernkreise** > **Nummernkreise**.
    2. Wählen Sie im Raster einen der Nummernkreis-Codes aus.
    3. Wählen Sie im Aktionsbereich **Bearbeiten** aus.
    4. Auf der Registerkarte **Allgemein** Inforegister, im Abschnitt **Einrichtung**, legen Sie die Option **Kontinuierlich** auf **Ja** fest.
    5. Wählen Sie im Aktionsbereich **Speichern** aus.

3. Legen Sie eine Lageradresse fest.

    1. Wechseln Sie zu **Lagerortverwaltung** &gt; **Einstellungen** &gt; **Lagerort** &gt; **Lagerorte**.
    2. Wählen Sie in der Liste das Lager **11**.
    3. Wählen Sie auf der Inforegisterkarte **Adresse** die Option **Hinzufügen**.
    4. Geben Sie im Dialogfeld **Neu** **Adresse** im Feld **Name** **oder** **Beschreibung** **Haupt** ein.
    5. Wählen Sie im Feld **Land/Region** die Option **ITA (Italien)**.
    6. Wählen Sie im Feld **Stadt** **Aprilia**.
    7. Wählen Sie **OK** aus.

4. Legen Sie Transaktionscodes fest.

    1. Wechseln Sie zu **Steuer** > **Einstellungen** > **Außenhandel** > **Art des Geschäfts**.
    2. Wählen Sie **Neu**, und legen Sie einen Transaktionscode für Eigentumsübertragungen fest.

        - Geben Sie im Feld **Transaktionscode** **1** ein.
        - Geben Sie in das Feld **Name** **Eigentumsübertragung** ein.

    3. Wählen Sie **Neu**, und legen Sie einen Transaktionscode für Rückgaben fest.

        - Geben Sie im Feld **Art** **des Geschäfts** **2** ein.
        - Geben Sie im Feld **Name** **Warenrücksendung** ein.

5.  Richten Sie Außenhandelsparameter ein.

    1. Gehen Sie zu **Steuer** > **Einstellungen** > **Außenhandel** > **Außenhandelsparameter**.
    2. Auf der Registerkarte **Intrastat** wählen Sie auf dem Inforegister **Allgemein** im Feld **Art** **des Geschäfts** **1** aus.
    3. Wählen Sie im Feld **Gutschrift** **2** aus.
    4. Wählen Sie im Feld **Verkaufs-Berichtszeitraum** den Wert **Monat**.
    5. Wählen Sie im Feld **Berichtszeitraum Kauf** den Wert **Monat**.
    6. Wählen Sie auf der Registerkarte **Elektronisches Reporting** Inforegister, im Feld **Dateiformat-Zuordnung**, **Intrastat (IT)**.
    7. Wählen Sie im Feld **Zuordnung des Berichtsformats** **Intrastat-Bericht**.
    8. Wählen Sie im Inforegister **Warencode-Hierarchie**, im Feld **Kategorie-Hierarchie**, **Intrastat**.
    9. Legen Sie auf der Registerkarte **Statistischer Wert** Inforegister die Option **Statistische Daten drucken und exportieren** auf **Ja** fest.
    10. Stellen Sie auf der Registerkarte **Länder/Regionen-Eigenschaften** sicher, dass die folgenden Zeilen vorhanden sind.

        | **Partei/Land/Region** | **Intrastat-Code** | **Währung** | **Länder-/Regionsart** |
        |--------------------------|--------------------|--------------|-------------------------|
        | ITA                      | IT                 | EUR          | Eigen                |
        | SMR                      | SM                 | EUR          | Sonderschlüssel Inland        |

    11. Wählen Sie in der Symbolleiste **Neu**, um die folgende Zeile zu erstellen.

        | **Partei/Land/Region** | **Intrastat-Code** | **Währung** | **Länder-/Regionsart** |
        |--------------------------|--------------------|--------------|-------------------------|
        | DNK                      | DK                 | DKK          | EU                      |

6. Legen Sie steuerbefreite Nummern fest.

    1. Gehen Sie zu **Steuern** > **Einrichtung** > **Mehrwertsteuer** > **Steuerbefreite Nummern**.
    2. Wählen Sie im Aktionsbereich **Neu**, um die folgenden Zeilen zu erstellen.

        | **Land/Region** | **Steuerbefreiungsnummer** | **Name des Unternehmens** |
        |--------------------|-----------------------|------------------|
        | DEU                | DE3456789012          | UE KREDITOR        |
        | DNK                | DK0987654321          | Customer ER      |

7. Legen Sie die Adresse des Kreditors fest.

    1. Wechseln Sie zu **Kreditorenkonten** &gt; **Kreditoren** &gt; **Alle Kreditoren**.
    2. Wählen Sie im Raster **UE Kreditor**.
    3. Wählen Sie auf dem Inforegister **Adressen** die Option **Hinzufügen**.
    4. Geben Sie im Dialogfeld **Neue Adresse** im Feld **Name oder Beschreibung** **Deutschland** ein.
    5. Wählen Sie im Feld **Land/Region** **DEU** aus.
    6. Wählen Sie **OK**, um die neue Adresse zu erstellen.
    7. Wählen Sie im Inforegister **Rechnung und Lieferung** im Abschnitt **Umsatzsteuer** im Feld **Steuerbefreite Nummer** die Option **Alle** und dann **DE1234567890**.
    8. Wählen Sie im Aktionsbereich **Speichern** aus.

8. Kundenadressen festlegen.

    1. Gehen Sie zu **Debitoren** > **Kunden** > **Alle Kunden**.
    2. Wählen Sie im Raster **ITCO-000001**.
    3. Wählen Sie auf der Inforegisterkarte **Adressen** die Option **Bearbeiten**.
    4. Geben Sie im Dialogfeld **Neue Adresse** im Feld **Name oder Beschreibung** **San Marino** ein.
    5. Wählen Sie im Feld **Land/Region** **SMR** aus.
    6. Wählen Sie **OK**, um die neue Adresse zu erstellen.
    7. Wählen Sie auf dem Inforegister **Rechnung und Lieferung**, im Abschnitt **Rechnung**, im Feld **Rechnungskonto**, **ITCO-000001**.
    8. Wählen Sie im Feld **Nummernkreis Gruppe** den Eintrag **IT \_VENDOM**.
    9. Wählen Sie im Aktivitätsbereich **Speichern**, und schließen Sie die Seite.
    10. Wählen Sie auf der Seite **Alle Kunden** im Raster **ITCO-000002**.
    11. Wählen Sie im Inforegister **Adressen** **Hinzufügen**.
    12. Geben Sie im Dialogfeld **Neue Adresse** im Feld **Name oder Beschreibung** **Dänemark** ein.
    13. Wählen Sie im Feld **Land/Region** **DNK** aus.
    14. Wählen Sie **OK**, um die neue Adresse zu erstellen.
    15. Wählen Sie auf dem Inforegister **Umsatzdemografie** im Feld **Währung** die Option **DKK**.
    16. Auf der Registerkarte **Rechnung und Lieferung** Inforegister, im Abschnitt **Umsatzsteuer**, im Feld **Umsatzsteuer-Gruppe**, wählen Sie **IT \_PUREU**.
    17. Im Feld **Steuerbefreiungsnummer** wählen Sie **Alle** und dann **DK0987654321**.
    18. Wählen Sie im Aktionsbereich **Speichern** aus.

9. Legen Sie die Kategorienhierarchie fest.

    1. Gehen Sie zu **Produktinformationsmanagement** > **Einrichtung** > **Kategorien und Attribute** > **Kategorie-Hierarchien**.
    2. Wählen Sie im Raster **Intrastat** aus.
    3. Klicken Sie im Aktivitätsbereich auf **Neuer Kategorieknoten**.
    4. Geben Sie in das Feld **Name** den Wert **Dienst** ein.
    5. Geben Sie in das Feld **Code** **123456** ein.
    6. Wählen Sie im Aktionsbereich **Speichern** aus.

10. Produkte einrichten.

    1. Gehen Sie zu **Produktinformationsverwaltung** > **Produkte** > **Freigegebene Produkte**.
    2. Wählen Sie im Raster **ITEM** aus.
    3. Auf dem Inforegister **Kauf**, im Abschnitt **Verwaltung**, im Feld **Kreditor** wählen Sie **ITCO-000001**.
    4. Auf der Registerkarte **Außenhandel** Inforegister, im Abschnitt **Intrastat**, im Feld **Ware**, wählen Sie **\[100 200 30\] Lautsprecher**.
    5. Wählen Sie im Abschnitt **Herkunft** im Feld **Land/Region** **DEU** aus.
    6. Wählen Sie im Feld **Staat/Provinz** den Eintrag **BE**.
    7. Auf der Registerkarte **Lagerbestand verwalten** Inforegister, im Abschnitt **Nettomessungen**, im Feld **Nettogewicht**, geben Sie **5** ein.
    8. Wählen Sie im Aktionsbereich **Speichern** aus.
    9. Wählen Sie auf der Seite **Zugelassene Artikel** im Raster **Serviceartikel**.
    10. Auf der Seite **Außenhandel** Inforegister, im Abschnitt **Intrastat**, im Feld **Ware**, wählen Sie **\[123456\] Service**.
    11. Wählen Sie im Aktionsbereich **Speichern** aus.

11. Legen Sie die Verkehrszweige fest.

    1. Gehen Sie zu **Steuer** > **Einrichtung** > **Außenhandel** > **Transportmethode**.
    2. Wählen Sie im Aktionsbereich **Neu**, um die folgenden Verkehrszweige zu erstellen.

        | **Transport** | **Beschreibung** |
        |---------------|-----------------|
        | 1             | Straße            |
        | 2             | Luft             |

12. Legen Sie eine Versandart fest.

    1. Gehen Sie zu **Beschaffung** > **Einstellungen** > **Vertrieb** > **Liefermodus**.
    2. Wählen Sie im Aktivitätsbereich **Neu** aus.
    3. Geben Sie in das Feld **Lieferart** **1** ein.
    4. Geben Sie in das Feld **Beschreibung** **LKW** ein.
    5. Wählen Sie auf dem Inforegister **Außenhandel** im Feld **Transport** die Option **1 Straße**.
    6. Wählen Sie im Aktionsbereich **Speichern** aus.

13. Legen Sie die Lieferbedingungen fest.

    1. Gehen Sie zu **Kreditoren** > **Einrichtung** > **Lieferbedingungen**.
    2. Wählen Sie in der Liste **CFR**.
    3. Auf dem Inforegister **Allgemein** geben Sie im Feld **Intrastat-Code** **1** ein.

## <a name="post-arrivals-for-intrastat"></a>Eingänge für Intrastat buchen

### <a name="purchase-goods-by-using-a-purchase-order"></a>Kauf von Waren mit Hilfe einer Bestellung

Dieser Teil des Beispiels zeigt, wie Sie eine Bestellung verwenden, um Waren (Artikel) aus Ländern der Europäischen Union (EU) zu kaufen.

1. Gehen Sie zu **Kreditoren** > **Bestellungen** > **Alle Bestellungen**.
2.  Wählen Sie im Aktivitätsbereich **Neu** aus.
3.  Wählen Sie im Dialogfeld **Bestellung erstellen** im Feld **Lieferantenkonto** den Eintrag **UE Kreditor**.
4.  Wählen Sie im Inforegister **Verwaltung** im Feld **Sprache** die Option **it**.
5.  Wählen Sie **OK** aus.
6.  Überprüfen Sie in der Ansicht **Kopfzeile** auf dem Inforegister **Ausland** **Inforegister**, dass das Feld **Transaktionscode** auf **1** festgelegt ist.
7.  Stellen Sie sicher, dass das Feld **Herkunfts-/Zielland** auf **RM** festgelegt ist.
8.  Wählen Sie im Inforegister **Zustellung** im Abschnitt **Zustellung** im Feld **Zustellungsart** den Wert **1**.
9.  Wählen Sie im Feld **Lieferbedingungen** **CFR**.
10. In der Ansicht **Zeilen**, auf dem Inforegister **Bestellzeilen**, wählen Sie im Feld **Positionsnummer** den Eintrag **Element**.
11. Im Feld **Standort** wählen Sei **1** aus.
12. Im Feld **Lagerort** wählen Sie **11** aus.
13. Geben Sie im Feld **Menge** den Wert **10** ein.
14. Geben Sie im Feld **Einzelpreis** die Zahl **100** ein.
15. Auf der Registerkarte **Einrichtung**, im Abschnitt **Umsatzsteuer**, im Feld **Element Mehrwertsteuergruppe**, wählen Sie **22%EU**.
16. Wählen Sie im Aktionsbereich, auf der Registerkarte **Kauf**, in der Gruppe **Aktionen** den Eintrag **Bestätigen**.
17. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Rechnung** in der Gruppe **Generieren** **Rechnung** aus.
18. Wählen Sie im Aktionsbereich **Standard von**.
19. Wählen Sie im Feld **Standardmenge für Zeilen** die Option **Bestellmenge** und anschließend **OK**.
20. Auf dem Inforegister **Kreditor Rechnungskopf**, im Abschnitt **Rechnungsidentifikation**, im Feld **Nummer** geben Sie **0001** ein.
21. Wählen Sie im Abschnitt **Rechnungsdaten** im Feld **Rechnungsdatum** den Wert **7/9/2021**.
22. Wählen Sie im Aktionsbereich **Buchen**, um die Rechnung zu buchen.

### <a name="purchase-services-by-using-a-vendor-invoice"></a>Kauf von Dienstleistungen mit Hilfe einer Servicerechnung

Dieser Teil des Beispiels zeigt, wie Sie eine Kreditor-Rechnung verwenden, um Dienstleistungen aus EU-Ländern zu kaufen.

1. Gehen Sie zu **Kreditoren** > **Rechnungen** > **Rechnungsjournal**.
2. Wählen Sie im Aktivitätsbereich **Neu** aus.
3. Wählen Sie im Feld **Name** den Eintrag **VERSAND \_EUINV**.
4. Wählen Sie im Aktivitätsbereich **Positionen** aus.
5. Im Feld **Datum** geben Sie **7/9/2021** ein.
6. Wählen Sie im Feld **Kontotyp** die Option **Kreditor**.
7. Wählen Sie im Feld **Konto** die Option **UE Kreditor**.
8. Wählen Sie im Feld **Rechnungsdatum** den Wert **7/9/2021**.
9. Geben Sie im Feld **Rechnung** **ITA-0004** ein.
10. Geben Sie in das Feld **Kredit** **120000** ein.
11. Wählen Sie im Feld **Sachkonto** **Typ** **Sachkonto**.
12. Im Feld **Saldokonto** wählen Sie **110130**.
13. Wählen Sie im Feld **Mehrwertsteuer-Gruppe** den Eintrag **IT \_PUREU**.
14. Wählen Sie im Feld **Element Mehrwertsteuergruppe** den Eintrag **22%EU**.
15. Gehen Sie auf der Registerkarte **Auslandshandel** wie folgt vor:

    1. Wählen Sie im Feld **Transaktionscode** den Wert **1**.
    2. Wählen Sie im Feld **Transport** die Option **2 Luft**.
    3. Wählen Sie im Feld **Ware** **\[123456\] Service**.
    4. Wählen Sie im Feld **Land/Region** **ITA** aus.
    5. Wählen Sie im Feld **Staat/Provinz** die Option **LAZ**.
    6. Wählen Sie im Feld **Herkunfts-/Bestimmungslandkreis** **LT**.


16. Wählen Sie im Aktionsbereich **Buchen** aus.
17. Erstellen Sie eine Intrastat-Meldung für Ankünfte.

    1. Wechseln Sie zu **Steuer** > **Meldungen** > **Außenhandel** > **Intrastat**.
    2. Wählen Sie im Aktivitätsbereich **Übertragung**.
    3. Legen Sie im Dialogfeld **Intrastat (Übertragung)** die Option **Kreditor-Rechnung** auf **Ja** fest.
    4. Wählen Sie **OK**, um die Transaktionen zu übertragen, und überprüfen Sie dann das Intrastat-Buch.-Blatt.

   ![Seite Intrastat-Buch.-Blatt, Registerkarte Übersicht.](media/ita_intrastat_journal_vendor_invoice.png)

18. Überprüfen Sie die Registerkarte **Allgemein** für die Bestellung.

    ![Details zur Intrastat-Buchungsblattzeile für die Bestellung](media/ita_intrastat_journal_purchase_order_line_details.png)

19. Überprüfen Sie die Registerkarte **Allgemein** für die Kreditor-Rechnung.

    ![Details der Buchungsblattzeile für die Kreditor-Rechnung im Intrastat-Journal](media/ita_intrastat_journal_vendor_invoice_line_details.png)

20. Generieren Sie den Intrastat-Bericht für Eingänge.

    1. Wählen Sie im Aktivitätsbereich **Ausgabe** > **Bericht**.
    2. Wählen Sie im Dialogfeld **Intrastat-Bericht** im Abschnitt **Datum** im Feld **Ausgangsdatum** den Wert **7/1/2021**.
    3. Wählen Sie im Feld **Bis zum Datum** den Wert **7/31/2021**.
    4. Legen Sie im Bereich **Exportoptionen** die Optionen **Datei generieren** und **Bericht generieren** auf **Ja** fest.
    5. Geben Sie im Feld **Dateiname** **Eingangsdatei** ein.
    6. Geben Sie in das Feld **Berichtsdateiname** **Eingangsbericht** ein.
    7. Wählen Sie im Feld **Richtung** die Option **Eingänge**.
    8. Geben Sie in das Feld **Referenznummer** **123456** ein.
    9. Wählen Sie **OK**, um den Intrastat-Bericht und die Intrastat-Datei zu erzeugen und zu überprüfen.

    Die folgende Abbildung zeigt ein Beispiel für einen Intrastat-Bericht.

    ![Intrastat-Ankunftsbericht.](media/ita_intrastat_arrivals_report.png)

    Die folgende Abbildung zeigt ein Beispiel für eine Intrastat-Datei.

    ![Intrastat-Eingangsdatei.](media/ita_intrastat_arrivals_file.png)

## <a name="post-dispatches-for-intrastat"></a>Versendungen für Intrastat buchen

### <a name="sell-goods-by-using-a-sales-order"></a>Verkaufen von Waren mit Hilfe eines Verkaufsauftrags

Dieser Teil des Beispiels zeigt, wie Sie einen Verkaufsauftrag verwenden, um Waren (Artikel) in Länder der Europäischen Union (EU) zu verkaufen.

1. Gehen Sie zu **Debitoren** > **Aufträge** > **Alle Aufträge**.
2. Wählen Sie im Aktivitätsbereich **Neu** aus.
3. Wählen Sie im Dialogfeld **Verkaufsauftrag erstellen** im Feld **Kundenkonto** die Option **ITCO-000002**.
4. Wählen Sie **OK** aus.
5. Wählen Sie in der Ansicht **Kopf** auf dem Inforegister **Lieferung** im Abschnitt **Sonstige Lieferinformationen** im Feld **Lieferart** die Option **1 LKW**.
6. Wählen Sie im Feld **Lieferbedingungen** **CFR**.
7. In der Ansicht **Zeilen**, auf dem Inforegister **Verkaufsauftragszeilen**, im Feld **Positionsnummer**, wählen Sie **ITEM**.
8. Geben Sie im Feld **Menge** den Wert **50** ein.
9. Im Feld **Standort** wählen Sei **1** aus.
10. Im Feld **Lagerort** wählen Sie **11** aus.
11. Geben Sie im Feld **Einzelpreis** die Zahl **250** ein.
12. Auf der Registerkarte **Zeilendetails** Inforegister, auf der Registerkarte **Einrichtung**, im Abschnitt **Umsatzsteuer**, im Feld **Element Mehrwertsteuergruppe**, wählen Sie **22%EU**.
13. Wählen Sie im Aktionsbereich **Speichern** aus.
14. Wählen Sie im Aktionsbereich auf der Registerkarte **Rechnung** in der Gruppe **Generieren** den Eintrag **Rechnung**, um die Rechnung für die Bestellung zu erstellen.
15. Im Dialogfenster **Rechnung buchen**, im Inforegister **Parameter**, im Abschnitt **Parameter**, im Feld **Menge**, wählen Sie **Alle**.
16. Auf der Registerkarte **Einrichtung** Inforegister, im Feld **Rechnung** **Datum**, wählen Sie **7/9/2021**.
17. Wählen Sie **OK** aus.
18. Überprüfen Sie die Zeilen im Intrastat-Buch.-Blatt.

    1. Wechseln Sie zu **Steuer** > **Meldungen** > **Außenhandel** > **Intrastat**.
    2. Wählen Sie im Aktivitätsbereich **Übertragung**.
    3. Legen Sie in der Dialogbox **Intrastat (Transfer)** die Option **Debitorenrechnung** auf **Ja** fest.
    4. Wählen Sie **OK**, um die Transaktionen zu übertragen, und überprüfen Sie das Intrastat-Buch.-Blatt. Die Gutschriftstransaktion wird als Korrektur markiert und hat einen negativen Rechnungsbetrag.

        ![Seite Intrastat-Buch.-Blatt](media/ita_intrastat_journal_sales_order.png)

        ![Details der Intrastat-Journalzeilen für den Verkaufsauftrag](media/ita_intrastat_journal_sales_order_line_details.png)

### <a name="return-goods-by-using-a-credit-note"></a>Rücksendung von Waren mit Hilfe einer Gutschrift

Dieser Teil des Beispiels zeigt, wie Sie eine Gutschrift verwenden, um Waren (Artikel) aus Ländern der Europäischen Union (EU) zurückzusenden.

1. Gehen Sie zu **Debitoren** > **Aufträge** > **Alle Aufträge**.
2. Wählen Sie im Aktivitätsbereich **Neu** aus.
3. Wählen Sie im Dialogfeld **Verkaufsauftrag erstellen** im Feld **Kundenkonto** die Option **ITCO-000002**.
4. Wählen Sie **OK** aus.
5. Wählen Sie in der Ansicht **Kopf** auf dem Inforegister **Lieferung** im Abschnitt **Sonstige Lieferinformationen** im Feld **Lieferart** die Option **1 LKW**.
6. Wählen Sie im Feld **Lieferbedingungen** **CFR**.
7. Wählen Sie auf dem Inforegister **Außenhandel** im Feld **Transaktionscode** die Option **2**.
8. Auf der Registerkarte **Zeilen**, auf dem Inforegister **Verkaufsauftragszeilen**, im Feld **Positionsnummer**, wählen Sie **ITEM**.
9. Geben Sie im Feld **Menge** **-10** ein.
10. Im Feld **Standort** wählen Sei **1** aus.
11. Im Feld **Lagerort** wählen Sie **11** aus.
12. Geben Sie im Feld **Einzelpreis** die Zahl **250** ein.
13. Auf der Registerkarte **Zeilendetails** Inforegister, auf der Registerkarte **Einrichtung**, im Abschnitt **Umsatzsteuer**, im Feld **Element Mehrwertsteuergruppe**, wählen Sie **22%EU**.
14. Wählen Sie im Abschnitt **Rücklieferung** im Feld **Rücklieferungsnummer** das Los, das Sie zuvor erstellt haben.
15. Wählen Sie im Aktionsbereich **Speichern** aus.
16. Wählen Sie im Aktionsbereich auf der Registerkarte **Rechnung** in der Gruppe **Generieren** den Eintrag **Rechnung**, um die Rechnung für die Bestellung zu erstellen.
17. Wählen Sie im Inforegister **Parameter**, im Abschnitt **Parameter**, im Feld **Menge** die Option **Alle**.
18. Im Dialogfenster **Rechnung buchen**, auf der Registerkarte **Einrichtung**, im Feld **Rechnung** **Datum** wählen Sie **7/9/2021**.
19. Klicken Sie auf **OK**, um die Rechnung zu buchen.
20. Überprüfen Sie die Zeilen im Intrastat-Buch.-Blatt.

    1. Wechseln Sie zu **Steuer** > **Meldungen** > **Außenhandel** > **Intrastat**.
    2. Wählen Sie im Aktivitätsbereich **Übertragung**.
    3. Legen Sie in der Dialogbox **Intrastat (Transfer)** die Option **Debitorenrechnung** auf **Ja** fest.
    4. Wählen Sie **OK**, um die Transaktionen zu übertragen, und überprüfen Sie das Intrastat-Buch.-Blatt. Die Gutschriftstransaktion wird als Korrektur markiert und hat einen negativen Rechnungsbetrag.

    ![Intrastat-Journal-Gutschrift](media/ita_intrastat_journal_credit_note.png)

    ![Details zur Intrastat-Buchungsblattzeile für die Gutschrift](media/ita_intrastat_journal_credit_note_line_details.png)

### <a name="sell-goods-to-san-marino-by-using-a-sales-order"></a>Verkauf von Waren nach San Marino mit Hilfe eines Verkaufsauftrags

Dieser Teil des Beispiels zeigt, wie Sie einen Verkaufsauftrag verwenden, um Waren (Artikel) nach San Marino zu kaufen.

1. Gehen Sie zu **Debitoren** > **Aufträge** > **Alle Aufträge**.
2. Wählen Sie im Aktivitätsbereich **Neu** aus.
3. Wählen Sie im Dialogfeld **Verkaufsauftrag erstellen** im Feld **Kundenkonto** die Option **ITCO-000001**.
4. Wählen Sie **OK** aus.
5. In der Ansicht **Kopf**, auf dem Inforegister **Lieferung**, im Abschnitt **Sonstige Lieferinfo**, im Feld **Lieferart**, wählen Sie **1**.
6. Wählen Sie im Feld **Lieferbedingungen** **CFR**.
7. Auf der Registerkarte **Zeilen**, auf dem Inforegister **Verkaufsauftragszeilen**, im Feld **Positionsnummer**, wählen Sie **ITEM**.
8. Geben Sie im Feld **Menge** den Wert **30** ein.
9. Im Feld **Standort** wählen Sei **1** aus.
10. Im Feld **Lagerort** wählen Sie **11** aus.
11. Geben Sie im Feld **Einzelpreis** die Zahl **200** ein.
12. Wählen Sie im Aktionsbereich **Speichern** aus.
13. Wählen Sie im Aktionsbereich auf der Registerkarte **Rechnung** in der Gruppe **Generieren** den Eintrag **Rechnung**, um die Rechnung für die Bestellung zu erstellen.
14. Wählen Sie im Inforegister **Parameter**, im Abschnitt **Parameter**, im Feld **Menge** die Option **Alle**.
15. Im Dialogfenster **Rechnung buchen**, auf der Registerkarte **Einrichtung**, im Feld **Rechnung** **Datum** wählen Sie **7/9/2021**.
16. Klicken Sie auf **OK**, um die Rechnung zu buchen.
17. Überprüfen Sie die Zeilen im Intrastat-Buch.-Blatt.

    1. Wechseln Sie zu **Steuer** > **Meldungen** > **Außenhandel** > **Intrastat**.
    2. Wählen Sie im Aktivitätsbereich **Übertragung**.
    3. Legen Sie in der Dialogbox **Intrastat (Transfer)** die Option **Debitorenrechnung** auf **Ja** fest.
    4. Wählen Sie **OK**, um die Transaktionen zu übertragen, und überprüfen Sie das Intrastat-Buch.-Blatt.

   ![Intrastat-Buch.-Blatt für San Marino](media/ita_intrastat_journal_sales_order_san_marino.png)

   ![Intrastat-Buchungsblattzeile Details für San Marino](media/ita_intrastat_journal_sales_order_san_marino_line_details.png)

18. Erstellen Sie eine Intrastat-Meldung für Versendungen.

    1. Wechseln Sie zu **Steuer** &gt; **Meldungen** &gt; **Außenhandel** &gt; **Intrastat**.
    2. Wählen Sie im Aktivitätsbereich **Ausgabe** &gt; **Bericht**.
    3. Wählen Sie im Dialogfeld **Intrastat-Bericht** im Abschnitt **Datum** im Feld **Ausgangsdatum** den Wert **7/1/2021**.
    4. Wählen Sie im Feld **Bis zum Datum** den Wert **7/31/2021**.
    5. Legen Sie im Bereich **Exportoptionen** die Optionen **Datei generieren** und **Bericht generieren** auf **Ja** fest.
    6. Geben Sie im Feld **Dateiname** **Versanddatei** ein.
    7. Geben Sie in das Feld **Berichtsdateiname** **Versandbericht** ein.
    8. Wählen Sie im Feld **Richtung** die Option **Versand**.
    9. Geben Sie in das Feld **Referenznummer** **98754** ein.
    10. Wählen Sie **OK**, um den Intrastat-Bericht und die Intrastat-Datei zu erzeugen.

        Die folgende Abbildung zeigt ein Beispiel für einen gedruckten Intrastat-Bericht.

        ![Intrastat-Bericht](media/ita_intrastat_report_for_dispatches.png)

        Die folgende Abbildung zeigt ein Beispiel für eine gedruckte Intrastat-Datei.

        ![Intrastat-Datei für Versendungen](media/ita_intrastat_file_for_dispatches.png)
