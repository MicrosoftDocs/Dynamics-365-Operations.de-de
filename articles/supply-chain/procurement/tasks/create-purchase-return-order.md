---
title: Einkaufsrücklieferung erstellen
description: Diese Prozedur zeigt Ihnen, wie eine Reklamation erstellt wird, indem die Aktivität "Gutschrift" verwendet wird, um Positionen von einem Kreditorenrechnungsdokument zu einer neuen Bestellung zu kopieren.
author: RichardLuan
manager: tfehr
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder, PurchCopying, InventMarking, PurchEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 10b3e695ffcd44909be4781eac5d4eaeef199b03
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/16/2021
ms.locfileid: "5017058"
---
# <a name="create-a-purchase-return-order"></a>Einkaufsrücklieferung erstellen

[!include [banner](../../includes/banner.md)]

Diese Prozedur zeigt Ihnen, wie eine Reklamation erstellt wird, indem die Aktivität "Gutschrift" verwendet wird, um Positionen von einem Kreditorenrechnungsdokument zu einer neuen Bestellung zu kopieren. Sie zeigt Ihnen auch, wie der Auftrag bestätigt und die Lieferung der Waren zurück zum Kreditor verarbeitet wird. Das Beispiel, das in dieser Prozedur angezeigt wird, kann im Demodatenunternehmen USMF verwendet werden. Normalerweise wird diese Aufgabe von einem Einkaufsvertreter ausgeführt.

## <a name="create-a-new-purchase-return-order"></a>Eine neue Reklamation erstellen
1. Wechseln Sie zu **Navigationsbereich > Module > Beschaffung > Bestellungen > Alle Bestellungen**. Der erste Schritt besteht darin, eine neue Bestellung zu erstellen, die als die Einkaufsreklamation zu verwenden ist.  
2. Klicken Sie auf **Neu**.
3. Geben Sie im Feld **Kreditorenkonto** den Wert „US-102“ ein.
4. Klicken Sie auf **OK**.
5. Klicken Sie im **Aktivitätsbereich** auf **Einkauf**.
6. Klicken Sie auf **Gutschrift**. Dies ist die Seite, von der aus Sie aus einer vorhandenen Kreditorenrechnung zu Ihrer Reklamation kopieren können. Dies ist die gleiche Seite, die auch für andere Kopieraktionen verwendet wird. Da wir sie aber von der Aktivität Gutschrif aus geöffnet haben, wird diese Seite so konfiguriert, dass sie die Erstellung einer Reklamation unterstützt, die Kreditorenrechnungen ausgleicht.  
7. Erweitern Sie den Abschnitt **Parameter**.
    - Die Option **Vorzeichen umkehren** ist automatisch ausgewählt und kann nicht geändert werden. Dies gewährleistet, dass das Vorzeichen für die Mengen geändert wird und dass Auftragspositionen, die hinzugefügt werden, die Kreditorenrechnung ausgleichen.  
    - Die Option **Belastungen kopieren** ist automatisch ausgewählt und kann nicht geändert werden. Dies heißt, dass Belastungen von einer Kreditorenrechnung zur Reklamation hinzugezählt werden, um die ursprüngliche Belastung auszugleichen. Es ist möglich, die Änderungen auch auf Auftragskopf und -positionen später zu ändern.  
    - Die Option **Exakt kopieren** ist automatisch ausgewählt und kann nicht geändert werden. Dies stellt sicher, dass eine genaue Kopie von den Werten in allen Feldern in Kreditorenrechnungskopf und -positionen erstellt wird. Dies heißt, dass eine Reklamation mit Werten erstellt wird, die mit allen Bedingungen übereinstimmen, die mit dem Kreditorenrechnungsdokument verwendet werden. 
    - Die Option **Bestellpositionen löschen** löscht sämtliche Bestellpositionen, die bereits in der Bestellung vorhanden sind, bevor die neuen Positionen hinzugefügt werden. In diesem Beispiel haben wir noch keine Positionen zur Reklamation hinzugefügt, sodass es noch keine Auswirkung geben würde. Verwenden Sie diese Option mit Vorsicht, da durch sie alle vorhandenen Positionen ohne weitere Warnung gelöscht werden.  
    * Die Option **Auftragskopf kopieren** ist automatisch ausgewählt und kann nicht geändert werden. Dieses stellt sicher, dass Informationen aus der Kreditorenrechnung kopiert werden und auf den Reklamationskopf angewendet werden. Dies ist nützlich, weil es hilft sicherzustellen, dass die Reklamation die Rechnung ausgleicht, indem ähnliche Bedingungen verwendet werden.  
