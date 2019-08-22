---
title: Ermittelt die optimale Kombination von überlappenden Rabatten
description: Wenn Rabatte überlappen, müssen Sie die Kombination von Rabatten überlappenden bestimmen, die Buchungssumme niedrigsten oder höchsten den Rechnungsrabatt erzeugen. Wenn der Rabattbetrag gemäß dem Preis der gekauften Produkte schwankt, wie bei üblichen Aktionen wie „kaufen 1 günstiger erhalten“ (BOGO), wird dieser Prozess ein Thema der kombinatorischen Optimierung.
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters, RetailPeriodicDiscount,
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 89643
ms.assetid: 09843c9a-3e19-4e4a-a8ce-80650f2095f9
ms.search.region: global
ms.search.industry: Retail
ms.author: kfend
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 00d7457b13e6633c9285a1fc43b8f6dd60dae9ae
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836531"
---
# <a name="determine-the-optimal-combination-of-overlapping-discounts"></a>Ermittelt die optimale Kombination von überlappenden Rabatten

[!include [banner](includes/banner.md)]

Wenn Rabatte überlappen, müssen Sie die Kombination von Rabatten überlappenden bestimmen, die Buchungssumme niedrigsten oder höchsten den Rechnungsrabatt erzeugen. Wenn der Rabattbetrag gemäß dem Preis der gekauften Produkte schwankt, wie bei üblichen Aktionen wie „kaufen 1 günstiger erhalten“ (BOGO), wird dieser Prozess ein Thema der kombinatorischen Optimierung.

Dieser Artikel gilt für Microsoft Dynamics AX 2012 R3 mit KB 3105973 (veröffentlicht am 2. November 2015) oder höher und für Microsoft Dynamics 365 for Retail. Damit die Kombination sich überschneidender Rabatte zeitnah angewendet werden kann, haben wir eine Methode zum Anwenden sich überschneidender Rabatte eingeführt. Es erhalten diese neue Methode angezeigt **Schwellenwertklassifizierung**. Die Schwellenwertklassifizierung wird verwendet, wenn die Zeit, die erforderlich ist, um die möglichen Kombinationen von sich überschneidenden Rabatten zu bewerten, einen Schwellenwert überschreitet, der auf der Seite **Einzelhandelsparameter** konfigurierbar ist. In der Schwellenwertklassifizierungsmethode wird ein Wert für jeden überlappenden Rabatt berechnet, indem der Wert des Rabatts auf den freigegebenen Produkten verwendet. Die überlappenden Rabatte werden dann dem höchsten relativen Wert der niedrigste relativen Wert angewendet. Einzelheiten über die neue Methode, lesen Sie den Abschnitt "Schwellenwert", später in diesem Artikel. Schwellenwertklassifizierung wird nicht verwendet, wenn Skontobeträgen für das Produkt nicht durch unterschiedliche Produkt in der Buchung betroffen sind. Beispielsweise kann diese Methode nicht für zwei einfache Rabatte oder einen einfachen Rabatt und einen einzelnen Produktmengenrabatt verwendet.

## <a name="discount-examples"></a>Rabattbeispiele

Sie können eine unbegrenzte Anzahl an Einzelhandelsrabatten für eine allgemeines Set an Produkten erstellen. Da jedoch kein Limit festgelegt ist, können Leistungsprobleme auftreten, wenn Sie versuchen, die Rabatte zu berechnen, die auf den verschiedenen Produkten verwendet werden sollen. Die folgenden Beispiele veranschaulichen dieses Problem genauer. In Beispiel 1 beginnen, wir mit zwei Produkten und zwei überlappenden Rabatten. Im Beispiel 2, zeigen wir, wie das Problem, entwickelt für weitere Produkte hinzugefügt werden.

### <a name="example-1-two-products-and-two-discounts"></a>Beispiel 1: Zwei beiden Rabatte und Produkte

In diesem Beispiel wurden zwei Produkte erforderlich, das für jeden Rabatt zu erlangen, und Rabatte können nicht zusammengefasst werden. Die in Rabatte diesem Beispiel sind **Bester Preis** Rabatte. Beide Produkte qualifizieren der beiden Rabatte. Hierbei gelten die beiden Rabatte.

![Beispiel zweiter bester Preisrabatte](./media/overlapping-discount-combo-01.jpg)

Bei zwei Produkten hängt der bessere der beiden Rabatte vom Preis der beiden Produkte ab. Wenn der Preis beider Produkte oder gleich fast gleich ist besser, Skonto 1. Wenn der Preis aus einem Produkt bei geringer als der anderen Preis des Produkts ist besser, Rabatt ist 2. Hier ist die mathematischen Regel zur Abwägung der beiden Rabatte gegeneinander.

![Regel für die Bewertung der Rabatte](./media/overlapping-discount-combo-02.jpg)

