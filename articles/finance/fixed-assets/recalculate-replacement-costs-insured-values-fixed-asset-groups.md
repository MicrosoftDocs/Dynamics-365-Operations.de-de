---
title: Neuberechnung von Wiederbeschaffungskosten und versicherten Werten für Anlagengruppen
description: Dieser Artikel beschreibt den Prozess der Aktualisierung von Wiederbeschaffungskosten und versicherten Werten für Anlagen.
author: ShylaThompson
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 3261
ms.assetid: b8876f83-8772-4f2a-b277-12724e2a0c44
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c0509c0ea2fe6e4d04aeec451969a81eb33b1d19
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826298"
---
# <a name="recalculate-replacement-costs-and-insured-values-for-fixed-asset-groups"></a>Neuberechnung von Wiederbeschaffungskosten und versicherten Werten für Anlagengruppen

[!include [banner](../includes/banner.md)]

Dieser Artikel beschreibt den Prozess der Aktualisierung von Wiederbeschaffungskosten und versicherten Werten für Anlagen.

Möglicherweise werden Sie in regelmäßigen Abständen darüber informiert, dass sich die Wiederbeschaffungs- oder Versicherungskosten für eine bestimmte Anlage geändert haben. So könnte Sie beispielsweise Ihr Vorgesetzter davon in Kenntnis setzen, dass die Inflation im letzten Jahr drei Prozent betrug und somit die Wiederbeschaffungskosten aller Anlagen um drei Prozent erhöht werden müssen. 

Zwar können die Wiederbeschaffungskosten sowie die versicherten Werte einzelner Anlagen auf der Seite **Anlagen** bearbeitet werden, zum gleichzeitigen Aktualisieren dieser Werte für eine Gruppe von Anlagen empfiehlt sich jedoch die Verwendung der Seite **Wiederbeschaffungskosten und versicherte Werte aktualisieren**. Diese Informationen beschreiben, wie Sie Werte für Anlagengruppen oder bestimmte Anlagen in Gruppen aktualisieren.

## <a name="how-values-are-updated"></a>Aktualisieren von Werten
Geben Sie zur Neuberechnung von Wiederbeschaffungskosten und versicherten Werten für Anlagengruppen zunächst den Prozentwert an, um den die vorhandenen Wiederbeschaffungskosten und versicherten Werte geändert werden sollen, und führen Sie anschließend zur tatsächlichen Neuberechnung der Werte die periodische Aktualisierung aus. Sie geben den Prozentsatz in den Feldern **Wiederbeschaffungskostenfaktor** und **Faktor für versicherten Wert** auf der Seite **Anlagengruppen** an. Diese Faktoren werden zwar für die Anlagengruppe angegeben, bei Verwendung der Seite **Wiederbeschaffungskosten und versicherte Werte aktualisieren** können Sie jedoch auswählen, dass die Wiederbeschaffungskosten sowie der versicherte Wert lediglich für bestimmte Anlagen in einer Gruppe neu berechnet werden sollen. 

Wenn Sie die Seite **Wiederbeschaffungskosten und versicherte Werte aktualisieren** verwenden, um die Wiederbeschaffungskosten und den versicherten Wert für die Anlagen neu zu berechnen, werden die folgenden Formeln verwendet:

-   \[(Wiederbeschaffungskostenfaktor der Anlagengruppe / 100) + 1\] \* vorhandene Wiederbeschaffungskosten der Anlage
-   \[(Versicherter Wert der Anlagengruppe / 100) + 1\] \* vorhandener versicherter Wert der Anlage

> [!NOTE] 
> Wenn Sie die Seite **Wiederbeschaffungskosten und versicherte Werte aktualisieren** verwenden, werden sowohl die Wiederbeschaffungskosten als auch der versicherte Wert der ausgewählten Anlagen aktualisiert. Die Aktualisierung lediglich eines der Werte ist nicht möglich. Soll lediglich einer der Werte aktualisiert werden, während der andere Wert unverändert bleibt, geben Sie als Faktor auf der Seite **Anlagengruppen** den Wert 0 (null) ein. Wenn Sie den Faktor 0 oder keinen Wert eingeben, wird die Berechnung bei der Aktualisierung übersprungen. Buchwert und Nettobuchwert von Anlagen sind von der periodischen Aktualisierung nicht betroffen. 

## <a name="how-to-use-a-date-to-select-which-items-to-update"></a>Auswählen der zu aktualisierenden Artikel mithilfe eines Datums
Standardmäßig werden durch den Aktualisierungsprozess die ausgewählten Anlagen aktualisiert, bei denen am aktuellen Tag noch keine Aktualisierung stattgefunden hat, die aber möglicherweise an früheren Tagen aktualisiert wurden. Beispielsweise &lt; bedeutet aktuelles Datum "vor dem heutigen Datum". Sie können das Datum auf der Seite **Wiederbeschaffungskosten und versicherte Werte aktualisieren** ändern, indem Sie auf die Schaltfläche **Auswählen** klicken. Die angegebenen Datumskriterien werden mit dem Datum der letzten periodischen Aktualisierung für die Anlage (dem Feld **Letzter periodischer Wert/Kostenaktualisierung** auf der Seite **Anlagen**) verglichen. Nach jeder erfolgreichen Aktualisierung der Wiederbeschaffungskosten oder des versicherten Werts einer Anlage wird das Feld **Letzter periodischer Wert/Kostenaktualisierung** automatisch auf das aktuelle Datum aktualisiert. 