8. Reduzieren Sie den Abschnitt **Parameter**.
9. Erweitern Sie den Abschnitt **Rechnungen**. Die Seite ist von der Aktivität "Gutschrift" aus geöffnet worden, sodass die einzige verfügbare Option darin besteht, Informationen aus Kreditorenrechnungen zu kopieren. Diese Registerkarte zeigt alle verfügbaren Rechnungen für das Kreditorenkonto an, das auf der Reklamation angegeben ist, welche Sie vorher erstellt haben.   Die Rechnungen werden durch den Rechnungsbeleg oder die Bestellungskennungen identifiziert.
10. Suchen Sie die Kreditorenrechnung, die durch Rechnungsnummer "AP-0006" identifiziert wird und heben Sie diese Position hervor, indem Sie auf irgendein Feld in dieser Position klicken.
11. Wählen Sie die Position aus, indem Sie auf das Kontrollkästchen für die Position klicken. Beachten Sie, dass die Positionen, die auf den Kreditorenrechnungen verfügbar sind, automatisch zusammen mit dem Auftrag ausgewählt werden. Diese bestimmte Kreditorenrechnung hat 2 Auftragspositionen. Für dieses Beispiel senden wir einen Teil der Menge von der zweiten Position zurück.
12. Heben Sie die zweite Position hervor (diejenige mit Artikel "M0006"), indem Sie auf irgendein Feld in dieser Position klicken.
13. Ändern Sie im Feld **Menge** die Menge zu „10“. Dies ist die Menge, die wir zum Lieferant zurücksenden. 
14. Heben Sie die erste Position hervor (diejenige mit Artikel "M0005"), indem Sie auf irgendein Feld in dieser Position klicken.
15. Deaktivieren Sie das Kontrollkästchen für die Position. Nur die Positionen, die Sie ausgewählt haben, werden in Ihren Auftrag kopiert.
16. Reduzieren Sie den Abschnitt **Rechnungen**.
17. Erweitern Sie den Abschnitt **Zum Kopieren ausgewählte Positionen oder Kopfzeile**. Diese Ansicht zeigt eine Zusammenfassung aller Dokumente und Positionen an, die Sie ausgewählt haben, damit sie zum Auftrag kopiert werden.  
18. Reduzieren Sie den Abschnitt **Zum Kopieren ausgewählte Positionen oder Kopfzeile**.
19. Klicken Sie auf **OK**. Die Position, die Sie ausgewählt haben, ist jetzt in Ihre Reklamation kopiert worden. Das Feld **Menge** zeigt „-10“ an.   
20. Klicken Sie im Abschnitt **Bestellposition** auf **Bestand**.
21. Klicken Sie auf **Markierung**. Die Auftragsposition, die erstellt wurde, ist gegenüber der Bestandstransaktion aus der Kreditorenrechnung markiert worden. Dies stellt sicher, dass der Bestand, der dem Lieferant zurückgesendet wird, derselbe Bestand ist, wie der Bestand, der von ihm zuvor empfangen wurde. Es gibt einige Situationen, in denen die Markierung nicht erfolgt, beispielsweise wenn der Bestand bereits als Verbraucht markiert wurde oder wenn es sich um ein Produkt handelt, für das keine Markierung verwendet wird.  

22. Klicken Sie auf **OK**.

## <a name="confirm-and-record-the-shipment-of-goods"></a>Die Lieferung von Waren bestätigen und erfassen
1. Klicken Sie auf **Aktionen > Bestätigen**.
2. Klicken Sie im **Aktivitätsbereich** auf **Empfangen**.
3. Klicken Sie auf **Produktzugang**.
    - Diese Seite wird verwendet, um den Produktzugang für Bestellungen zu erfassen und auch um die Rücklieferung von Waren zum Kreditor zu verarbeiten. Auftragspositionen mit einer negativen Menge bedeuten, dass Waren an den Kreditor zurückzusenden sind und dass das Dokument, das von dieser Seite aus generiert werden kann, als Lieferschein für diesen Zweck verwendet werden kann.   
    - Wählen Sie im Feld **Menge** die Option „Bestellte Menge“ für dieses Beispiel aus. Dies stellt sicher, dass die Lieferung für die gesamte bestellte Menge verarbeitet wird, mit der die Auftragspositionen erstellt wurden.   
4. Geben Sie im Feld **Produktzugang** einen Wert ein. Dieses Feld wird benutzt, um einen Verweis einzugeben, der als Beleg für die Produktzugangserfassung verwendet wird.  
5. Klicken Sie auf **OK**. Die Waren sind jetzt auf der Reklamation als versendet erfasst worden und eine Produktzugangserfassung ist erstellt worden. Sie können die Aktivität "Produktzugang" verwenden, um die Erfassungen zu überprüfen, die mit der Bestellung erstellt wurden und um zu sehen, was wann empfangen oder zurückgesendet wurde.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]