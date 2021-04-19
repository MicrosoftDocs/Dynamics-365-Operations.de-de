---
title: Direkteinzugsmandat für einen Debitor erstellen
description: Diese Aufgabenanleitung veranschaulicht, wie eine Einzugsermächtigung erstellt und in einer Rechnung verwendet wird.
author: ShivamPandey-msft
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, BankAccountTable, CustPaymMode, CustDirectDebitMandate, BankAccountTableLookUp, SrsReportViewerForm,  LogisticsAddressCityLookup, CustFreeInvoice, CustTableLookup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e3bbf3703941255dfd82b8fb501ba8a9d1f3a2ec
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5835075"
---
# <a name="create-a-direct-debit-mandate-for-a-customer"></a>Direkteinzugsmandat für einen Debitor erstellen

[!include [banner](../../includes/banner.md)]

Diese Aufgabenanleitung veranschaulicht, wie eine Einzugsermächtigung erstellt und in einer Rechnung verwendet wird.


## <a name="create-a-bank-account"></a>Bankkonto erstellen
1. Wechseln Sie im **Navigationsbereich** zu **Module > Debitoren > Debitoren > Alle Debitoren**.
2. Wählen Sie in der Liste einen Datensatz aus. Wählen Sie z. B. "US-001" aus.
3. Klicken Sie im Aktivitätsbereich **Debitor**.
4. Klicken Sie auf **Bankkonten**.
5. Klicken Sie auf **Neu**.
6. Geben Sie im Feld **Bankkonto** einen Wert ein.
7. Geben Sie im Feld **Name** einen Wert ein.
8. Geben Sie im Feld **IBAN** einen Wert ein.
9. Geben Sie im Feld **Währung** einen Wert ein.
10. Klicken Sie auf **Speichern**.
11. Schließen Sie die Seite.
12. Gehen Sie im **Navigationsbereich** zu **Module > Bargeld- und Bankverwaltung > Bankkonten > Bankkonten**.
13. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
14. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
15. Klicken Sie auf **Bearbeiten**.
16. Erweitern Sie das Inforegister **Zusätzliche Kennung**.
17. Geben Sie im Feld **Bankeinzugskennung** einen Wert ein.
18. Geben Sie im Feld **IBAN** einen Wert ein.
19. Schließen Sie die Seite.
20. Schließen Sie die Seite.

## <a name="define-the-electronic-payment-method"></a>Elektronische Zahlungsmethode definieren
1. Wechseln Sie im **Navigationsbereich** zu **Module > Debitoren > Zahlungseinstellungen > Zahlungsmethoden**.
2. Klicken Sie auf **Neu**.
3. Geben Sie im Feld **Zahlungsmethode** einen Wert ein.
4. Geben Sie im Feld **Beschreibung** einen Wert ein.
5. Geben Sie im Feld **Zahlungstyp** 'Elektronischer Zahlungsverkehr' ein. Der Zahlungstyp für eine Einzugsermächtigungs-Zahlungsmethode muss "Elektronische Zahlung" sein.
6. Wählen Sie „Ja“ im Feld **Mandat anfordern** aus.
7. Schließen Sie die Seite.

## <a name="add-a-direct-debit-mandate-to-a-customer"></a>Direkteinzugsmandat einem Debitor hinzufügen.
1. Wechseln Sie im **Navigationsbereich** zu **Module > Debitoren > Debitoren > Alle Debitoren**.
2. Wählen Sie in der Liste einen Datensatz aus. Wählen Sie z. B. "US-001" aus.
3. Klicken Sie auf **Bearbeiten**.
4. Erweitern Sie das Inforegister **Zahlungsausfälle**.
5. Geben Sie im Feld **Zahlungsmethode** einen Wert ein, oder wählen Sie einen Wert aus.
6. Erweitern Sie das Inforegister **Zahlungsausfälle**.
7. Erweitern Sie das Inforegister **Einzugsermächtigungen**.
8. Klicken Sie auf **Hinzufügen**.
9. Geben Sie im Feld **Bankkonto** einen Wert ein, oder wählen Sie einen Wert aus.
10. Geben Sie im Feld **Kreditorenbankkonto** einen Wert ein, oder wählen Sie einen Wert aus.
11. Geben Sie im Feld **Zahlungshäufigkeit** die Anzahl der Zahlungen ein, deren Verarbeitung Sie für diese Vollmacht erwarten.
12. Klicken Sie auf **OK**.
13. Klicken Sie auf **Drucken**.
14. Klicken Sie auf **Vollmachtsbericht**.
15. Schließen Sie die Seite.
16. Klicken Sie auf **Bearbeiten**.
17. Geben Sie im Feld **Unterschriftsdatum** ein Datum ein.
18. Klicken Sie auf **Ja**.
19. Geben Sie den Ort ein, an dem die Vollmacht unterzeichnet wurde.
20. Klicken Sie auf **OK**.
21. Schließen Sie die Seite.

## <a name="create-a-free-text-invoice-with-mandate"></a>Freitextrechnung mit Vollmacht erstellen
1. Wechseln Sie im **Navigationsbereich** zu **Module > Debitoren > Rechnungen > Alle Freitextrechnungen**.
2. Klicken Sie auf **Neu**.
3. Wählen Sie den Debitor aus, dem Sie die Vollmacht hinzugefügt haben.
4. Geben Sie im Feld **Direkteinzugsmandats-ID** einen Wert ein, oder wählen Sie einen Wert aus.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]