> [!NOTE]
> Wenn der Preis von Produkt 1 gleich Zweidrittel des Preises von Produkt 2 beträgt, sind die beiden Rabatte identisch. In diesem Beispiel ist der zum Diskont effektive Rabattprozentsatz 1 von einigen Prozent (wenn die Preise der beiden Produkte weites getrennt sind), bis zu maximal 25 Prozent (wenn die Produkte zwei denselben Preis haben). Der Rabattprozentsatz für den Skonto 2 ist fest. Es ist immer 20 Prozent. Da der gültigen Rabattprozentsatz für Skonto 1 einen Bereich hat, der mehr als Rabatt oder kleiner als 2 sein kann, hängt der beste Rabatt von Preisen der beiden Produkte aus, die für den Rabatt gewährt werden müssen. In diesem Beispiel wird die Berechnung schnell ausgefüllt, da nur beiden Rabatte auf nur zwei Produkten angewendet werden. Es gibt lediglich zwei mögliche Kombinationen: eine Bewerbung der Anwendung des Rabatts 1 oder einen Rabatt. 2. Es sind keine zuzuteilenden Belastungen vorhanden. Der Wert jedes Rabatt wird berechnet, indem das sowohl Produkte verwendet, und der beste Rabatt wird verwendet.

### <a name="example-2-four-products-and-two-discounts"></a>Beispiel 2: Vier beiden Rabatte und Produkte

Danach verwenden Sie vier Produkte und dieselben beiden Rabatte. Alle vier Produkte qualifizieren der beiden Rabatte. Es gibt zwölf mögliche Kombinationen. Am Ende der Buchung werden beiden Rabatte auf drei verschiedene Kombinationen verwendet: Anwendungen zwei von Skonto 1, zwei Bewerbungen der Anwendung des Rabatts 2 oder einer der Anwendung des Rabatts 1 und einer von Rabatt. 2. Um die möglichen Kombinationen zum Demonstrieren, beachten Sie zwei verschiedene Gruppen der Produkte die vier verschiedene Preise haben:

- Alle vier Produkte denselben Preis haben, €15,00. In diesem Fall ist die beste Rabattkombination zwei Bewerbungen von Rabatt. 1. Zwei Produkte sind voller Preis, und sind zwei heruntergesetzt 50 Prozent. Die rabattierte Summe für die Buchung ist €45 (15 + 15 + 7,50 + 7,50), die €15 (25 Prozent) die zur Abrundung der nicht-rabattierten Summe von €60 ist. Skonto 2 ist nur €12 (20 Prozent).
- Zwei Produkte sind €20 je, ist ein Produkt €15, und das Produkt ist €5. In diesem Fall ist die beste Rabattkombination eine Bewerbung der Anwendung des Rabatts 2 und einer erweiterten Rabatts. 1. Die folgenden Tabellen wird gezeigt Rabatte.

Um die Tabellen gelesen, verwenden Sie ein Produkt aus einer Zeile und ein Produkt aus einer Spalte. In der Tabelle für Skonto 1, wenn Sie mit den beiden €20 Produkte kombinieren, werden Sie bei €10 ab. In der Tabelle für Skonto 2, wenn Sie mit den €15 Produkt und dem €5 Produkt kombinieren, erhalten Sie €4 Rabatt.

![Beispiel, das vier Produkte für dieselben zwei Rabatte verwendet](./media/overlapping-discount-combo-03.jpg)

Zunächst suchen wir den höchsten Rabatt, der für einen der beiden Produkte verfügbar ist, in dem wir einen der Rabatte anwenden. Die beiden Tabellen zeigen den Rabattbetrag für alle Kombinationen der beiden Produkte angezeigt. Die schattierten Teile der Tabellen finden jeden Fälle, in denen ein Produkt mit dem zugeordnet ist, das von uns nicht ausführen können, oder ein Rückzuordnen zweier Produkten dar, weshalb dieselbe Rabattbetrag hergestellt und ignoriert werden kann. Durch Festlegen der Tabellen einmal genauer anschauen, werden Sie sehen, dass Skonto 1 für die zwei €20 Artikel der größten Rabatt ist, für jeden der Rabatt auf alle vier Produkte verfügbar ist. (Dieser Rabatt wird in grün in der ersten Tabelle. Markieren) Dadurch lassen nur das Produkt €15 und das Produkt €5. Wenn Sie erneut die beiden Tabellen einmal genauer anschauen, werden Sie sehen, dass, für diese beiden Produkte, Skonto 1 einen Rabatt €2,50 gibt, für Skonto 2 einen Rabatt €4 gibt. Daher wird Skonto 2 aus. Der Rechnungsrabatt beträgt €14. Um diese Diskussion zu vereinfachen visualisiert werden, sollten Sie hier zwei zusätzliche Tabellen die der eigentliche Rabattprozentsatz für alle möglichen Zwei-Produktkombinationen für Skonto 1 Skonto 2 und anzeigen. Nur ist Hälfte Liste mit Kombinationen eingeschlossen, weil, für diese beiden Rabatte, den Auftrag, in der zwei die Produkte in den Rabatt angewendet werden, noch ist. Der höchste effektive Rabatt (25 Prozent) wird in grün und niedrigsten im tatsächlichen Rabatt (10 Prozent) markiert wird rot hervorgehoben.

