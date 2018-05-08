--- 
title: Akkreditiv importieren
description: Diese Prozedur zeigt Ihnen, wie Sie einen Kreditbrief importieren.
author: kweekley
manager: AnnBe
ms.date: 02/26/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 02be2627186a149a05eaccfa3e5906a9fe1d74dd
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="import-a-letter-of-credit"></a>Akkreditiv importieren

[!include [task guide banner](../../includes/task-guide-banner.md)]

Diese Prozedur zeigt Ihnen, wie Sie einen Kreditbrief importieren. Folgendes muss eingerichtet werden, bevor sie das Verfahren beginnen: - Bankfazilitäten, Buchungsprofile, eine Bankfazilitätsvereinbarung und die Bankdetails des Kreditors.

Für diese Prozedur wird das Demo-Unternehmen USMF verwendet.


## <a name="create-a-purchase-order-with-letter-of-credit"></a>Erstellen Sie eine Bestellung mit Kreditbrief.
1. Wechseln Sie zu "Kreditoren" > "Bestellungen" > "Alle Bestellungen".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Kreditorenkonto" einen Wert ein, oder wählen Sie einen Wert aus.
4. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
5. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
6. Erweitern Sie den Abschnitt "Allgemein".
7. Geben Sie im Feld "Standort" einen Wert ein, oder wählen Sie einen Wert aus.
8. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
9. Geben Sie im Feld 'Lagerort' einen Wert ein, oder wählen Sie einen Wert aus.
10. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
11. Geben Sie ein Datum in das Feld "Datum" ein.
12. Geben Sie im Feld "Lieferdatum" ein Datum ein.
    * Hinweis: Wählen Sie im Feld "Bankdokumenttyp" den Wert "Kreditbrief" aus.  
13. Klicken Sie auf "OK".
14. Geben Sie im Feld "Artikelnummer" einen Wert ein oder wählen Sie einen Wert aus.
15. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
16. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
17. Erweitern Sie den Abschnitt "Positionsdetails".
18. Klicken Sie auf die Registerkarte "Lieferung".
19. Geben Sie im Feld "Lieferdatum" ein Datum ein.
20. Geben Sie im Feld "Bestätigtes Lieferdatum" ein Datum ein.
21. Geben Sie im Feld "Preis je Einheit" eine Zahl ein.
    * Definieren Sie die Kreditbrief-Details.  
22. Klicken Sie im Aktivitätsbereich auf Verwalten.
23. Klicken Sie Kreditbrief/Importinkasso.
24. Geben Sie im Feld "Datum des Antrags" ein Datum und eine Uhrzeit ein.
    * Vergewissern Sie sich, dass im "Bankkonto" Feld das standardmäßig aktive Bankkonto steht, das auf dem Datum des Antrags basiert.  
25. Geben Sie im Feld "Bankdokumentnummer" einen Wert ein.
26. Geben Sie im Feld "Wareneingangsdatum" ein Datum und eine Uhrzeit ein.
27. Erweitern Sie den Abschnitt 'Bankdokument'.
28. Geben Sie im Feld "Ablaufdatum" ein Datum und eine Uhrzeit ein.
29. Erweitern Sie den Abschnitt 'Bankverbindung'.
30. Geben Sie im Feld 'Avisierende Bank' einen Wert ein, oder wählen Sie einen Wert aus.
31. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
32. Klicken Sie auf "Speichern".
33. Klicken Sie "Lieferungen von Bestellungen abrufen".
34. Schließen Sie die Seite.
35. Klicken Sie im Aktivitätsbereich auf "Einkauf".
36. Klicken Sie auf "Bestätigen".
37. Klicken Sie im Aktivitätsbereich auf Verwalten.
38. Klicken Sie Kreditbrief/Importinkasso.
39. Prozess anklicken.
40. Klicken Sie auf "Bestätigen".
    * Überprüfen Sie, ob der Fazilitätssaldo den Bestellbetrag verringert.  In diesem Beispiel ist der Einkaufsbetrag = 500.00, Einrichtungsgrenze = 10000.00 daher Einrichtungssaldo = 9500.00.  
41. Schließen Sie die Seite.
42. Geben Sie im Feld "Preis je Einheit" eine Zahl ein.
43. Klicken Sie auf "Speichern".
44. Klicken Sie im Aktivitätsbereich auf "Einkauf".
45. Klicken Sie auf "Bestätigen".
    * Ergänzen Sie den Kreditbrief aufgrund der Preisänderung je Einheit.  
46. Klicken Sie im Aktivitätsbereich auf Verwalten.
47. Klicken Sie Kreditbrief/Importinkasso.
    * Ergänzen Sie den Kreditbrief aufgrund der Preisänderung je Bestelleinheit.  
48. Prozess anklicken.
49. Klicken Sie auf "Ergänzen".
50. Klicken Sie auf "Entfernen".
51. Klicken Sie auf "Ja".
52. Klicken Sie "Lieferungen von Bestellungen abrufen".
53. Prozess anklicken.
54. Klicken Sie auf "Bestätigen".
    * Überprüfen Sie, ob der Fazilitätssaldo den Bestellbetrag verringert.  In diesem Beispiel ist der bearbeitete Einkaufsbetrag = 600.00, Fazilitätslimit= 10000.00 daher Fazilitätssaldo = 9400.00.  
55. Schließen Sie die Seite.

