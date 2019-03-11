---
title: Umsatzprovisionen registrieren
description: Dieses Verfahren zeigt Ihnen, wie Verkaufsprovisionen berechnet und registriert werden.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesEditLines,  CustInvoiceJournal, CommissionTrans, LedgerTransVoucher
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2c39b2fcf521106dfb58466bc45a316c0b506345
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "355149"
---
# <a name="register-sales-commissions"></a>Umsatzprovisionen registrieren

[!include [task guide banner](../../includes/task-guide-banner.md)]

Dieses Verfahren zeigt Ihnen, wie Verkaufsprovisionen berechnet und registriert werden. Sie können diese Prozedur im Demodatenunternehmen USMF oder für Ihre eigenen Daten ausführen. Bevor Sie mit diesem Leitfaden beginnen, führen Sie den Leitfaden "Vertriebsprovisionsregeln einrichten" aus, um sicherzustellen, das Sie alle erforderlichen Provisionsberechnungseinstellungen haben.

Beachten Sie den Debitor und die Artikelnummern, die Sie für den Provisionsprozess ausgewählt haben und verwenden Sie diese, wenn Sie gebeten werden, einen Auftrag in diesem Leitfaden zu erstellen.


## <a name="invoice-a-sales-order-that-qualifies-a-salesperson-for-a-commission"></a>Fakturieren eines Auftrag, der einen Verkäufer für eine Provision qualifiziert
1. Wechseln Sie zu "Vertrieb und Marketing" > "Aufträge" > "Alle Aufträge".
2. Klicken Sie auf "Neu".
3. Klicken Sie im Feld "Debitorenkonto" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
4. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
5. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
6. Klicken Sie auf "OK".
7. Klicken Sie im Aktivitätsbereich auf "Optionen".
8. Klicken Sie auf "Ansicht ändern".
9. Klicken Sie auf die Kopfzeilenansicht.
10. Erweitern Sie den Abschnitt 'Einstellungen'.
    * Der Wert im Feld "Verkaufsgruppe" stellt eine Gruppe mit einem oder mehreren Verkäufern die ihr zugewiesen wurden dar. Die Personen in der Gruppe sind die, die Provisionen erhalten, wenn der Auftrag fakturiert wird, entsprechend der vordefinierten Sätze und der Verteilung.   Der Wert wird aus der Debitorenkarte kopiert, Sie können ihn jedoch ändern.  Die Verkaufsgruppe wird auch in die Auftragsposition kopiert. Sie können diese ändern, sodass sie von der im Kopf und/oder den Positionen variieren kann.  
    * Der Wert im Feld "Provisionsgruppe" ist eine Gruppe, die Sie für einen oder mehrere Debitoren mit dem Zweck der Nachverfolgungs von Provisionen erstellt haben.   Der Wert wird aus der Debitorenkarte kopiert, Sie können ihn jedoch ändern.   
11. Klicken Sie im Aktivitätsbereich auf "Optionen".
12. Klicken Sie auf "Ansicht ändern".
13. Klicken Sie auf Positionsansicht.
14. Klicken Sie im Feld "Artikelnummer" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
15. Wählen Sie in der Liste den Artikel aus, für den Sie Provisionen eingerichtet haben. 
16. Geben Sie im Feld "Menge" eine Zahl ein.
    * Beachten Sie den Nettobetrag der Position. Er stellt den Umsatzerlös dar, der in diesem Beispiel die Grundlage für Provisionsberechnung ist.  
17. Klicken Sie auf "Speichern".
18. Klicken Sie im Aktivitätsbereich auf "Rechnung".
19. Klicken Sie auf "Rechnung".
20. Erweitern Sie den Abschnitt "Parameter".
21. Wählen Sie im Feld "Menge" die Option "Alle" aus.
22. Wählen Sie "Ja" im Feld "Buchung" aus.
23. Klicken Sie auf "OK".
24. Klicken Sie auf "OK".
    * Es kann eine Minute dauern die Transaktion zu buchen. Geben Sie der Verarbeitung ausreichend Zeit und schließen Sie nicht die Seite.  

## <a name="review-the-registered-sales-commissions"></a>Überprüfen der erfassten Verkaufsprovisionen
1. Klicken Sie im Aktivitätsbereich auf "Rechnung".
2. Klicken Sie auf "Rechnung".
3. Klicken Sie im Aktivitätsbereich auf "Rechnung".
4. Klicken Sie auf "Provisionstransaktionen".
    * Die Registerkarte "Überblick" zeigt Positionen an, welche die provisionsfälligen Beträge für die Verkäufer darstellen, die dem fakturierten Auftrag zugeordnet sind. Sehen wir uns die Einzelheiten an.     
    * Wenn Sie "Vertriebsprovisionsregeln einrichten" verwendet haben, um die Provisionsverkaufsgruppe einzurichten, gibt es zwei Verkäufer für Verkaufsprovisionen und die Provision wird gleichmäßig zwischen ihnen geteilt.  
    * In diesem Beispiel wird der Gesamtbetrag der Provision als Prozentsatz des Umsatzerlöse berechnet (der Nettobetrag der Auftragsposition).   
5. Schließen Sie die Seite.
6. Klicken Sie auf Beleg.
    * Sie können die Belegbuchungen für die Provisionsbeträge, die für die vordefinierten Provisionsausgaben gebucht werden, anzeigen.  

