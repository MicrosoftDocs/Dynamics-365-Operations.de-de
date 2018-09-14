--- 
title: Eine wiederholte Bestellung erstellen
description: "Diese Prozedur zeigt Ihnen, wie man eine Wiederholungsbestellung (PO) erstellt, indem Positionen von früheren Bestelldokumenten zu einer neuen Bestellung oder einer vorhandenen Bestellung kopiert werden."
author: FrankDahl
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable, PurchCreateOrder, PurchCopying
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 257582d889ff55753f9bdbd234f0540503d20f27
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-repeat-purchase-order"></a>Eine wiederholte Bestellung erstellen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Diese Prozedur zeigt Ihnen, wie man eine Wiederholungsbestellung (PO) erstellt, indem Positionen von früheren Bestelldokumenten zu einer neuen Bestellung oder einer vorhandenen Bestellung kopiert werden. Es gibt zwei Methoden für die Erstellung von Wiederholungsaufträgen. Sie können die Aktivitäten verwenden, die auf dem Dokumentenniveau vom Aktionsbereich verfügbar sind, oder Sie können die Positionsdetailaktivitäten verwenden. Die Aktivitäten auf Dokumentebene sind hauptsächlich dazu bestimmt, eine neue Bestellung zu erstellen, indem Positionen und Kopfzeileninformationen aus einem anderen Auftrag hinzugefügt werden, während die Positionsdetailaktivität hauptsächlich dazu dient, Positionen aus einem vorhandenen Auftrag hinzuzufügen. Das Beispiel, das in diesem Leitfaden angezeigt wird, kann im Demodatenunternehmen USMF verwendet werden. Normalerweise wird diese Aufgabe von einem Einkaufsvertreter ausgeführt.


## <a name="create-a-new-repeat-purchase-order"></a>Eine neue Wiederholungsbestellung erstellen
1. Wechseln Sie zu "Beschaffung" > "Bestellung" > "Alle Bestellungen".
    * Zuerst probieren wir die Optionen aus, bei der Informationen zu einem neuen Auftrag kopiert werden.  
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Kreditorenkonto" den Wert US-101 ein.
4. Klicken Sie auf "OK".
5. Klicken Sie im Aktionsbereich auf "Bestellung".
6. Klicken Sie auf "Aus allen".
    * Dies ist die Seite, von der aus Sie aus vorhandenen Aufträgen in Ihren Auftrag kopieren können. Es gibt verschiedene Optionen dazu, wie die Positionen kopiert werden, und verschiedene Arten von Dokumenten, aus denen Sie kopieren können. Wir betrachten zuerst die Optionen dazu, wie Positionen kopiert werden.   
7. Erweitern Sie den Abschnitt "Parameter".
    * Das Mengenfaktorfeld ist nützlich, wenn Sie eine Menge verwenden müssen, die unterschiedlich als die ist, die auf dem Auftrag ist, aus dem Sie kopieren. Zum Beispiel wenn Sie das Doppelte der Menge bestellen möchten, die sich in den Positionen befindet, aus denen Sie kopieren, würden Sie "2" in dieses Feld eingeben und dann wird das System Positionen hinzufügen, in denen die ursprüngliche Menge verdoppelt worden ist.  
    * Das Feld "Vorzeichen umkehren" unterstützt auch das Ändern der bestellten Menge, indem das Vorzeichen der Menge für Auftragspositionen, die hinzugefügt werden, geändert wird. Dies ist möglicherweise nützlich, wenn Sie eine Transaktion rückgängig machen müssen, indem Sie Auftragspositionen erstellen, die die Transaktion negieren. Diese Option ist automatisch ausgewählt, wenn die Seite von der Aktivität "Gutschrift erstellen" aus geöffnet wird.  
    * Die Option "Belastungen kopieren" ermöglicht es Ihnen, Belastungen zu Ihrem neuen Auftrag vom Dokument aus zu kopieren, aus dem Sie die Auftragspositionen kopieren.  
    * Die Option "Preise neu berechnen" verwendet die aktuellen Preise und Rabatte, anstatt sie aus dem Dokument zu kopieren, aus dem Sie andere Informationen kopieren.  
    * Die Option "Exakt kopieren" erstellt eine exakte Kopie der Werte in allen Feldern in der Kopfzeile und den Positionen des Auftragsdokuments. Wenn diese Option nicht ausgewählt ist, werden Standardwerte für viele der Felder in Bezug auf den Kreditor und Produkte verwendet, so als ob Sie den neuen Auftrag manuell erstellen würden. Zum Beispiel wenn der Auftrag, aus dem Sie kopieren, das standardmäßige Rechnungskonto für den Kreditor überschrieben hätte, würde dieses selbe Rechnungskonto zu Ihrem Auftrag kopiert. Wenn Sie nicht die Option "Exakt kopieren" auswählen würden, würde stattdessen das standardmäßige Rechnungskonto für den Kreditor für Ihren Auftrag verwendet werden.  
    * Der Option "Bestellpositionen löschen" löscht alle Bestellpositionen, die bereits in der Bestellung vorhanden sind, zu der Sie kopieren, bevor die neuen Positionen angewendet werden. Verwenden Sie diese Option mit Vorsicht, da durch sie alle vorhandenen Positionen ohne weitere Warnung gelöscht werden.  
    * Wenn Sie die Option "Auftragskopf kopieren" verwenden, müssen Sie die Kopfzeileninformationen für Ihren neuen Auftrag nicht manuell erstellen. Beachten Sie, dass diese Option dazu führt, dass Standardwerte für die Felder verwendet werden, die dem Kreditor zugeordnet sind. Wenn das Dokument, aus dem Sie kopieren, keine Standardwerte hat, die Sie kopieren möchten, verwenden Sie ebenfalls die Option "Exakt kopieren".  
