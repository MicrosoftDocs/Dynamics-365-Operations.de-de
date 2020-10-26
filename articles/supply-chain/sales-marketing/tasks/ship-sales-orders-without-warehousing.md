---
title: Aufträge ohne Lagerort liefern
description: In diesem Thema wird erläutert, wie Sie einen Kundenauftrag aktualisieren, wenn Produkte an den Kunden geliefert werden.
author: omulvad
manager: tfehr
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesTable, SalesEditLines,  SrsReportViewerForm, SalesTableLineQuantity, CustPackingSlipJournal
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b6b1dbb4d53785c226f7c9d40339d9dd19f47152
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/10/2020
ms.locfileid: "3984153"
---
# <a name="ship-sales-orders-without-warehousing"></a>Aufträge ohne Lagerort liefern

[!include [banner](../../includes/banner.md)]

In diesem Thema wird erläutert, wie Sie einen Kundenauftrag aktualisieren, wenn Produkte an den Kunden geliefert werden. Der Leitfaden betrifft den Erfüllungsfluss, der nicht für die Lagerortverwaltung eingerichtet ist (weder grundlegende oder erweiterte Lagerung) und daher keine Produktentnahme vor Lieferung erfassen muss. Sie können diese Prozedur in Ihrem eigenen Demodatenunternehmen oder in USMF ausführen. In beiden Fällen erstellen Sie einen Auftrag für ein inventarisiertes Produkt mit einer Menge größer als 1, bevor Sie mit der Aufgabe beginnen. Um ein Buchungsfehler zu vermeiden, müssen Sie überprüfen ob die verfügbare Menge des Produkts im Standort und Lagerort, den Sie im Auftrag ausgewählt haben, in der Auftragsmenge enthalten sind.

## <a name="post-packing-slip-for-an-order"></a>Lieferschein für eine Bestellung buchen
1. Gehen Sie im Navigationsbereich zu **Module > Vertrieb und Marketing > Kundenaufträge > Alle Kundenaufträge**.
2. Wählen Sie in der Liste den Auftrag aus, den Sie für diese Aufgabe erstellt haben.
3. Wählen Sie im Aktionsbereich **Auswahl und packen Sie**.
4. Wählen Sie **Postkarte**.
5. Erweitern oder komprimieren Sie den Abschnitt **Parameter**.
6. Wählen Sie im Feld **Menge** die Option **Alle** aus.
    - Andere Optionen sind **Lieferung jetzt** und **Kommissioniert**. Wenn die Bestellzeile teilweise versendet werden soll und das Feld **Lieferung jetzt** in der Bestellzeile eine Menge enthält, würden Sie **Lieferung jetzt** auswählen. Wenn der Erfüllungsablauf Ihres Unternehmens die Kommissionierung als separaten Prozess beinhaltet, der von einer Kommissionierliste verwaltet und registriert wird, wählen Sie **Kommissioniert**.  
    - Überprüfen Sie, ob die Option **Buchung** auf **Ja** gesetzt ist.  
7. Stellen Sie die Option **Packzettel** drucken auf **Ja**. Die Registerkarte **Übersicht** enthält eine Liste der Packzettel, die in diesem Beitrag generiert werden sollen. Wenn Sie einen einzelnen Auftrag liefern, gibt es in der Regel einen Lieferschein. Wenn die Positionen dieses Auftrags von unterschiedlichen Standorten versendet werden sollen, wird das Buchen automatisch in die entsprechende Anzahl von Dokumenten geteilt. Dies ist eine erforderliche Bedingung, die nicht geändert werden kann. Ebenso wird die Buchung ebenfalls in mehrere Dokumente aufgeteilt, wenn die Positionen des Auftrags zu verschiedenen Lieferadressen versendet werden sollen, und die Lieferrichtlinie so eingerichtet ist, dass eine Teilung erforderlich ist.  
8. Wählen Sie auf der Registerkarte **Linien** die Zeile für die zu versendende Auftragszeile aus.
9. Geben Sie im Feld **Aktualisierung** eine Zahl ein, die kleiner ist als die ursprüngliche Menge.
10. Wählen Sie **OK**.
11. Wählen Sie **Ja** aus.
12. Schließen Sie die Seite.
13. Wählen Sie im Aktivitätsbereich **Optionen** aus.
14. Wählen Sie **Ansicht ändern**.
15. Wählen Sie **Kopfansicht**.
    - Wenn alle Positionen im Auftrag vollständig geliefert wurden, wird der Auftragsstatus von "Offen" auf "Geliefert" geändert.  
    - In diesem Beispiel ist die Auftragsposition teilweise geliefert worden. Daher verbleibt der Auftragsstatus "Offen".     
    - Das Feld **Dokumentstatus** wird auf Packzettel gesetzt, da mindestens eine der Auftragszeilen versendet wurde.  
16. Wählen Sie im Aktivitätsbereich **Allgemein** aus.
17. Wählen Sie **Linienmenge**.
18. Schließen Sie die Seite.
19. Wählen Sie im Aktionsbereich **Auswahl und packen Sie**.
20. Wählen Sie **Packzettel**. Die Seite **Packzetteljournal** enthält alle Packzettel-Dokumente, die für Ihre Bestellung generiert wurden. Sie können Details jedes Dokuments zu prüfen und drucken, wenn Sie wünschen.  

