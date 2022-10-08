---
title: Eine wiederholte Bestellung erstellen
description: Dieser Artikel zeigt Ihnen, wie man eine Wiederholungsbestellung (PO) erstellt, indem Positionen von früheren Bestelldokumenten zu einer neuen Bestellung oder einer vorhandenen Bestellung kopiert werden.
author: GalynaFedorova
ms.date: 09/30/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder, PurchCopying
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 335461d60fa0bc92e9711806c6e42643a3f75d02
ms.sourcegitcommit: 073604c07116e0a87f78ab2c76cb89ae83ebba3c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/30/2022
ms.locfileid: "9608110"
---
# <a name="create-a-repeat-purchase-order"></a>Eine wiederholte Bestellung erstellen

[!include [banner](../../includes/banner.md)]

Dieser Artikel zeigt Ihnen, wie man eine Wiederholungsbestellung (PO) erstellt, indem Positionen von früheren Bestelldokumenten zu einer neuen Bestellung oder einer vorhandenen Bestellung kopiert werden. Es gibt zwei Methoden für die Erstellung von Wiederholungsaufträgen. Sie können die Aktivitäten verwenden, die auf dem Dokumentenniveau vom Aktionsbereich verfügbar sind, oder Sie können die Positionsdetailaktivitäten verwenden. Die Aktivitäten auf Dokumentebene sind dazu bestimmt, eine neue Bestellung zu erstellen, indem Positionen und Kopfzeileninformationen aus einem anderen Auftrag hinzugefügt werden, während die Positionsdetailaktivität hauptsächlich dazu dient, Positionen aus einem vorhandenen Auftrag hinzuzufügen. Das Beispiel, das in diesem Leitfaden angezeigt wird, kann im Demodatenunternehmen USMF verwendet werden. Normalerweise wird diese Aufgabe von einem Einkaufsvertreter ausgeführt.

## <a name="create-a-new-repeat-purchase-order"></a>Eine neue Wiederholungsbestellung erstellen

1. Wechseln Sie im Navigationsbereich zu **Module \> Beschaffung \> Bestellungen \> Alle Bestellungen**. Zuerst probieren wir die Optionen aus, bei denen Informationen zu einem neuen Auftrag kopiert werden.  
1. Wählen Sie **Neu** aus.
1. Geben Sie im Feld **Kreditorenkonto** den Wert `US-101` ein.
1. Wählen Sie **OK** aus.
1. Öffnen Sie im Aktionsbereich die Registerkarte **Bestellung** und wählen Sie aus der Gruppe **Kopieren** **Aus allen** aus. Es öffnet sich das Dialogfeld **Aus anderen Dokumenten kopieren**. Von hier aus können Sie vorhandene Aufträge in Ihren Auftrag kopieren. Es gibt verschiedene Optionen dazu, wie die Positionen kopiert werden, und verschiedene Arten von Dokumenten, aus denen Sie kopieren können. Wir betrachten zuerst die Optionen, wie Positionen kopiert werden.
1. Erweitern Sie den Inforegister **Parameter**.

    - Das Feld **Mengenfaktor** ist nützlich, wenn Sie eine Menge verwenden müssen, die anders als die, die auf dem Auftrag ist, aus dem Sie kopieren. Zum Beispiel wenn Sie das Doppelte der Menge bestellen möchten, die sich in den Positionen befindet, aus denen Sie kopieren, würden Sie 2 in dieses Feld eingeben und dann wird das System Positionen hinzufügen, in denen die ursprüngliche Menge verdoppelt worden ist.  
    - Das Feld **Vorzeichen umkehren** unterstützt auch das Ändern der bestellten Menge, indem das Vorzeichen der Menge für Auftragspositionen, die hinzugefügt werden, geändert wird. Dies ist möglicherweise nützlich, wenn Sie eine Transaktion rückgängig machen müssen, indem Sie Auftragspositionen erstellen, die die Transaktion negieren. Diese Option ist automatisch ausgewählt, wenn die Seite von der Aktivität **Gutschrift erstellen** aus geöffnet wird.  
    - Die Option **Belastungen kopieren** ermöglicht es Ihnen, Belastungen zu Ihrem neuen Auftrag vom Dokument aus zu kopieren, aus dem Sie die Auftragspositionen kopieren.  
    - Die Option **Preise neu berechnen** verwendet die aktuellen Preise und Rabatte, statt sie aus dem Dokument zu kopieren, aus dem Sie andere Informationen kopieren.  
    - Die Option **Exakt kopieren** erstellt Kopien der Werte verschiedener Felder in der Kopfzeile und den Positionen des Auftrags. Wenn diese Option nicht ausgewählt ist, werden Standardwerte für viele der Felder in Bezug auf den Kreditor und Produkte verwendet, so als ob Sie manuell einen neuen Auftrag erstellen würden. Wenn Sie zum Beispiel **Exakt kopieren** auf *Ja* festlegen und einen Auftrag kopieren, der das standardmäßige Rechnungskonto für den Kreditor überschreibt, wird dasselbe Rechnungskonto zu Ihrem neuen Auftrag kopiert. Wenn Sie **Exakt kopieren** auf *Nein* festgelegt haben, wird stattdessen das standardmäßige Rechnungskonto für den Kreditor für Ihren neuen Auftrag verwendet. Werte für die folgenden Felder werden kopiert, wenn **Exakt kopieren** auf *Ja* festgelegt ist:
        - Sprache
        - Zahlungsbedingungen
        - Zahlungsmethode
        - Zahlungsspezifikation
        - Nummernkreisgruppe
        - Skonto
        - Rabattprozentsatz
        - Währung
        - Lieferbedingungen
        - Lieferart
        - Dimension
        - Mehrwertsteuergruppe
        - Mehrwertsteuerüberschreibung
        - Preise inkl. Mehrwertsteuer
        - Transport
        - Port
        - Intrastat-Statistikverfahren
        - Vorlagenkennung
        - Liefername
        - Postadresse
        - Referenz
        - Referenz-Tabellen-ID
    - Die Option **Bestellpositionen löschen** löscht alle Bestellpositionen, die bereits in der Bestellung vorhanden sind, zu der Sie kopieren, bevor die neuen Positionen angewendet werden. Verwenden Sie diese Option mit Vorsicht, da durch sie alle vorhandenen Positionen ohne weitere Warnung gelöscht werden.  
    - Wenn Sie die Option **Auftragskopf kopieren** verwenden, müssen Sie die Kopfzeileninformationen für Ihren neuen Auftrag nicht zuerst manuell erstellen. Diese Option führt dazu, dass Standardwerte für die Felder verwendet werden, die dem Kreditor zugeordnet sind. Wenn das Dokument, aus dem Sie kopieren, keine Standardwerte hat, die Sie kopieren möchten, verwenden Sie die Option **Exakt kopieren**.
    - Es gibt verschiedene Dokumentquellen, aus denen Sie kopieren können. Jede hat einen getrennten Abschnitt auf dieser Seite. Zum Beispiel gestattet es der Abschnitt **Bestellungen** Ihnen, aus vorhandenen Bestellungen zu kopieren.  

