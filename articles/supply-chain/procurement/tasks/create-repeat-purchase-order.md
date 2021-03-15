---
title: Eine wiederholte Bestellung erstellen
description: Dieses Thema zeigt Ihnen, wie man eine Wiederholungsbestellung (PO) erstellt, indem Positionen von früheren Bestelldokumenten zu einer neuen Bestellung oder einer vorhandenen Bestellung kopiert werden.
author: RichardLuan
manager: tfehr
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder, PurchCopying
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 65eb801fb363ce2484dcce4d086d1b2b5ad3388f
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/16/2021
ms.locfileid: "5017341"
---
# <a name="create-a-repeat-purchase-order"></a>Eine wiederholte Bestellung erstellen

[!include [banner](../../includes/banner.md)]

Dieses Thema zeigt Ihnen, wie man eine Wiederholungsbestellung (PO) erstellt, indem Positionen von früheren Bestelldokumenten zu einer neuen Bestellung oder einer vorhandenen Bestellung kopiert werden. Es gibt zwei Methoden für die Erstellung von Wiederholungsaufträgen. Sie können die Aktivitäten verwenden, die auf dem Dokumentenniveau vom Aktionsbereich verfügbar sind, oder Sie können die Positionsdetailaktivitäten verwenden. Die Aktivitäten auf Dokumentebene sind hauptsächlich dazu bestimmt, eine neue Bestellung zu erstellen, indem Positionen und Kopfzeileninformationen aus einem anderen Auftrag hinzugefügt werden, während die Positionsdetailaktivität hauptsächlich dazu dient, Positionen aus einem vorhandenen Auftrag hinzuzufügen. Das Beispiel, das in diesem Leitfaden angezeigt wird, kann im Demodatenunternehmen USMF verwendet werden. Normalerweise wird diese Aufgabe von einem Einkaufsvertreter ausgeführt.


## <a name="create-a-new-repeat-purchase-order"></a>Eine neue Wiederholungsbestellung erstellen
1. Wechseln Sie im Navigationsbereich zu **Module > Beschaffung > Bestellungen > Alle Bestellungen**. Zuerst probieren wir die Optionen aus, bei denen Informationen zu einem neuen Auftrag kopiert werden.  
2. Wählen Sie **Neu** aus.
3. Geben Sie im Feld **Kreditorenkonto** den Wert `US-101` ein.
4. Wählen Sie **OK**.
5. Wählen Sie im Aktivitätsbereich **Bestellung** aus.
6. Wählen Sie **Aus allen** aus. Dies ist die Seite, von der aus Sie aus vorhandenen Aufträgen in Ihren Auftrag kopieren können. Es gibt verschiedene Optionen dazu, wie die Positionen kopiert werden, und verschiedene Arten von Dokumenten, aus denen Sie kopieren können. Wir betrachten zuerst die Optionen, wie Positionen kopiert werden. 
7. Erweitern Sie den Abschnitt **Parameter**.

    - Das Feld **Mengenfaktor** ist nützlich, wenn Sie eine Menge verwenden müssen, die anders als die, die auf dem Auftrag ist, aus dem Sie kopieren. Zum Beispiel wenn Sie das Doppelte der Menge bestellen möchten, die sich in den Positionen befindet, aus denen Sie kopieren, würden Sie 2 in dieses Feld eingeben und dann wird das System Positionen hinzufügen, in denen die ursprüngliche Menge verdoppelt worden ist.  
    - Das Feld **Vorzeichen umkehren** unterstützt auch das Ändern der bestellten Menge, indem das Vorzeichen der Menge für Auftragspositionen, die hinzugefügt werden, geändert wird. Dies ist möglicherweise nützlich, wenn Sie eine Transaktion rückgängig machen müssen, indem Sie Auftragspositionen erstellen, die die Transaktion negieren. Diese Option ist automatisch ausgewählt, wenn die Seite von der Aktivität **Gutschrift erstellen** aus geöffnet wird.  
    - Die Option **Belastungen kopieren** ermöglicht es Ihnen, Belastungen zu Ihrem neuen Auftrag vom Dokument aus zu kopieren, aus dem Sie die Auftragspositionen kopieren.  
    - Die Option **Preise neu berechnen** verwendet die aktuellen Preise und Rabatte, statt sie aus dem Dokument zu kopieren, aus dem Sie andere Informationen kopieren.  
    - Die Option **Exakt kopieren** erstellt eine exakte Kopie der Werte in allen Feldern in der Kopfzeile und den Positionen des Auftragsdokuments. Wenn diese Option nicht ausgewählt ist, werden Standardwerte für viele der Felder in Bezug auf den Kreditor und Produkte verwendet, so als ob Sie den neuen Auftrag manuell erstellen würden. Zum Beispiel wenn der Auftrag, aus dem Sie kopieren, das standardmäßige Rechnungskonto für den Lieferant überschrieben hätte, würde dieses selbe Rechnungskonto zu Ihrem Auftrag kopiert. Wenn Sie nicht die Option **Exakt kopieren** auswählen würden, würde stattdessen das standardmäßige Rechnungskonto für den Lieferant für Ihren Auftrag verwendet werden.  
    - Die Option **Bestellpositionen löschen** löscht alle Bestellpositionen, die bereits in der Bestellung vorhanden sind, zu der Sie kopieren, bevor die neuen Positionen angewendet werden. Verwenden Sie diese Option mit Vorsicht, da durch sie alle vorhandenen Positionen ohne weitere Warnung gelöscht werden.  
    - Wenn Sie die Option **Auftragskopf kopieren** verwenden, müssen Sie die Kopfzeileninformationen für Ihren neuen Auftrag nicht zuerst manuell erstellen. Beachten Sie, dass diese Option dazu führt, dass Standardwerte für die Felder verwendet werden, die dem Kreditor zugeordnet sind. Wenn das Dokument, aus dem Sie kopieren, keine Standardwerte hat, die Sie kopieren möchten, verwenden Sie die Option **Exakt kopieren**.   
    - Es gibt verschiedene Dokumentquellen, aus denen Sie kopieren können. Jede hat einen getrennten Abschnitt auf dieser Seite. Zum Beispiel gestattet es der Abschnitt **Bestellungen** Ihnen, aus vorhandenen Bestellungen zu kopieren.  

