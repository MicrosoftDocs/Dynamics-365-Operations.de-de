---
title: Kreditbrief exportieren
description: Diese Prozedur zeigt Ihnen den Prozess des Exportkreditbriefs.
author: kweekley
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, DefaultDashboard, SalesTableListPage, SalesCreateOrder, SalesTable, BankLCExport, SalesEditLines,  LedgerJournalTable, LedgerJournalTransCustPaym, CustOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 260ef2d05e1f21708817346af2db2841aa6acdd9
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834787"
---
# <a name="export-letter-of-credit"></a>Kreditbrief exportieren

[!include [banner](../../includes/banner.md)]

Diese Prozedur zeigt Ihnen den Prozess des Exportkreditbriefs.

Ein Kreditbrief stellt eine Vereinbarung dar, die von einer Bank ausgegeben wird. Darin gewährleistet die Bank die Zahlung im Auftrag des Einkäufers, sofern die Vertragsbedingungen zwischen Einkäufer und Verkäufer erfüllt sind.



Führen Sie die Prozedur "Einrichten der Bankfazilitäten und Buchungsprofile" und die Prozedur "Letter of Credit_Create a bank facility agreement" vor dieser Prozedur aus. Das Demo-Unternehmen USMF muss ausgewählt werden, um diese Prozedur erfolgreich ausführen.




## <a name="create-sales-order-for-export-letter-of-credit"></a>Erstellen eines Exportkreditbrief-Auftrags
1. Wechseln Sie zu "Debitoren" > "Aufträge" > "Alle Aufträge".
2. Klicken Sie auf "Neu".
3. Klicken Sie im Feld "Debitorenkonto" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
4. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
5. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
6. Erweitern oder reduzieren Sie den Abschnitt "Allgemein".
7. Klicken Sie im Feld "Standort" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
    * Wählen Sie den Standort, an dem der ausgegebene Artikel gelagert wird.  
8. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
9. Klicken Sie im Feld "Lagerort" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
    * Wählen Sie den Lagerort, an dem der ausgegebene Artikel gelagert wird.  
10. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
    * Hinweis: Wählen Sie im Feld "Bankdokumenttyp" den Wert "Kreditbrief" aus.  
11. Wählen Sie im Feld "Bankdokumenttyp" "Kreditbrief" aus.
12. Erweitern oder reduzieren Sie den Abschnitt 'Lieferung'.
    * Hinweis: Wählen Sie "Lieferdatumskontrolle = keine".  
13. Geben Sie im Feld "Angefordertes Wareneingangsdatum" ein Datum ein.
14. Klicken Sie auf "OK".
15. Klicken Sie im Feld "Artikelnummer" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
    * Wählen Sie den erforderlichen Artikel zur Entnahme/Verkauf.  
16. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
17. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
18. Geben Sie im Feld "Einzelpreis" eine Zahl ein.
19. Erweitern oder reduzieren Sie den Abschnitt "Positionsdetails".
20. Klicken Sie auf die Registerkarte "Lieferung".
21. Geben Sie im Feld "Angefordertes Lieferdatum" ein Datum ein.
22. Geben Sie im Feld "Bestätigtes Versanddatum" ein Datum ein.
23. Klicken Sie im Aktivitätsbereich auf Verwalten.
24. Klicken Sie Bankbürgschaft.
25. Geben Sie im Feld "Bankdokumentnummer" einen Wert ein.
26. Geben Sie im Feld "Ablaufdatum" ein Datum und eine Uhrzeit ein.
27. Erweitern oder reduzieren Sie den Abschnitt "Bankverbindung".
28. Klicken Sie im Feld "Ausgebende Bank" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
29. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
30. Klicken Sie im Feld "Avisierende Bank" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
31. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
32. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
33. Klicken Sie auf "Auftragslieferungen abrufen".
34. Klicken Sie auf "Bankdokument ausgeben".
35. Schließen Sie die Seite.

## <a name="post-packing-slip"></a>Lieferschein buchen
1. Klicken Sie im Aktivitätsbereich auf "Entnehmen und verpacken".
2. Klicken Sie auf "Lieferschein buchen".
3. Erweitern oder reduzieren Sie den Abschnitt "Parameter".
4. Wählen Sie im Feld "Menge" die Option "Alle" aus.
5. Erweitern oder reduzieren Sie den Abschnitt 'Einrichten'.
6. Geben Sie im Feld "Lieferscheindatum" ein Datum ein.
7. Wählen Sie eine Liefernummer.
8. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
9. Klicken Sie auf "OK".
10. Klicken Sie auf "OK".

## <a name="post-sales-invoice"></a>Verkaufsrechnung buchen.
1. Klicken Sie im Aktivitätsbereich auf "Rechnung".
2. Klicken Sie auf "Rechnung".
3. Erweitern oder reduzieren Sie den Abschnitt 'Überblick'.
4. Wählen Sie eine Liefernummer.
5. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
6. Erweitern oder reduzieren Sie den Abschnitt 'Einrichten'.
7. Geben Sie in das Feld "Rechnungsdatum" ein Datum ein.
8. Klicken Sie auf "OK".
9. Klicken Sie auf "OK".

## <a name="shipment-document-submitted-status"></a>Übermittelter Status der Lieferdokumente
1. Klicken Sie im Aktivitätsbereich auf Verwalten.
2. Klicken Sie Bankbürgschaft.
3. Erweitern oder reduzieren Sie den Abschnitt 'Positionen'.
    * Hinweis: Das Feld "Dokument übermittelt" sollte auf "Ja" festgelegt werden.  

## <a name="verify-export-letter-of-credit"></a>Exportkreditbrief überprüfen
1. Wechseln Sie zu "Bargeld- und Bankverwaltung" > "Kreditbrief" > "Exportkreditbrief und Importinkasso".
2. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
3. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
    * Vergewissern Sie sich, dass der Lieferstatus des Exportkreditbriefs auf" Fakturiert" steht.  

## <a name="customer-payment"></a>Debitorenzahlung
1. Wechseln Sie zu "Debitoren" > "Zahlungen" > "Zahlungserfassung".
2. Klicken Sie auf "Neu".
3. Markieren Sie in der Liste die ausgewählte Zeile.
4. Klicken Sie im Feld "Name" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
5. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
6. Klicken Sie auf Positionen.
7. Geben Sie ein Datum in das Feld "Datum" ein.
8. Geben Sie im Feld "Konto" die gewünschten Werte an.
9. Klicken Sie auf "Ausgleich".
10. Aktivieren Sie das Kontrollkästchen in der Kopfzeile von 'Summen'.
    * Hinweis: Legen Sie das Feld "Anzeigen"auf "Kreditbrief" fest.  
11. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
12. Aktivieren bzw. deaktivieren Sie das Kontrollkästchen 'Markieren'.
13. Klicken Sie auf "OK".
14. Klicken Sie auf die Registerkarte Zahlung.
    * Überprüfen Sie die Bankdokumentnummer und Liefernummerdetails.  
15. Klicken Sie auf "Buchen".

## <a name="verify-export-letter-of-credit-after-payment"></a>Überprüfen Sie den Exportkreditbrief nach der Zahlung.
1. Wechseln Sie zu "Bargeld- und Bankverwaltung" > "Kreditbrief" > "Exportkreditbrief und Importinkasso".
2. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
3. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
    * Überprüfen Sie, ob Lieferstatus = empfangene Zahlung und Saldobetrag = 0.00.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]