1. Im Abschnitt **Bestellungen** wählen Sie die Zeilen aus, die in die Zwischenablage kopiert werden sollen. Es ist möglich, zusätzliche Bestellpositionen aus anderen Bestellungen auszuwählen und sie auch in Ihren Auftrag zu kopieren. Es ist ebenfalls möglich, Positionen aus anderen Arten von Einkaufsbelegen hinzuzufügen. In den nächsten Schritten werden die verschiedenen Optionen überprüft.  
1. Erweitern Sie den Abschnitt **Bestätigung**. Hier können Sie Bestellungsbestätigung auswählen, um von ihnen zu kopieren. Die Bestellungsbestätigungen werden durch die zugeordnete Einkaufserfassungskennung oder die Bestellungskennung identifiziert.  
1. Erweitern Sie den Abschnitt **Produktzugänge**. Hier können Sie Produktzugangserfassungen auswählen, um von ihnen zu kopieren. Die Produktzugangserfassungen werden durch die Produktzugangsbescheinigung oder die Bestellungskennung identifiziert.
1. Erweitern Sie den Abschnitt **Rechnungen**. Hier können Sie Kreditorenrechnungen auswählen, um von ihnen zu kopieren. Die Rechnungen werden durch den Rechnungsbeleg oder die Bestellungskennung identifiziert.
1. Erweitern Sie den Abschnitt **Zum Kopieren ausgewählte Positionen oder Kopfzeile**. Diese Ansicht zeigt eine Zusammenfassung aller Dokumente und Positionen an, die ausgewählt worden sind, um zu Ihrem Auftrag kopiert zu werden.
1. Wählen Sie **OK**. Die Positionen, die Sie ausgewählt haben, sind zu Ihrer neuen Bestellung kopiert worden.

## <a name="copy-lines-to-an-existing-purchase-order"></a>Positionen in eine vorhandene Bestellung kopieren  

Anstatt einen gesamten Auftrag zu kopieren, ist es üblicher, eine neue Bestellung zu erstellen und Informationen im Bestellungskopf auszufüllen und dann die einzelnen Positionen aus vorhandenen Aufträgen zu kopieren.  

1. Wählen Sie die Position **Bestellung** aus.
1. Wählen Sie **Aus allen** aus. Die Seite, die sich öffnet, ist mit jender identisch, die zuvor angezeigt wurde, aber verschiedene Optionen sind ausgewählt, wenn sie von der Auftragspositionsansicht aus geöffnet wird. Überprüfen wir die Parameter.
1. Erweitern Sie den Abschnitt **Parameter**.

    - Die Option **Bestellpositionen löschen** ist nicht ausgewählt. Dies heißt, dass Sie neue Positionen zu Ihrem Auftrag kopieren können, ohne vorhandene Positionen zu entfernen.
    - Die Option **Auftragskopf kopieren** ist nicht ausgewählt, da wir dem Auftrag nur zusätzliche Positionen hinzufügen.
    - Für dieses Beispiel kopieren wir nun Positionen aus einer vorhandenen Bestellung.

1. Wählen Sie die Position für die gewünschte Bestellung aus. Beachten Sie, dass die einzelne Auftragsposition, die auf dieser Bestellung ist, ebenfalls ausgewählt ist.  
1. Wählen Sie **OK**. Die zusätzliche Auftragsposition ist Ihrer Bestellung hinzugefügt worden.  

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]