---
title: Umsatzprovisionen registrieren
description: In diesem Thema wird erläutert, wie Verkaufsprovisionen berechnet und registriert werden.
author: omulvad
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesEditLines,  CustInvoiceJournal, CommissionTrans, LedgerTransVoucher
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8f9cb895f733442e95cd7008c63942463bbd2cba
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148510"
---
# <a name="register-sales-commissions"></a>Umsatzprovisionen registrieren

[!include [banner](../../includes/banner.md)]

In diesem Thema wird erläutert, wie Verkaufsprovisionen berechnet und registriert werden. Sie können diese Prozedur im Demodatenunternehmen USMF oder für Ihre eigenen Daten ausführen. Bevor Sie mit diesem Leitfaden beginnen, führen Sie den Leitfaden "Vertriebsprovisionsregeln einrichten" aus, um sicherzustellen, das Sie alle erforderlichen Provisionsberechnungseinstellungen haben.

Beachten Sie den Debitor und die Artikelnummern, die Sie für den Provisionsprozess ausgewählt haben und verwenden Sie diese, wenn Sie gebeten werden, einen Auftrag in diesem Leitfaden zu erstellen.


## <a name="invoice-a-sales-order-that-qualifies-a-salesperson-for-a-commission"></a>Fakturieren eines Auftrag, der einen Verkäufer für eine Provision qualifiziert
1. Gehen Sie im Navigationsbereich zu **Module > Vertrieb und Marketing > Kundenaufträge > Alle Kundenaufträge**.
2. Wählen Sie **Neu** aus.
3. Wählen Sie im Feld **Kundenkonto** den gewünschten Datensatz aus dem Dropdown-Menü aus.
4. Wählen Sie **OK**.
5. Wählen Sie im Aktivitätsbereich **Optionen** aus.
6. Wählen Sie **Ansicht ändern**.
7. Wählen Sie **Kopfansicht**.
8. Erweitern Sie den Abschnitt **Einrichtung**.

    - Der Wert im Feld **Vertriebsgruppe** repräsentiert eine Gruppe, der ein oder mehrere Außendienstmitarbeiter zugeordnet sind. Die Personen in der Gruppe sind die, die Provisionen erhalten, wenn der Auftrag fakturiert wird, entsprechend der vordefinierten Sätze und der Verteilung.   
    - Der Wert wird aus der Debitorenkarte kopiert, Sie können ihn jedoch ändern.  
    - Die Verkaufsgruppe wird auch in die Auftragsposition kopiert. Sie können diese ändern, sodass sie von der im Kopf und/oder den Positionen variieren kann.  
    - Der Wert im Feld **Provisionsgruppe** repräsentiert eine Gruppe, die Sie für einen oder mehrere Kunden angelegt haben, um Provisionen zu verfolgen.   
    - Der Wert wird aus der Debitorenkarte kopiert, Sie können ihn jedoch ändern.   

9. Wählen Sie im Aktivitätsbereich **Optionen** aus.
10. Wählen Sie **Ansicht ändern**.
11. Wählen Sie **Linienansicht**.
12. Wählen Sie im Dropdown-Menü des Feldes **Artikelnummer** den Punkt aus, den Sie für Provisionen eingerichtet haben. 
13. Geben Sie im Feld **Menge** eine Zahl ein. Beachten Sie den Nettobetrag der Position. Er stellt den Umsatzerlös dar, der in diesem Beispiel die Grundlage für Provisionsberechnung ist.  
14. Wählen Sie **Speichern**.
15. Wählen Sie im Aktionsbereich **Rechnung**.
16. Wählen Sie **Rechnung**.
17. Erweitern Sie den Abschnitt **Parameter**.
18. Wählen Sie im Feld **Menge** die Option **Alle** aus.
19. Wählen Sie **Ja** im Feld **Buchung**.
20. Wählen Sie **OK**, dann **OK** im nächsten Fenster. Es kann eine Minute dauern die Transaktion zu buchen. Geben Sie der Verarbeitung ausreichend Zeit und schließen Sie nicht die Seite.  

## <a name="review-the-registered-sales-commissions"></a>Überprüfen der erfassten Verkaufsprovisionen
1. Wählen Sie im Aktionsbereich **Rechnung** und dann erneut **Rechnung**.
2. Wählen Sie im Aktionsbereich **Rechnung** und dann **Provisionstransaktionen**.

    - Auf der Registerkarte **Übersicht** werden Zeilen mit den Provisionsbeträgen angezeigt, die an Vertriebsmitarbeiter zu zahlen sind, die dem fakturierten Kundenauftrag zugeordnet sind. Sehen wir uns die Einzelheiten an.  
    - Wenn Sie die Gruppe **Provisionsverkauf** mit dem Leitfaden „Provisionierungsregeln einrichten“ eingerichtet haben, gibt es zwei Verkäufer, die eine Provision erhalten, und die Provision wird zu gleichen Teilen auf sie aufgeteilt.  
    - In diesem Beispiel wird der Gesamtbetrag der Provision als Prozentsatz des Umsatzerlöse berechnet (der Nettobetrag der Auftragsposition).  
3. Schließen Sie die Seite.
4. Wählen Sie **Beleg**. Sie können die Belegbuchungen für die Provisionsbeträge, die für die vordefinierten Provisionsausgaben gebucht werden, anzeigen.  