8. Im Abschnitt **Bestellungen** wählen Sie die Zeilen aus, die in die Zwischenablage kopiert werden sollen. Es ist möglich, zusätzliche Bestellpositionen aus anderen Bestellungen auszuwählen und sie auch in Ihren Auftrag zu kopieren. Es ist ebenfalls möglich, Positionen aus anderen Arten von Einkaufsbelegen hinzuzufügen. In den nächsten Schritten werden die verschiedenen Optionen überprüft.  
9. Erweitern Sie den Abschnitt **Bestätigung**. Hier können Sie Bestellungsbestätigung auswählen, um von ihnen zu kopieren. Die Bestellungsbestätigungen werden durch die zugeordnete Einkaufserfassungskennung oder die Bestellungskennung identifiziert.  
10. Erweitern Sie den Abschnitt **Produktzugänge**. Hier können Sie Produktzugangserfassungen auswählen, um von ihnen zu kopieren. Die Produktzugangserfassungen werden durch die Produktzugangsbescheinigung oder die Bestellungskennung identifiziert.   
11. Erweitern Sie den Abschnitt **Rechnungen**. Hier können Sie Kreditorenrechnungen auswählen, um von ihnen zu kopieren. Die Rechnungen werden durch den Rechnungsbeleg oder die Bestellungskennung identifiziert.   
12. Erweitern Sie den Abschnitt **Zum Kopieren ausgewählte Positionen oder Kopfzeile**. Diese Ansicht zeigt eine Zusammenfassung aller Dokumente und Positionen an, die ausgewählt worden sind, um zu Ihrem Auftrag kopiert zu werden.   
13. Wählen Sie **OK**. Die Positionen, die Sie ausgewählt haben, sind zu Ihrer neuen Bestellung kopiert worden.   

## <a name="copy-lines-to-an-existing-purchase-order"></a>Positionen in eine vorhandene Bestellung kopieren  

Anstatt einen gesamten Auftrag zu kopieren, ist es üblicher, eine neue Bestellung zu erstellen und Informationen im Bestellungskopf auszufüllen und dann die einzelnen Positionen aus vorhandenen Aufträgen zu kopieren.  

1. Wählen Sie die Position **Bestellung** aus.
2. Wählen Sie **Aus allen** aus. Die Seite, die sich öffnet, ist mit jender identisch, die zuvor angezeigt wurde, aber verschiedene Optionen sind ausgewählt, wenn sie von der Auftragspositionsansicht aus geöffnet wird. Überprüfen wir die Parameter.   
3. Erweitern Sie den Abschnitt **Parameter**.

    - Die Option **Bestellpositionen löschen** ist nicht ausgewählt. Dies heißt, dass Sie neue Positionen zu Ihrem Auftrag kopieren können, ohne vorhandene Positionen zu entfernen.   
    - Die Option **Auftragskopf kopieren** ist nicht ausgewählt, da wir dem Auftrag nur zusätzliche Positionen hinzufügen.   
    - Für dieses Beispiel kopieren wir nun Positionen aus einer vorhandenen Bestellung.   

4. Wählen Sie die Position für die gewünschte Bestellung aus. Beachten Sie, dass die einzelne Auftragsposition, die auf dieser Bestellung ist, ebenfalls ausgewählt ist.  
5. Wählen Sie **OK**. Die zusätzliche Auftragsposition ist Ihrer Bestellung hinzugefügt worden.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]