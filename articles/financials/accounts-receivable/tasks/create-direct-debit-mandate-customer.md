--- 
title: "Direkteinzugsmandat für einen Debitor erstellen"
description: "Diese Aufgabenanleitung veranschaulicht, wie eine Einzugsermächtigung erstellt und in einer Rechnung verwendet wird."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 10/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: d01c7c19925a3c7064ab3f845b92b610b162066c
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-direct-debit-mandate-for-a-customer"></a>Direkteinzugsmandat für einen Debitor erstellen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Diese Aufgabenanleitung veranschaulicht, wie eine Einzugsermächtigung erstellt und in einer Rechnung verwendet wird.


## <a name="create-a-bank-account"></a>Bankkonto erstellen
1. Wechseln Sie zu "Debitoren" > "Debitoren" > "Alle Debitoren".
2. Wählen Sie z. B. "US-001" aus.
3. Klicken Sie im Aktivitätsbereich auf "Debitor".
4. Klicken Sie auf Bankkonten.
5. Klicken Sie auf "Neu".
6. Geben Sie im Feld "Bankkonto" einen Wert ein.
7. Geben Sie im Feld "Name" einen Wert ein.
8. Geben Sie im Feld "IBAN" einen Wert ein.
9. Geben Sie im Feld "Währung" einen Wert ein.
10. Klicken Sie auf "Speichern".
11. Schließen Sie die Seite.
12. Gehen Sie zu "Bargeld- und Bankverwaltung" > Bankkonten > Bankkonten.
13. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
14. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
15. Klicken Sie auf "Bearbeiten".
16. Erweitern Sie den Abschnitt "Zusätzliche Kennung".
17. Geben Sie im Feld "Bankeinzugskennung" einen Wert ein.
18. Geben Sie im Feld "IBAN" einen Wert ein.
19. Schließen Sie die Seite.
20. Schließen Sie die Seite.

## <a name="define-the-electronic-payment-method"></a>Elektronische Zahlungsmethode definieren
1. Wechseln Sie zu "Debitoren" > "Zahlungseinstellungen" > "Zahlungsmethoden".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Zahlungsmethode" einen Wert ein.
4. Geben Sie im Feld "Beschreibung" einen Wert ein.
5. Der Zahlungstyp für eine Einzugsermächtigungs-Zahlungsmethode muss "Elektronische Zahlung" sein.
6. Wählen Sie "Ja" im Feld "Mandat anfordern" aus.
7. Schließen Sie die Seite.

## <a name="add-a-direct-debit-mandate-to-a-customer"></a>Direkteinzugsmandat einem Debitor hinzufügen.
1. Wechseln Sie zu "Debitoren" > "Debitoren" > "Alle Debitoren".
2. Wählen Sie z. B. "US-001" aus.
3. Klicken Sie auf "Bearbeiten".
4. Erweitern Sie den Abschnitt "Zahlungsausfälle".
5. Geben Sie im Feld "Zahlungsmethode" einen Wert ein, oder wählen Sie einen Wert aus.
6. Erweitern Sie den Abschnitt "Zahlungsausfälle".
7. Erweitern Sie den Abschnitt "Einzugsermächtigungen".
8. Klicken Sie auf Hinzufügen.
9. Geben Sie im Feld 'Bankkonto' einen Wert ein, oder wählen Sie einen Wert aus.
10. Geben Sie im Feld 'Kreditorenbankkonto' einen Wert ein, oder wählen Sie einen Wert aus.
11. Geben Sie die Anzahl der Zahlungen ein, deren Verarbeitung Sie für diese Vollmacht erwarten.
12. Klicken Sie auf "OK".
13. Klicken Sie auf Drucken.
14. Klicken Sie auf "Vollmachtsbericht".
15. Schließen Sie die Seite.
16. Klicken Sie auf "Bearbeiten".
17. Geben Sie im Feld "Unterschriftsdatum" ein Datum ein.
18. Klicken Sie auf "Ja".
19. Geben Sie den Ort ein, an dem die Vollmacht unterzeichnet wurde.
20. Klicken Sie auf "OK".
21. Schließen Sie die Seite.

## <a name="create-a-free-text-invoice-with-mandate"></a>Freitextrechnung mit Vollmacht erstellen
1. Wechseln Sie zu "Debitoren" > "Rechnungen" > "Alle Freitextrechnungen".
2. Klicken Sie auf "Neu".
3. Wählen Sie den Debitor aus, dem Sie die Vollmacht hinzugefügt haben.
4. Geben Sie im Feld "Direkteinzugsmandats-ID" einen Wert ein, oder wählen Sie einen Wert aus.


