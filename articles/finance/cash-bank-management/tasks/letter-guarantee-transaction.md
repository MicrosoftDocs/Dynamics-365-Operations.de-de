---
title: Bankgarantiebuchung
description: Diese Prozedur führt Sie Schritt für Schritt durch den Garantiebriefprozess.
author: kweekley
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: Reasons, SalesTableListPage, SalesCreateOrder, SalesTable, BankLGRequestForm, BankLGRequestFormRequest, BankLGGuarantee, BankLGFormSubmitToBank, BankDocumentAgreementLineLookup, BankLGFormReceiveFromBank, LedgerJournalTable, LedgerJournalTransDaily, BankLGRequestFormGiveToBeneficiary, BankLGFormGiveToBeneficiary, BankLGRequestFormIncreaseValue, BankLGFormIncreaseValue, BankLGRequestFormLiquidate, BankLGFormLiquidate
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 089515287fc5706983b10614f69b4b1cd90178c5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834715"
---
# <a name="letter-of-guarantee-transaction"></a>Bankgarantiebuchung

[!include [banner](../../includes/banner.md)]

Diese Prozedur führt Sie Schritt für Schritt durch den Garantiebriefprozess.



Schließen Sie folgende Aufgaben ab, bevor Sie diese starten:

- Einrichten der Bankfazilitäten und Buchungsprofile für eine Bankgarantie.

- Erstellen einer Bankfazilitätsvereinbarung für einen Garantiebrief.



Für diese Prozedur wird das Demo-Unternehmen USMF verwendet.


## <a name="create-sales-order-with-letter-of-guarantee"></a>Auftrag mit Garantiebrief erstellen
1. Wechseln Sie zu "Debitoren" > "Aufträge" > "Alle Aufträge".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Debitorenkonto" einen Wert ein oder wählen Sie einen Wert aus.
4. Erweitern Sie den Abschnitt "Allgemein".
5. Geben Sie im Feld "Standort" einen Wert ein, oder wählen Sie einen Wert aus.
6. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
7. Geben Sie im Feld 'Lagerort' einen Wert ein, oder wählen Sie einen Wert aus.
8. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
9. Wählen Sie im Feld "Bankdokumenttyp" "Garantiebrief" aus.
10. Klicken Sie auf "OK".
11. Geben Sie im Feld "Artikelnummer" einen Wert ein oder wählen Sie einen Wert aus.
12. Geben Sie im Feld "Preis je Einheit" eine Zahl ein.
13. Erweitern Sie den Abschnitt "Positionsdetails".
14. Klicken Sie auf die Registerkarte "Lieferung".
    * Hinweis: Wählen Sie "Lieferdatumskontrolle = keine"  
15. Geben Sie im Feld "Angefordertes Lieferdatum" ein Datum ein.
16. Geben Sie im Feld "Bestätigtes Versanddatum" ein Datum ein.

## <a name="process-letter-of-guarantee_request"></a>letter of guarantee_Request verarbeiten
1. Klicken Sie im Aktivitätsbereich auf Verwalten.
2. Klicken Sie "Garantiebrief".
3. Klicken Sie im Aktivitätsbereich auf Garantiebrief.
4. Klicken Sie "Anforderung" zum Öffnen des Dropdown-Dialogfelds.
5. Geben Sie im Typfeld einen Wert ein, oder wählen Sie einen Wert aus.
6. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
7. Geben Sie im Feld "Wert" eine Zahl ein.
8. Geben Sie im Feld "Ablaufdatum" ein Datum und eine Uhrzeit ein.
9. Klicken Sie auf "OK".
10. Schließen Sie die Seite.

## <a name="process-letter-of-guarantee_submit-to-bank"></a>letter of guarantee_Submit to bank verarbeiten
1. Wechseln Sie zu "Bargeld- und Bankverwaltung" > "Garantiebriefe" > "Garantiebriefe".
2. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
3. Klicken Sie auf "An Bank übermitteln", um das Dialogfeld zu öffnen.
4. Geben Sie im Feld 'Bankkonto' einen Wert ein, oder wählen Sie einen Wert aus.
5. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
6. Klicken Sie auf "OK".

