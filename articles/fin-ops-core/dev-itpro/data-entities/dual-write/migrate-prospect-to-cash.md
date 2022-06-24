---
title: Migrieren von Prospect-to-Cash-Daten vom Datenintegrator nach Dual-Write
description: In diesem Artikel wird beschrieben, wie man Prospect-to-Cash-Daten vom Datenintegrator nach Dual-Write migriert.
author: RamaKrishnamoorthy
ms.date: 02/01/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-26
ms.openlocfilehash: 8e5c11e535bd61e9955a4abf1491e88991ee40f1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894265"
---
# <a name="migrate-prospect-to-cash-data-from-data-integrator-to-dual-write"></a>Migrieren von Prospect-to-Cash-Daten vom Datenintegrator nach Dual-Write

[!include [banner](../../includes/banner.md)]

Die für Data Integrator verfügbare Prospect to cash-Lösung ist nicht mit duales Schreiben kompatibel. Der Grund dafür ist der Index msdynce_AccountNumber in der Kontotabelle, der Teil der Prospect to cash-Lösung ist. Wenn dieser Index vorhanden ist, können Sie nicht dieselbe Debitor-Kontonummer in zwei verschiedenen juristischen Entitäten erstellen. Sie können entweder mit duales Schreiben neu beginnen, indem Sie die Prospect to cash-Daten von Data Integrator zu duales Schreiben migrieren, oder Sie können die letzte „dorman“ Version der Prospect to cash-Lösung installieren. Dieser Artikel deckt beide Ansätze ab.

## <a name="install-the-last-dorman-version-of-the-data-integrator-prospect-to-cash-solution"></a>Installieren Sie die letzte „dorman“ Version des Data Integrator Prospect to cash solution

**P2C Version 15.0.0.2** gilt als die letzte „dorman“ Version der Datenintegrator Prospect to cash Lösung. Sie können sie von [FastTrack for Dynamics 365](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Dual-write/P2C) herunterladen.

Sie müssen es manuell installieren. Nach der Installation bleibt alles genau gleich, außer dass der Index msdynce_AccountNumber entfernt wird.

## <a name="steps-to-migrate-prospect-to-cash-data-from-data-integrator-to-dual-write"></a>Schritte zur Migration von Prospect to cash-Daten von Data Integrator zu duales Schreiben

Um Ihre Prospect-to-Cash-Daten vom Datenintegrator nach Dual-Write zu migrieren, führen Sie die folgenden Schritte aus.

