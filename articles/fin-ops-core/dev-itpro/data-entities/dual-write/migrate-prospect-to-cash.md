---
title: Migrieren von Prospect-to-Cash-Daten vom Datenintegrator nach Dual-Write
description: In diesem Thema wird beschrieben, wie man Prospect-to-Cash-Daten vom Datenintegrator nach Dual-Write migriert.
author: RamaKrishnamoorthy
ms.date: 01/04/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: d216f1c46aa3362730c126ffc33fefdddddf1853
ms.sourcegitcommit: 259ba130450d8a6d93a65685c22c7eb411982c92
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/24/2021
ms.locfileid: "7416376"
---
# <a name="migrate-prospect-to-cash-data-from-data-integrator-to-dual-write"></a>Migrieren von Prospect-to-Cash-Daten vom Datenintegrator nach Dual-Write

[!include [banner](../../includes/banner.md)]

Um Ihre Prospect-to-Cash-Daten vom Datenintegrator nach Dual-Write zu migrieren, führen Sie die folgenden Schritte aus.

1. Führen Sie die Prostpect-to-Cash-Aufträge des Datenintegrators aus, um eine letzte vollständige Synchronisierung durchzuführen. Auf diese Weise stellen Sie sicher, dass beide Systeme (Finance and Operations-App und Customer Engagement-App) über alle Daten verfügen.
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
5. Stellen Sie für eine oder mehrere juristische Personen eine Dual-Write-Verbindung zwischen der Finance and Operations-App und der Customer Engagement-App her.
6. Aktivieren Sie Tabellenzuordnungen für duales Schreiben und führen Sie die erste Synchronisierung für die erforderlichen Referenzdaten aus. (Weitere Informationen finden Sie unter [Überlegungen zur Erstsynchronisierung](initial-sync-guidance.md).) Beispiele für erforderliche Daten sind Kundengruppen, Zahlungsbedingungen und Zahlungspläne. Aktivieren Sie die Zuordnungen für duales Schreiben nicht für Tabellen, für die eine Initialisierung erforderlich ist, z. B. Konto-, Angebots-, Angebotspositions-, Auftrags- und Auftragspositionstabellen.
7. Wechseln Sie in der Customer Engagement-App zu **Erweiterte Einstellungen \> Systemeinstellungen \> Datenverwaltung \> Erkennungsregeln für Duplikate** und deaktivieren Sie alle Regeln.
8. Initialisieren Sie die in Schritt 2 aufgeführten Tabellen. Anweisungen finden Sie in den verbleibenden Abschnitten dieses Themas.
9. Öffnen Sie die Finance and Operations-App und aktivieren Sie die Tabellenzuordnungen, z. B. die Tabellenzuordnungen für Konten, Angebote, Angebotspositionen, Aufträge und Auftragspositionen. Führen Sie anschließend die Erstsynchronisierung durch. (Weitere Informationen finden Sie unter [Überlegungen zur Erstsynchronisierung](initial-sync-guidance.md) .) Dieser Prozess synchronisiert zusätzliche Informationen aus der Finance and Operations-App, wie z. B. Verarbeitungsstatus, Versand- und Rechnungsadressen, Standorte und Lagerorte.

## <a name="account-table"></a>Kontotabelle

1. Geben Sie in der Spalte **Unternehmen** den Namen des Unternehmens ein, z. B. **USMF**.
2. Geben Sie in der Spalte **Beziehungstyp** den Wert **Kunde** als einen statischen Wert ein. Möglicherweise möchten Sie in Ihrer Geschäftslogik nicht jeden Kontodatensatz als Kunden klassifizieren.
3. Geben Sie in der Spalte **Kundengruppenkennung** die Kundengruppennummer aus der Finance and Operations-App ein. Der Standardwert aus der Prospect-to-Cash-Lösung ist **10**.
4. Wenn Sie die Prospect-to-Cash-Lösung ohne Anpassung von **Kontonummer** verwenden, geben Sie für **Kontonummer** in der Spalte **Parteinummer** einen Wert ein. Wenn Anpassungen vorgenommen wurden und Sie die Parteinummer nicht kennen, beschaffen Sie sich diese Informationen aus der Finance and Operations-App.

## <a name="contact-table"></a>Kontakttabelle

1. Geben Sie in der Spalte **Unternehmen** den Namen des Unternehmens ein, z. B. **USMF**.
2. Legen Sie die folgenden Spalten basierend auf dem Wert **IsActiveCustomer** in der CSV-Datei fest:

    - Wenn **IsActiveCustomer** in der CSV-Datei auf **Ja** festgelegt ist, legen Sie die Spalte **Verkäuflich** auf **Ja** fest. Geben Sie in der Spalte **Kundengruppenkennung** die Kundengruppennummer aus der Finance and Operations-App ein. Der Standardwert aus der Prospect-to-Cash-Lösung ist **10**.
    - Wenn **IsActiveCustomer** in der CSV-Datei auf **Nein** festgelegt ist, legen Sie die Spalte **Verkäuflich** auf **Nein** und die Spalte **Kontakt für** auf **Kunde** fest.

3. Wenn Sie die Prospect-to-Cash-Lösung ohne Anpassung von **Kontaktnummer** verwenden, legen Sie die folgenden Spalten fest:

    - Migrieren Sie die Kontaktnummer aus der CSV-Datei (**msdynce\_contactnumber**) in die Kontaktnummer in der Tabelle **Kontakt** (**msdyn\_contactnumber**).
    - Verwenden Sie Werte aus der Tabelle **Kontaktnummer** in der Spalte **Parteinummer**.
    - Verwenden Sie Werte aus der Tabelle **Kontaktnummer** in der Spalte **Kontonummer/Kontaktpersonkennung**.

## <a name="invoice-table"></a>Rechnungstabelle

Da die Daten aus der Tabelle **Rechnung** so konzipiert sind, dass sie nur in eine Richtung fließen, nämlich von der Finance and Operations-App zur Customer Engagement-App, ist keine Initialisierung erforderlich. Führen Sie die Erstsynchronisierung durch, um alle erforderlichen Daten von der Finance and Operations-App zur Customer Engagement-App zu migrieren. Weitere Informationen finden Sie unter [Überlegungen zur Erstsynchronisierung](initial-sync-guidance.md).

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

Da die Daten aus der Tabelle **Produkte** so konzipiert sind, dass sie nur in eine Richtung fließen, nämlich von der Finance and Operations-App zur Customer Engagement-App, ist keine Initialisierung erforderlich. Führen Sie die Erstsynchronisierung durch, um alle erforderlichen Daten von der Finance and Operations-App zur Customer Engagement-App zu migrieren. Weitere Informationen finden Sie unter [Überlegungen zur Erstsynchronisierung](initial-sync-guidance.md).

## <a name="quote-and-quote-product-tables"></a>Anbegots- und Angebotsproduktetabellen

Befolgen Sie für die Tabelle **Angebot** die Anweisungen im Abschnitt [Auftragstabelle](#order-table) weiter oben in diesem Thema. Befolgen Sie für die Tabelle **Angebotsprodukt** die Anweisungen im Abschnitt [Auftragsproduktetabelle](#order-products-table).


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]