## <a name="process-letter-of-guarantee_receive-from-bank"></a>letter of guarantee_Receive from bank verarbeiten
1. Klicken Sie auf "Von Bank empfangen", um das Dialogfeld zu öffnen.
2. Geben Sie im Feld "Banknummer" einen Wert ein.
    * Überprüfen Sie die Werte in den berechneten Gewinnspannen- und Ausgabenfeldern.  
3. Klicken Sie auf "OK".
4. Erweitern Sie den Abschnitt "Aktionen".
    * Überprüfen Sie den "Von Bank empfangen" Datensatz.  
5. Klicken Sie, um dem Link im Feld "Lfd. Nummer" zu folgen.
6. Klicken Sie auf "Positionen".
    * Überprüfen Sie die Buchung der Erfassungseinträge.  
7. Schließen Sie die Seite.

## <a name="process-letter-of-guarantee_give-to-beneficiary"></a>letter of guarantee_Give to beneficiary verarbeiten
1. Wechseln Sie zu "Debitoren" > "Aufträge" > "Alle Aufträge".
2. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
3. Klicken Sie im Aktivitätsbereich auf Verwalten.
4. Klicken Sie "Garantiebrief".
5. Klicken Sie im Aktivitätsbereich auf Garantiebrief.
6. Klicken Sie auf "An Begünstigten übergeben", um das Dialogfeld zu öffnen.
7. Klicken Sie auf "OK".
8. Wechseln Sie zu "Bargeld- und Bankverwaltung" > "Garantiebriefe" > "Garantiebriefe".
9. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
10. Klicken Sie auf "An Begünstigten übergeben", um das Dialogfeld zu öffnen.
11. Klicken Sie auf "OK".
12. Erweitern Sie den Abschnitt "Aktionen".
    * Überprüfen Sie den "An Begünstigten übergeben" Datensatz.  

## <a name="process-letter-of-guarantee_increase-value"></a>letter of guarantee_Increase value verarbeiten
1. Wechseln Sie zu "Debitoren" > "Aufträge" > "Alle Aufträge".
2. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
3. Klicken Sie im Aktivitätsbereich auf Verwalten.
4. Klicken Sie "Garantiebrief".
5. Klicken Sie im Aktivitätsbereich auf Garantiebrief.
6. Klicken Sie zum Öffnen des Dropdown-Dialogfelds auf "Wert erhöhen".
7. Geben Sie eine Zahl in das Feld "Hinzuzufügender Wert" ein.
8. Klicken Sie auf "OK".
9. Wechseln Sie zu "Bargeld- und Bankverwaltung" > "Garantiebriefe" > "Garantiebriefe".
10. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
11. Klicken Sie zum Öffnen des Dropdown-Dialogfelds auf "Wert erhöhen".
12. Klicken Sie auf "OK".
13. Erweitern Sie den Abschnitt "Aktionen".
    * Überprüfen Sie den "Wert erhöhen" Datensatz.  
14. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
15. Klicken Sie, um dem Link im Feld "Lfd. Nummer" zu folgen.
16. Klicken Sie auf "Positionen".
    * Überprüfen Sie die gebuchten Erfassungseinträge.  

## <a name="process-letter-of-guarantee_liquidate"></a>letter of guarantee_Liquidate verarbeiten
1. Wechseln Sie zu "Debitoren" > "Aufträge" > "Alle Aufträge".
2. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
3. Klicken Sie im Aktivitätsbereich auf Verwalten.
4. Klicken Sie "Garantiebrief".
5. Klicken Sie im Aktivitätsbereich auf Garantiebrief.
6. Klicken Sie zum Öffnen des Dropdown-Dialogfelds auf "Liquidieren".
7. Klicken Sie auf "OK".
8. Wechseln Sie zu "Bargeld- und Bankverwaltung" > "Garantiebriefe" > "Garantiebriefe".
9. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
10. Klicken Sie zum Öffnen des Dropdown-Dialogfelds auf "Liquidieren".
11. Klicken Sie auf "OK".
12. Erweitern Sie den Abschnitt "Aktionen".
    * Überprüfen Sie den "Liquidieren" Datensatz.  
13. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
14. Klicken Sie, um dem Link im Feld "Lfd. Nummer" zu folgen.
15. Klicken Sie auf "Positionen".
    * Überprüfen Sie die gebuchten Erfassungseinträge.  
16. Schließen Sie die Seite.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]