8. Reduzieren Sie den Abschnitt "Parameter".
    * Es gibt verschiedene Dokumentquellen, aus denen Sie kopieren können. Jede hat einen getrennten Abschnitt auf dieser Seite. Zum Beispiel gestattet es der Abschnitt "Bestellungen" Ihnen, aus vorhandenen Bestellungen zu kopieren.  
9. Klicken Sie auf die Position für die Bestellung, die die Kennung "00015" hat. 
10. Wählen Sie durch Aktivieren des Kontrollkästchens die Position aus.
11. Deaktivieren Sie das Kontrollkästchen für die Position, sodass sie nicht in Ihren Auftrag kopiert wird.
    * Jetzt sind 4 Positionen ausgewählt worden, um zu Ihrer Bestellung kopiert zu werden. Es ist möglich, zusätzliche Bestellpositionen aus anderen Bestellungen auszuwählen und sie ebenfalls in Ihren Auftrag zu kopieren. Es ist auch möglich, Positionen aus anderen Arten von Einkaufsbelegen hinzuzufügen. In den nächsten Schritten werden die verschiedenen Optionen überprüft.  
12. Reduzieren Sie den Abschnitt "Bestellungen".
13. Erweitern Sie den Abschnitt "Bestätigung".
    * Hier können Sie Bestellungsbestätigung auswählen, um von ihnen zu kopieren. Die Bestellungsbestätigungen werden durch die zugeordnete Einkaufserfassungskennung oder die Bestellungskennung identifiziert.  
14. Reduzieren Sie den Abschnitt "Bestätigung".
15. Erweitern Sie den Abschnitt "Produktzugänge".
    * Hier können Sie Produktzugangserfassungen auswählen, um von ihnen zu kopieren. Die Produktzugangserfassungen werden durch die Produktzugangsbescheinigung oder die Bestellungskennung identifiziert.   
16. Reduzieren Sie den Abschnitt "Produktzugänge".
17. Erweitern Sie den Abschnitt "Rechnungen".
    * Hier können Sie Kreditorenrechnungen auswählen, um von ihnen zu kopieren. Die Rechnungen werden durch den Rechnungsbeleg oder die Bestellungskennung identifiziert.   
18. Reduzieren Sie den Abschnitt "Rechnungen".
19. Erweitern Sie den Abschnitt "Zum Kopieren ausgewählte Positionen oder Kopfzeile".
    * Diese Ansicht zeigt eine Zusammenfassung aller Dokumente und Positionen an, die ausgewählt worden sind, um zu Ihrem Auftrag kopiert zu werden.   
20. Reduzieren Sie den Abschnitt "Zum Kopieren ausgewählte Positionen oder Kopfzeile".
21. Klicken Sie auf "OK".
    * Die 4 Positionen, die Sie ausgewählt haben, sind zu Ihrer neuen Bestellung kopiert worden.   

## <a name="copy-lines-to-an-existing-purchase-order"></a>Positionen in eine vorhandene Bestellung kopieren
    * Anstatt einen gesamten Auftrag zu kopieren, ist es üblicher, eine neue Bestellung zu erstellen und Informationen im Bestellungskopf auszufüllen und dann einzelne Positionen aus vorhandenen Aufträgen zu kopieren.  
1. Klicken Sie auf die Bestellposition.
2. Klicken Sie auf "Aus allen".
    * Die Seite, die sich öffnet, ist mit der identisch, die zuvor angezeigt wurde, aber verschiedene Optionen sind ausgewählt, wenn sie von der Auftragspositionsansicht aus geöffnet wird. Überprüfen wir nun die Parameter.   
3. Erweitern Sie den Abschnitt "Parameter".
    * Die Option "Bestellpositionen löschen" ist nicht ausgewählt. Dies heißt, dass Sie neue Positionen zu Ihrem Auftrag kopieren können, ohne vorhandene Positionen zu entfernen.   
    * Die Option "Auftragskopf kopieren" ist ebenfalls nicht ausgewählt, da wir dem Auftrag nur zusätzliche Positionen hinzufügen.   
4. Reduzieren Sie den Abschnitt "Parameter".
    * Für dieses Beispiel kopieren wir Positionen aus einer vorhandenen Bestellung.   
5. Klicken Sie auf die Position für die Bestellung, die die Kennung "00034" hat. 
6. Wählen Sie durch Aktivieren des Kontrollkästchens die Position aus.
    * Beachten Sie, dass die einzelne Auftragsposition, die auf dieser Bestellung ist, auch ausgewählt ist.  
7. Klicken Sie auf "OK".
    * Die zusätzliche Auftragsposition ist Ihrer Bestellung hinzugefügt worden.  