## <a name="post-packing-slip"></a>Lieferschein buchen
1. Klicken Sie im Aktivitätsbereich auf "Empfangen".
2. Klicken Sie auf "Produktzugang".
3. Geben Sie im Feld "PurchParmTable_Num" einen Wert ein.
    * Wählen Sie den Liefernummer aus, der mit Bezug auf den Kreditbrief erstellt wird.  
4. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
5. Geben Sie im Feld "Produktzugangsdatum" ein Datum ein.
6. Klicken Sie auf "OK".
7. Schließen Sie die Seite.
8. Schließen Sie die Seite.

## <a name="verify-import-letter-of-credit-status"></a>Überprüfen Sie den Status des Importkreditbriefs.
1. Wechseln Sie zu "Bargeld- und Bankverwaltung" > "Kreditbrief" > "Importkreditbrief und Importinkasso".
2. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
3. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
    * Überprüfen Sie den Importkreditbriefstatus.  
4. Schließen Sie die Seite.
5. Schließen Sie die Seite.

## <a name="post-purchase-invoice"></a>Einkaufsrechnung buchen
1. Wechseln Sie zu "Kreditoren" > "Bestellungen" > "Alle Bestellungen".
    * Wählen Sie die Bestellung aus, die mit Kreditbrief erstellt wurde.  
2. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
3. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
4. Klicken Sie im Aktivitätsbereich auf "Rechnung".
5. Klicken Sie auf "Rechnung".
6. Geben Sie im Feld "Zahl" einen Wert ein.
7. Geben Sie im Feld "Liefernummer" einen Wert ein oder wählen Sie einen Wert aus.
8. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
9. Geben Sie in das Feld "Rechnungsdatum" ein Datum ein.
10. Klicken Sie auf "Status des Abgleichs aktualisieren".
11. Klicken Sie auf "Buchen".
12. Schließen Sie die Seite.
13. Schließen Sie die Seite.

## <a name="verify-import-letter-of-credit-status"></a>Überprüfen Sie den Status des Importkreditbriefs.
1. Wechseln Sie zu "Bargeld- und Bankverwaltung" > "Kreditbrief" > "Importkreditbrief und Importinkasso".
2. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
3. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
    * Überprüfen Sie den Importkreditbrief2.  
    * Überprüfen Sie: Lieferstatus = fakturierte Bankfazilitätsdetails  
4. Klicken Sie auf "Ansicht".
5. Klicken Sie auf "Antrag drucken".
6. Klicken Sie auf "OK".
    * Vergewissern Sie sich, dass der Kreditbriefantrag gedruckt wird.  
7. Schließen Sie die Seite.
8. Schließen Sie die Seite.
9. Schließen Sie die Seite.

## <a name="post-vendor-payment-journal-for-the-created-purchase-invoice-with-letter-of-credit"></a>Buchen Sie Kreditorenzahlungserfassung für die erstellte Einkaufsrechnung mit Kreditbrief.
1. Wechseln Sie zu "Kreditoren" > "Zahlungen" > "Zahlungserfassung".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Name" einen Wert ein, oder wählen Sie einen Wert aus.
4. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
5. Klicken Sie auf Positionen.
6. Geben Sie ein Datum in das Feld "Datum" ein.
7. Geben Sie im Feld "Konto" die gewünschten Werte an.
8. Klicken Sie auf Transaktionen ausgleichen.
9. Erweitern Sie den Abschnitt "Summen".
10. Wählen Sie im Feld 'Anzeigen:' eine Option aus.
    * Überprüfen Sie, ob die Felder "Bankdokumentnummer" und "Liefernummer" aktualisiert wurden.  
11. Wählen Sie das Kontrollkästchen "Markieren" aus.
12. Klicken Sie auf "OK".
13. Klicken Sie auf die Registerkarte Zahlung.
    * Überprüfen Sie, ob die Felder "Bankdokumentnummer" und "Liefernummer" aktualisiert wurden.  
14. Klicken Sie auf "Buchen".
15. Schließen Sie die Seite.
16. Schließen Sie die Seite.

## <a name="verify-import-letter-of-credit-status-after-invoice-paid"></a>Überprüfen Sie den Status des Importkreditbriefs nach gezahlter Rechnung.
1. Wechseln Sie zu "Bargeld- und Bankverwaltung" > "Kreditbrief" > "Importkreditbrief und Importinkasso".
2. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
3. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
    * Überprüfen Sie den Importkreditbriefstatus.   
4. Schließen Sie die Seite.

## <a name="verify-the-bank-facility-limit-and-utilization-report"></a>Überprüfen Sie das Bankfazilitätslimit und den Auslastungsbericht.
1. Wechseln Sie zu "Bargeld und Bankverwaltung" > "Abfragen und Berichte" > "Kreditbrief oder Garantie" > "Bankfazilitäten und Auslastungsbericht".
2. Erweitern Sie den Abschnitt "Einzuschließende Datensätze".
3. Klicken Sie auf "Filter".
    * Definieren Sie das Feld "Kriterien" über das erforderliche Bankkonto.  
4. Geben Sie im Feld "Kriterien" einen Wert ein oder wählen Sie einen Wert aus.
5. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
6. Klicken Sie auf "OK".
7. Klicken Sie auf "OK".
    * Überprüfen Sie den Bericht, in dem die Transaktionen aufgelistet werden.  
    * Überprüfen Sie, ob der Bericht Transaktionen mit Bankdokumentnummer, Einrichtungsgrenze, Auslastungsbetrag und dem Einrichtungsbilanzbetrag auflistet.  
8. Schließen Sie die Seite.