Beispiel 

Gestern wurden die Wiederbeschaffungskosten für die Gruppe "Fuhrpark, Büroausstattung und Gebäude" per Aktualisierung um fünf Prozent geändert. Damit diese Anlagen von der heutigen Aktualisierung aller anderen Anlagen ausgeschlossen werden, geben Sie im Feld **Letzter periodischer Wert/Kostenaktualisierung** ein Datum ein, das vor dem gestrigen Tag liegt (&lt; Datum von gestern), da die letzte Aktualisierung für die Gruppen **Fuhrpark**, **Büroausstattung** und **Gebäude** außerhalb der eingegebenen Datumskriterien stattfand.

## <a name="cumulative-effect-of-each-update"></a>Kumulative Wirkung der einzelnen Aktualisierungen
Jede Aktualisierung besitzt eine kumulative Wirkung. Aus diesem Grund müssen die Aktualisierungen stets sehr sorgfältig geplant werden. Beispiel: Am Dienstag werden alle Anlagen um drei Prozent erhöht. Am Freitag wird eine Erhöhung für "Büroausstattung" um vier Prozent vorgenommen. In diesem Fall beträgt die Gesamterhöhung für "Büroausstattung" 7,12 Prozent.

## <a name="scenario"></a>Szenario
Ihr Vorgesetzter informiert Sie über die folgenden Änderungen für Anlagen:
-   Erhöhung der Wiederbeschaffungskosten aller Anlagen (ausgenommen Computer) um 3,25 Prozent
-   Erhöhung der Wiederbeschaffungskosten bei der gesamten Büroausstattung um ein weiteres Prozent
-   Verringerung der Wiederbeschaffungskosten sowie des versicherten Werts aller Computer um 10 Prozent

Sie nehmen die folgenden Änderungen vor:
1.  Geben Sie auf der Seite **Anlagengruppen** für alle Anlagengruppen außer der Gruppe **Büroausstattung** und **Computer** den Wert 3,25 im Feld **Wiederbeschaffungskostenfaktor** ein sowie 0 im Feld **Faktor für versicherten Wert** ein.
2.  Geben Sie für die Gruppe **Büroausstattung** den Wert 4,25 im Feld **Wiederbeschaffungskostenfaktor** und 0 im Feld **Faktor für versicherten Wert** ein.
3.  Geben Sie für die Gruppe **Computer** den Wert -10 im Feld **Wiederbeschaffungskostenfaktor** und -10 im Feld **Faktor für versicherten Wert** ein.
4.  Auf der Seite **Wiederbeschaffungskosten und versicherte Werte aktualisieren** klicken Sie auf **OK**, um die Neuberechnung für alle Anlagen auszuführen.

Am nächsten Tag teilt Ihnen Ihr Vorgesetzter mit, dass die Verringerung bei den Computern nicht zehn, sondern lediglich acht Prozent beträgt und die Wiederbeschaffungskosten sowie die versicherten Werte deshalb geändert werden müssen. Für die Behebung dieses Fehlers stehen zwei Methoden zur Verfügung:
-   Ändern Sie auf der Seite **Anlagen** die Felder **Versicherter Wert** und **Wiederbeschaffungskosten** für jede Anlage der Anlagengruppe **Computer** manuell. Berechnen Sie die Werte so, als hätten Sie den ursprünglichen Betrag um acht Prozent verringert, und geben Sie diese Werte ein. Mithilfe dieser Methode verwenden Sie nicht die Seite **Wiederbeschaffungskosten und versicherte Werte aktualisieren**.
-   Geben Sie die Faktoren für Wiederbeschaffungskosten und versicherten Wert für die Gruppe **Computer** in den Feldern **Wiederbeschaffungskostenfaktor** und **Faktor für versicherten Wert** auf der Seite **Anlagengruppen** ein. Dadurch werden die Anlagen auf ihren ursprünglichen Wert (vor der zehnprozentigen Verringerung) zurückgesetzt, und die achtprozentige Verringerung wird auf den ursprünglichen Wert angewendet. Verwenden Sie dann die Seite **Wiederbeschaffungskosten und versicherte Werte aktualisieren**, um die Werte neu zu berechnen, abhängig von den Faktoren, die Sie eingegeben haben.

> [!NOTE]  
> Der Faktor "-10" lässt sich nicht durch Eingabe eines positiven Faktors mit dem Wert "10" (oder durch Eingabe des Faktors "2" – also der Differenz zwischen "-10" und "-8") rückgängig machen, da die Beträge dann nicht korrekt berechnet werden. 







[!INCLUDE[footer-include](../../includes/footer-banner.md)]