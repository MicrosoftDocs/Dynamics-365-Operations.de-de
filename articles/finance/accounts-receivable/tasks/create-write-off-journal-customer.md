---
title: Eine Abschreibungserfassung für einen Debitor erstellen
description: In diesem Aufgabenhandbuch wird dargestellt, wie Sie die Parameter für Abschreibungen einrichten und dann Abschreibungstransaktionen auf der Seite "Inkassi", der Seite "Offene Debitorenrechnungen" und auf der Seite "Debitoren" abschreiben.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustParameters, CustPosting, DefaultDashboard, CustCollectionsPoolsListPage, CustWriteOff, LedgerJournalTable, LedgerJournalTransDaily, CustCollections, CustOpenInvoicesListPage, CustTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dd97f91f1ba53b56150b556fffdfed10a0c8911a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4443683"
---
# <a name="create-a-write-off-journal-for-a-customer"></a>Eine Abschreibungserfassung für einen Debitor erstellen

[!include [banner](../../includes/banner.md)]

In diesem Aufgabenhandbuch wird dargestellt, wie Sie die Parameter für Abschreibungen einrichten und dann Abschreibungstransaktionen auf der Seite "Inkassi", der Seite "Offene Debitorenrechnungen" und auf der Seite "Debitoren" abschreiben. Für diese Aufgabe wird das Demo-Unternehmen USMF verwendet.


## <a name="set-up-the-write-off-parameters"></a>Abschreibungsparameter einrichten
1. Wechseln Sie zu **Navigationsbereich > Module > Kredit und Inkasso > Einstellungen > Debitorenparameter**.
2. Klicken Sie auf die Registerkarte **Inkassi**.
3. Erweitern oder reduzieren Sie den Abschnitt **Abschreiben**.
    - Die **Abschreibungserfassung** ist die allgemeine Erfassung, die die Abschreibungsbuchungen enthält, die Sie erstellen.  
    - Sie können einen Ursachencode zu jeder Abschreibung zuordnen. Sie können diesen Standardwert in der Erfassung zum Zeitpunkt der Abschreibung übergehen.  
    - Legen Sie **Separate Mehrwertsteuer** auf „Ja“ fest, wenn Sie die Mehrwertsteuer aus der ursprünglichen Transaktion in der Abschreibung trennen möchten.  
4. Schließen Sie die Seite.
5. **Wechseln Sie zu "Kredit und Inkasso > Einstellungen > Debitorenbuchungsprofile**. Das Abschreibungskonto wird als die Ausgabenkonto- oder Rücklageregulierung in der allgemeinen Erfassung verwendet.
6. Schließen Sie die Seite.

## <a name="write-off-a-customer-balance-from-the-aged-balances-page"></a>Debitorensaldo auf der Seite "Saldenrückblick" abschreiben
1. Wechseln Sie zu **Kredit und Inkasso > Inkassi > Saldenrückblick**.
2. Markieren Sie die Zeile für den Debitor, den Sie abschreiben möchten. Markieren Sie z. B. die Position mit Birch Company.
3. Klicken Sie im **Aktivitätsbereich** auf **Sammeln**.
4. Klicken Sie auf **Abschreiben**.
5. Klicken Sie auf **OK**.
6. Schließen Sie die Seite.
7. Gehen Sie zu **Navigationsbereich > Module > Hauptbuch > Journaleinträge > Allgemeine Erfassungen**.
8. Wählen Sie die Nummer der Stapelverarbeitungserfassung für die Erfassung aus, die die Abschreibung enthält. Eine Position wird erstellt, um den Debitorensaldo umzukehren. Eine oder mehrere Positionen werden erstellt, um die Abschreibung auf dem Abschreibungskonto zu buchen.  
9. Schließen Sie die Seite.
10. Schließen Sie die Seite.

## <a name="write-off-transactions-from-the-collections-form"></a>Transaktionen aus dem Inkassoformular abschreiben.
1. Wechseln Sie zu **Kredit und Inkasso > Inkassi > Saldenrückblick**.
2. Wählen Sie den Namen des Debitors aus, der die Transaktionen beinhaltet, die Sie abschreiben möchten. Wählen Sie beispielsweise Cave Wholesales (US-004).
3. Zeile für erste Transaktion markieren.
4. Zeile für zweite Transaktion markieren.
5. Klicken Sie auf **Abschreiben**.
6. Geben Sie im Feld **Kommentar zur Ursache** „Uneinbringliche Außenstände“ ein.
7. Klicken Sie auf **OK**.
8. Schließen Sie die Seite.
9. Schließen Sie die Seite.
10. Wechseln Sie zu **Hauptbuch > Journaleinträge > Allgemeine Erfassungen**.
11. Wählen Sie die Nummer der Stapelverarbeitungserfassung für die Erfassung aus, die die Abschreibung enthält. Eine Position wird erstellt, um den Debitorensaldo umzukehren. Eine oder mehrere Positionen werden erstellt, um die Abschreibung auf dem Abschreibungskonto zu buchen.  
12. Schließen Sie die Seite.
13. Schließen Sie die Seite.

## <a name="write-off-an-invoice-from-the-open-customers-invoices-page"></a>Rechnung auf der Seite der offenen Debitorenrechnungsseite abschreiben
1. Wechseln Sie zu **Navigationsbereich > Module > Debitoren > Rechnungen > Offene Debitorenrechnungen**.
2. Markieren Sie die Position für eine Rechnung. Markieren Sie z. B. die Position für CIV-000667.
3. Klicken Sie im **Aktivitätsbereich** auf **Rechnung**.
4. Klicken Sie auf **Abschreiben**.
5. Klicken Sie auf **OK**.
6. Schließen Sie die Seite.

## <a name="write-off-a-customer-balance-from-the-customer-page"></a>Saldo eines Debitors auf der Seite "Debitoren" abschreiben
1. Wechseln Sie zu **Debitoren > Debitoren > Alle Debitoren**.
2. Dient zum Auswählen eines Debitorenkontos. Wählen Sie beispielsweise US-001 (Contoso Retail San Diego).
3. Klicken Sie im **Aktivitätsbereich** auf **Sammeln**.
4. Klicken Sie auf **Abschreiben**.
5. Klicken Sie auf **OK**.
6. Schließen Sie die Seite.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]