![Effektiver Rabattprozentsatz für alle Zwei-Produkt-Kombinationen für beide Rabatte](./media/overlapping-discount-combo-04.jpg)

> [!NOTE]
> Wenn Preise variieren, und zwei oder mehr Rabatte miteinander konkurrieren, besteht die einzige Möglichkeit, die beste Rabattkombination zu garantieren, darin, beide Rabatte zu bewerten und miteinander zu vergleichen.

## <a name="total-possible-combinations"></a>Insgesamt mögliche Kombinationen

Dieser Abschnitt wird das beispielsweise von vorherigen Abschnitt fort. Es können weitere Produkte und einen anderen Rabatt hinzu und finden, wie viele Kombinationen berechnet und verglichen werden müssen. In der folgenden Tabelle wird die Anzahl für mögliche Rabattkombinationen als die Produktmengenerhöhungen angezeigt. Die Tabelle ist angegeben, was einerseits, wenn zwei überlappende Rabatte gibt, wie im vorherigen Beispiel erfolgt, und wenn es drei überlappende Rabatte gibt. Die Anzahl für mögliche Rabattkombinationen, die demnächst ausgewertet werden müssen, überschreitet, was auch ein Computer schneller berechnen sowie Vergleichen kann schnell genug, um für Einzelhandelstransaktionen akzeptiert werden sollen.

![Anzahl für mögliche Rabattkombinationen bei Erhöhung der Produktmenge](./media/overlapping-discount-combo-05.jpg)

Werden sogar größere Mengen oder mehr sich überschneidende Rabatte angewendet, geht die gesamte Anzahl möglicher Rabattkombinationen schnell in die Millionen. Und die Zeit, die erforderlich ist, die bestmögliche Kombination zu bewerten und auszuwählen, wird schnell spürbar. Einige Optimierungen sind im Kleineinzelhandelspreismodul fertig, aktualisiert die Gesamtanzahl von Kombinationen zu reduzieren, die überprüft werden müssen. Da jedoch die überlappenden Rabatte der Nummer und Mengen in einer Buchung nicht eingeschränkt werden, müssen mehrere Kombinationen immer ausgewertet werden, sobald sich überlappende Rabatte gibt. Dieses Problem wird der Abgang die Schwellenwertklassifizierungs-Methodenadressen.

## <a name="marginal-value-method"></a>Schwellenwertmethode

Um den Abgang einer exponential zunehmenden Anzahl von Kombinationen die Behebung ausgewertet werden müssen, ist eine Optimierung die den Wert pro freigegebenes Produkt jedes Rabatts im Satz von Produkten berechnet die zwei oder mehr Rabatte angewendet werden kann. Wir bezeichnen diesen Wert als **Schwellenwert** des Rabatts für die freigegebene Produkte angezeigt. Der Schwellenwert ist der Durchschnitt pro Produkterhöhung im freigegebenen Gesamtrabattbetrag, wenn die Produkte in den Rabattzeitraum einbezogen werden sollen. Der Schwellenwert wird berechnet, indem der Gesamtrabattbetrag (DTotal), den Rabattbetrag ohne die freigegebene Produkte (DMinus\\Shared) abgezogen, und die Differenz von der Anzahl von freigegebenen Produkten (ProductsShared) geteilt.

![Formel für die Berechnung des Schwellenwerts](./media/overlapping-discount-combo-06.jpg)

Nachdem der Schwellenwert eines jeden Rabatts auf einem freigegebenen Produktsatz berechnet wurde, werden die Rabatte auf die freigegebenen Produkten angewendet, und zwar in der Reihenfolge vom höchsten Schwellenwert bis zu niedrigsten Schwellenwert. Bei dieser Methode werden alle restlichen Rabattmöglichkeiten nicht jedes Mal verglichen, nachdem eine einzelne AOS-Instanz einen Rabatt angewendet wurde. Stattdessen werden einmal verglichen überlappenden die Rabatte angewendet und dann im Auftrag. Keine weiteren Vergleiche durchgeführt werden. Sie können den Schwellenwert konfigurieren, die der auf der Schwellenwertmethode **Rabatt** Registerkarte der **Einzelhandelsparameter** Seite zu wechseln. Die akzeptierte Zeit, den Rechnungsrabatt zu berechnen variiert zu Einzelhandel. Allerdings liegt diese Zeit im Allgemeinen im Bereich der zehnten Millisekunden auf einer Sekunde.
