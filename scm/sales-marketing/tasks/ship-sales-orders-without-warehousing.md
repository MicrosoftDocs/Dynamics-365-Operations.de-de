--- 
title: "Aufträge ohne Lagerort liefern"
description: Dieser Leitfaden veranschaulicht, wie ein Auftrag aktualisiert wird, wenn Produkte an den Debitor versendet werden.
author: omulvad
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: ab2b52b91bcaef57996ae35120e8713aac5852e7
ms.contentlocale: de-de
ms.lasthandoff: 07/27/2017

---
# <a name="ship-sales-orders-without-warehousing"></a>Aufträge ohne Lagerort liefern

[!include[task guide banner](../../includes/task-guide-banner.md)]

Dieser Leitfaden veranschaulicht, wie ein Auftrag aktualisiert wird, wenn Produkte an den Debitor versendet werden. Der Leitfaden betrifft den Erfüllungsfluss, der nicht für die Lagerortverwaltung eingerichtet ist (weder grundlegende oder erweiterte Lagerung) und daher keine Produktentnahme vor Lieferung erfassen muss. Sie können diese Prozedur in Ihrem eigenen Demodatenunternehmen oder in USMF ausführen. In beiden Fällen erstellen Sie einen Auftrag für ein inventarisiertes Produkt mit einer Menge größer als 1, bevor Sie mit der Aufgabe beginnen. Um ein Buchungsfehler zu vermeiden, müssen Sie überprüfen ob die verfügbare Menge des Produkts im Standort und Lagerort, den Sie im Auftrag ausgewählt haben, in der Auftragsmenge enthalten sind.


## <a name="post-packing-slip-for-an-order"></a>Lieferschein für eine Bestellung buchen
1. Wechseln Sie zu "Vertrieb und Marketing" > "Aufträge" > "Alle Aufträge".
2. Wählen Sie in der Liste den Auftrag aus, den Sie für diese Aufgabe erstellt haben.
3. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
4. Klicken Sie im Aktivitätsbereich auf "Entnehmen und verpacken".
5. Klicken Sie auf "Lieferschein buchen".
6. Erweitern oder reduzieren Sie den Abschnitt "Parameter".
7. Wählen Sie im Feld "Menge" die Option "Alle" aus.
    * Andere Optionen sind "Jetzt liefern" und "Entnommen": Falls die Auftragsposition teilweise geliefert werden soll und das Feld Jetzt liefern auf der Auftragsposition eine Menge enthält, würden Sie Jetzt liefern auswählen. Wenn der Erfüllungsfluss Ihrer Organisation die Entnahme als separater Prozess umfasst, der über eine Entnahmeliste verwaltet und erfasst wird, würden Sie "Entnommen" auswählen.  
    * Überprüfen Sie, ob die Buchungsoption auf "Ja" festgelegt ist.  
8. Legen Sie die Option "Lieferschein drucken" auf "Ja" fest.
    * Die Registerkarte "Überblick" enthält eine Liste der in dieser Buchung zu erstellende Lieferscheine. Wenn Sie einen einzelnen Auftrag liefern, gibt es in der Regel einen Lieferschein. Wenn die Positionen dieses Auftrags von unterschiedlichen Standorten versendet werden sollen, wird das Buchen automatisch in die entsprechende Anzahl von Dokumenten geteilt. Dies ist eine erforderliche Bedingung, die nicht geändert werden kann. Ebenso wird die Buchung ebenfalls in mehrere Dokumente aufgeteilt, wenn die Positionen des Auftrags zu verschiedenen Lieferadressen versendet werden sollen, und die Lieferrichtlinie so eingerichtet ist, dass eine Teilung erforderlich ist.  
9. Wählen Sie auf der Registerkarte "Positionen" die Zeile die zu liefernde Auftragsposition aus.
10. Wählen Sie im Feld "Aktualisieren" eine Zahl kleiner als die ursprüngliche Menge ein.
11. Klicken Sie auf "OK".
12. Klicken Sie auf "Ja".
13. Schließen Sie die Seite.
14. Klicken Sie im Aktivitätsbereich auf "Optionen".
15. Klicken Sie auf "Ansicht ändern".
16. Klicken Sie auf die Kopfzeilenansicht.
    * Wenn alle Positionen im Auftrag vollständig geliefert wurden, wird der Auftragsstatus von "Offen" auf "Geliefert" geändert.  
    * In diesem Beispiel ist die Auftragsposition teilweise geliefert worden. Daher verbleibt der Auftragsstatus "Offen".     
    * Das Feld "Dokumentstatus" wird auf "Lieferschein" festgelegt, da mindestens eine der Auftragspositionen geliefert wurde.  
17. Klicken Sie im Aktivitätsbereich auf "Allgemein".
18. Klicken Sie auf "Positionsmenge".
19. Schließen Sie die Seite.
20. Klicken Sie im Aktivitätsbereich auf "Entnehmen und verpacken".
21. Klicken Sie auf "Lieferschein".
    * Die Seite "Lieferscheinerfassung" enthält alle Lieferscheindokumente, die für Ihren Auftrag generiert wurden. Sie können Details jedes Dokuments zu prüfen und drucken, wenn Sie wünschen.  