1. Führen Sie die Prostpect-to-Cash-Aufträge des Datenintegrators aus, um eine letzte vollständige Synchronisierung durchzuführen. Auf diese Weise stellen Sie sicher, dass beide Systeme (Finance und Operations-Apps und Customer-Engagement-Apps) über alle Daten verfügen.
2. Um potenziellen Datenverlust zu vermeiden, exportieren Sie die Prospect-to-Cash-Daten aus Microsoft Dynamics 365 Sales in eine Excel-Datei oder eine CSV-Datei (Comma Separated Values). Exportieren Sie Daten aus folgenden Entitäten:

    - [Konto](#account-table)
    - [Kontakt](#contact-table)
    - [Rechnung](#invoice-table)
    - Rechnungsprodukte
    - [Auftrag](#order-table)
    - [Auftrag (Produkte)](#order-products-table)
    - [Produkte](#products-table)
    - [Angebot](#quote-and-quote-product-tables)
    - [Angebotsprodukte](#quote-and-quote-product-tables)

3. Deinstallieren Sie die Prospect-to-Cash-Lösung aus der Sales-Umgebung. In diesem Schritt werden die Spalten und die entsprechenden Daten entfernt, die von der Prospect-to-Cash-Lösung eingeführt wurden.
4. Installieren Sie die Dual-Write-Lösung.
5. Erstellen Sie eine duales Schreiben-Verbindung zwischen der Finance und Operations App und der Customer-Engagement-App für eine oder mehrere juristische Entitäten.
6. Aktivieren Sie Tabellenzuordnungen für duales Schreiben und führen Sie die erste Synchronisierung für die erforderlichen Referenzdaten aus. (Weitere Informationen finden Sie unter [Überlegungen zur Erstsynchronisierung](initial-sync-guidance.md).) Beispiele für erforderliche Daten sind Kundengruppen, Zahlungsbedingungen und Zahlungspläne. Aktivieren Sie die Zuordnungen für duales Schreiben nicht für Tabellen, für die eine Initialisierung erforderlich ist, z. B. Konto-, Angebots-, Angebotspositions-, Auftrags- und Auftragspositionstabellen.
7. Wechseln Sie in der Customer Engagement-App zu **Erweiterte Einstellungen \> Systemeinstellungen \> Datenverwaltung \> Erkennungsregeln für Duplikate** und deaktivieren Sie alle Regeln.
8. Initialisieren Sie die in Schritt 2 aufgeführten Tabellen. Anweisungen finden Sie in den verbleibenden Abschnitten dieses Artikels.
9. Öffnen Sie die App Finance und Operations und aktivieren Sie die Zuordnungen der Tabellen, wie z.B. die Zuordnungen der Tabellen Konto, Kurs, Kurszeile, Auftrag und Auftragszeile. Führen Sie anschließend die Erstsynchronisierung durch. (Weitere Informationen finden Sie unter [Berücksichtigung bei der ersten Synchronisierung](initial-sync-guidance.md)). Bei diesem Vorgang werden zusätzliche Informationen aus der App Finance und Operations synchronisiert, z.B. der Verarbeitungsstatus, Lieferadressen und Rechnungsadressen, Standorte und Lager.

## <a name="account-table"></a>Kontotabelle

1. Geben Sie in der Spalte **Unternehmen** den Namen des Unternehmens ein, z. B. **USMF**.
2. Geben Sie in der Spalte **Beziehungstyp** den Wert **Kunde** als einen statischen Wert ein. Möglicherweise möchten Sie in Ihrer Geschäftslogik nicht jeden Kontodatensatz als Kunden klassifizieren.
3. In der Spalte **Kundengruppen-ID** geben Sie die Nummer der Kundengruppe aus der App Finance und Operations ein. Der Standardwert aus der Prospect-to-Cash-Lösung ist **10**.
4. Wenn Sie die Prospect-to-Cash-Lösung ohne Anpassung von **Kontonummer** verwenden, geben Sie für **Kontonummer** in der Spalte **Parteinummer** einen Wert ein. Wenn es Anpassungen gibt und Sie die Nummer der Partei nicht kennen, ziehen Sie diese Information aus der Finance und Operations App.

## <a name="contact-table"></a>Kontakttabelle

1. Geben Sie in der Spalte **Unternehmen** den Namen des Unternehmens ein, z. B. **USMF**.
2. Legen Sie die folgenden Spalten basierend auf dem Wert **IsActiveCustomer** in der CSV-Datei fest:

    - Wenn **IsActiveCustomer** in der CSV-Datei auf **Ja** festgelegt ist, legen Sie die Spalte **Verkäuflich** auf **Ja** fest. In der Spalte **Kundengruppen-ID** geben Sie die Nummer der Kundengruppe aus der App Finance und Operations ein. Der Standardwert aus der Prospect-to-Cash-Lösung ist **10**.
    - Wenn **IsActiveCustomer** in der CSV-Datei auf **Nein** festgelegt ist, legen Sie die Spalte **Verkäuflich** auf **Nein** und die Spalte **Kontakt für** auf **Kunde** fest.

3. Wenn Sie die Prospect-to-Cash-Lösung ohne Anpassung von **Kontaktnummer** verwenden, legen Sie die folgenden Spalten fest:

    - Migrieren Sie die Kontaktnummer aus der CSV-Datei (**msdynce\_contactnumber**) in die Kontaktnummer in der Tabelle **Kontakt** (**msdyn\_contactnumber**).
    - Verwenden Sie Werte aus der Tabelle **Kontaktnummer** in der Spalte **Parteinummer**.
    - Verwenden Sie Werte aus der Tabelle **Kontaktnummer** in der Spalte **Kontonummer/Kontaktpersonkennung**.

## <a name="invoice-table"></a>Rechnungstabelle

Da die Daten aus der Tabelle **Rechnung** nur in eine Richtung fließen sollen, nämlich von der Finance und Operations-App zur Customer-Engagement-App, ist eine Initialisierung nicht erforderlich. Führen Sie die anfängliche Synchronisierung aus, um alle erforderlichen Daten aus der Finance und Operations-App in die Customer-Engagement-App zu migrieren. Weitere Informationen finden Sie unter [Überlegungen zur Erstsynchronisierung](initial-sync-guidance.md).

## <a name="order-table"></a>Auftragstabelle

1. Geben Sie in der Spalte **Unternehmen** den Namen des Unternehmens ein, z. B. **USMF**.
2. Kopieren Sie den Wert aus der Spalte **Auftragskennung** in der CSV-Datei in die Spalte **Auftragsnummer**.
3. Kopieren Sie den Wert aus der Spalte **Kunde** in der CSV-Datei in die Spalte **Rechnungskundennummer**.
4. Kopieren Sie den Wert aus der Spalte **Versand nach Land/Region** in der CSV-Datei in die Spalte **Versand nach Land/Region**. Beispiele für diesen Wert sind **USA** und **Vereinigte Staaten**.
5. Legen Sie den Wert der Spalte **Angefordertes Wareneingangsdatum** fest. Wenn Sie kein Eingangsdatum verwenden, verwenden Sie die Spalten **Angefordertes Lieferdatum**, **Datum erfüllt** und **Datum übermittelt** in der CSV-Datei. Ein Beispiel für diesen Wert ist **2020-03-27T00: 00: 00Z**.
6. Legen Sie den Wert der Spalte **Sprache** fest. Ein Beispiel für diesen Wert ist **en-us**.
7. Legen Sie den Wert der Spalte **Auftragstyp** fest, indem Sie die Spalte **Artikelbezogen** verwenden.

## <a name="order-products-table"></a>Auftragsproduktetabelle

- Geben Sie in der Spalte **Unternehmen** den Namen des Unternehmens ein, z. B. **USMF**.

## <a name="products-table"></a>Produktetabelle

Da die Daten aus der Tabelle **Produkte** in eine Richtung fließen sollen, nämlich von der Finance und Operations-App zur Customer-Engagement-App, ist eine Initialisierung nicht erforderlich. Führen Sie die anfängliche Synchronisierung aus, um alle erforderlichen Daten aus der Finance und Operations-App in die Customer-Engagement-App zu migrieren. Weitere Informationen finden Sie unter [Überlegungen zur Erstsynchronisierung](initial-sync-guidance.md).

## <a name="quote-and-quote-product-tables"></a>Anbegots- und Angebotsproduktetabellen

Befolgen Sie für die Tabelle **Angebot** die Anweisungen im Abschnitt [Auftragstabelle](#order-table) weiter oben in diesem Artikel. Befolgen Sie für die Tabelle **Angebotsprodukt** die Anweisungen im Abschnitt [Auftragsproduktetabelle](#order-products-table).


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
