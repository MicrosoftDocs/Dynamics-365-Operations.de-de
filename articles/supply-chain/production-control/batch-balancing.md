---
title: Chargenausgleich
description: In diesem Artikel wird der Chargenausgleichprozess beschrieben.
author: johanhoffmann
ms.date: 01/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BOMTable, WHSReservationHierarchy, WHSInventTableReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 939066fbf4ab7b316283d406c321f1a7936c187f
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/29/2022
ms.locfileid: "9066545"
---
# <a name="batch-balancing"></a>Chargenausgleich

[!include [banner](../includes/banner.md)]

In diesem Artikel wird der Chargenausgleichprozess unterstützt.

Weitere Informationen erhalten Sie im [Video zum Chargenausgleich](https://www.youtube.com/watch?v=4SNLWsU9KyI&feature=youtu.be)

Im Chargenausgleichprozess wird der Betrag der Substanz zur Verwendung innerhalb einer Produktionscharge von der aus Wirksubstanzen in ausgewählten Produktchargen berechnet.

## <a name="products-that-have-an-active-ingredient"></a>Produkte, die eine Wirksubstanz haben

Ein Produkt kann durch seine Konzentration einer Wirksubstanz definiert werden. Die Wirksubstanz eines Produkts wird modelliert, indem ein produktspezifisches Chargenattribut verwendet wird, das einen Mindestwert, einen Höchstwert und eine Zielstufe hat.

Die Zielstufe eines Chargenattributs stellt den Prozentsatz einer Wirksubstanz in einem Produkt dar. Die Mindest- und Höchstwerte entsprechen der akzeptierten Abweichung von der Zielstufe. Sie können z. B. am Toleranz für Chargen am Produktzugang verwendet werden.

Ein Produkt darf nur eine Wirksubstanz haben. Wenn Sie die Wirksubstanz eines Produkt definieren möchten, müssen Sie ein produktspezifisches Chargenattribut zuerst definieren. Sie ordnen Attributs als Basisattribut des Produkts zu.

Auf der Produktebene müssen Sie auch angeben, ob die Ebene der Wirksubstanz für eine Charge des Fertigprodukts erfasst werden soll: als Teil des Bestellungsempfangsprozesses von oder als Bestandteil eines Qualitätsprüfungsauftragprozesses.

Wenn Sie ein Basisattribut einem einzelnen Produkt zuzuordnen, müssen die folgenden Elemente eingerichtet werden:

- Das Produkt muss in der Charge enthalten sein. Wenn ein Produkt von einer Charge kontrolliert wird, müssen Sie eine Rückverfolgungsangabengruppe dem Produkt zuweisen, das eine aktive Chargendimension hat.

- Das Attribut, das die Inhaltsstoffebene angibt, muss als produktspezifisches Chargenattributs für das fertig gestellte Produkt definiert werden.

So suchen und bearbeiten Sie den tatsächlichen Wert der Wirksubstanz für eine Charge:
1. Wechseln Sie zu **Lagerverwaltung \> Abfragen und Berichte \> Rückverfolgungsangaben \> Chargen**.
1. Wählen Sie eine Chargennummer aus dem Raster.
1. Öffnen Sie im Aktionsbereich die Registerkarte **Ansicht**, und wählen Sie **Lagerchargenattribute** aus.

## <a name="ingredient-types-and-how-they-interact-in-the-batch-balancing-process"></a>Inhaltsstofftypen und wie sie im Chargenausgleichprozess interagieren

Eine Formelposition, die erstellt wird, kann eine dieser Inhaltsstofftypen haben:

- None
- Aktiv
- Kompensation
- Füller

Der Rest dieses Abschnitts enthält Beispiele, die zeigen, wie jeder Inhaltsstofftyp arbeitet. Die Beispiele basieren auf der folgenden Formel, die eine vollständige Chargengröße von 100 Litern hat.

| Typ des Inhaltsstoffs | Artikelnummer | Formelzeilenmenge | Einheit |
|---|---|---|---|
| None | H | 20 | Liter |
| Aktiv | Mrd | 30 | Liter |
| Kompensation | C | 10 | Liter |
| Füller | S | 40 | Liter |

Die folgende Tabelle gibt einen Überblick über die Ergebnisse der einzelnen Beispiele.

| Artikelnummer | Typ des Inhaltsstoffs | Vorkalkulierte Menge | Saldomenge | Aktive Menge | Einheit | Basiswert |
|---|---|---|---|---|---|---|
| H | None | 20 | 20 | | Liter | |
| b | Aktiv | 30 | 25.71 | 9:00 | Liter | 30.00 |
| C | Kompensation | 10 | 14.72 | | Liter | |
| S | Füller | 40 | 39.57 | | Liter | |

### <a name="active-ingredients"></a>Wirksubstanzen

Wenn einem Produkt, das ein Basisattribut hat, eine Formelposition hinzugefügt wird, wird es als *Wirksubstanz* der Formel. Chargenaufträge, die Formeln haben, die Wirksubstanzen enthalten, können für den Chargenausgleichprozess verwendet werden. Für jede Substanz in der Formel schätzt der Chargenausgleichprozess den Betrag, der erforderlich ist, um das Produkt herzustellen. Die Vorkalkulation von Beträgen basiert auf der Konzentration der Wirksubstanzen in der ausgewählten Charge.

#### <a name="active-ingredient-example"></a>Beispiel für Wirksubstanz

Ihaltsstoff B hat Basisattribut X und Zielstufe von 30 und ist in einer Formel enthalten, die 30 Liter des Inhaltsstoffs B für alle 100 Liter des Produkts benötigt. Ein Chargenauftrag wird erstellt, der die Chargengröße von 100 Litern hat. Der Chargenauftrag wird gestartet und während dem gesamten Chargenausgleichprozesses wählt der Benutzer eine Charge des Inhaltsstoffs B aus, der ein Stärkeniveau von 35 hat. Da das Stärkeniveau von 35 höher ist als die Zielstufe 30, wird die ausgeglichene Menge des Inhaltsstoffs B verringert, indem das Verhältnis des Stärkewerts der Zielstufe der Charge verwendet, die von der vorkalkulierten Menge multipliziert wird. Die Berechnung der ausgeglichenen Menge sieht wie folgt aus:

(30 ÷ 35) × 30 Liter = 25,71 Liter

### <a name="none-ingredients"></a>Keine Substanzen

Wenn Sie den Chargenausgleichprozess anwenden und der **Typ der Substanz** *Keiner* lautet, sind die vorkalkulierte Menge und die ausgeglichene Menge der Formelposition im Chargenauftrag identisch.

#### <a name="none-ingredient-example"></a>Beispiel für keine Substanz

Substanz A ist einer Substanz im Typ *Keine* zugewiesen und hinzugefügt einer Formel für ein Produkt. Die Formel erfordert 10 Liter Inhaltsstoff von A für alle 100 Liter des Produkts. Erfordert ein Chargenauftrag 200 Liter, werden die vorkalkulierte Menge und die ausgeglichene Menge als 20 Liter berechnet.

### <a name="compensating-ingredients"></a>Kompensationssubstanzen

Eine Kompensationssubstanz kann entweder die Auswirkungen der Wirksubstanz in einem Produkt ergänzen oder ausgleichen. Daher hängt die Menge einer Kompensationssubstanz, die verbraucht wird, von der Stärke des Produkts ab:

- **Gegenüberliegende Auswirkungen** – Wenn der Betrag der Wirksubstanz höher ist als angenommen, müssen Sie weniger von der Kompensationssubstanz hinzufügen.

- **Ergänzende Auswirkungen** – Wenn der Betrag der Wirksubstanz kleiner ist als angenommen, müssen Sie mehr von der Kompensationssubstanz hinzufügen.

Die Beziehung zwischen einer Wirksubstanz und einer ergänzenden Substanz wird auf der Seite **Kompensierendes Prinzip** eingerichtet.

Folgen Sie diesen Schritten, um die Beziehungen zwischen Substanzen einzurichten.

1. Wählen Sie **Produktinformationsverwaltung \> Stücklisten und Formeln \> Formeln** aus.
1. Öffnen Sie eine Formelposition, und wählen Sie **Substanzen** aus, um die Seite **Kompensierendes Prinzip** zu öffnen.
1. Wählen Sie die Position aus, die ein kompensierendes Prinzip darstellt, und wählen Sie dann zum Ausgleichen Wirksubstanz aus.

Im kompensierenden Prinzip geben Sie auch einen positiven oder negativen kompensierenden Faktor ein, um anzugeben wie viel zu entschädigen ist und ob das Prinzip entgegensetzend oder ergänzend ist. Ein positiver Faktor zeigt eine ergänzenden Auswirkungen an, und ein negativer Faktor zeigt eine umgekehrte Auswirkung an.

#### <a name="compensating-ingredient-example"></a>Beispiel für Kompensationssubstanz

Inhaltsstoff B ist eine Wirksubstanz, die Basisattribut X und eine Zielstufe von 30 an hat. Die Formel erfordert 30 Liter Substanz von A für alle 100 Liter des Produkts. Inhaltsstoff C ist eine Kompensationssubstanz, und die Menge 10 ist in der gleichen Formel aufgenommen. Ein kompensierender Faktor von 1.10 wird für das kompensierende Prinzip eingerichtet. Daher wird die ausgeglichene Menge der Kompensationssubstanz reduziert um den Unterschied der Differenz zwischen der Menge der Wirksubstanz und der vorkalkulierten Menge verringert, die mit 1,10 multipliziert wird.

Im Beispiel für den *Aktiven* Substanztyp wurde die ausgeglichene Menge der erforderlichen Wirksubstanz als 25,71 berechnet und die erforderliche vorkalkulierte Menge wurde als 30 berechnet. In diesem Fall wird die ausgeglichene Menge der Kompensationssubstanz so berechnet:

1. Die Differenz zwischen der erwarteten und ausgeglichenen Menge wird bestimmt:  
    25.71 – 30 = –4.29

1. Das Ergebnis wird dann mit dem Jahresbetrag multipliziert.  
    4.29 × 1.10 = –4.72

1. Die vorkalkulierte kompensierte Menge wird durch – 4,72 verringert, um die ausgeglichene kompensierende Menge zu bestimmen:  
    10 – (–4.72) = 14.72

Da 1.10 ein positiver kompensierender Faktor ist, hat dieses kompensierende Prinzip eine zusätzliche Auswirkung. In diesem Fall ist die Wirksubstanz stärker als angenommen. Daher ist der Kompensationssubstanz erforderlich.

### <a name="filler-ingredients"></a>Füllsubstanzen

*Füllsubstanz* ist eine neutrale Substanz, die verwendet wird, um die gewünschte Berechnung des Produkts zu geben. Änderungen an Füllermengen werden auf Grundlage der Schwankungen der Wirksubstanz und der Kompensationssubstanz berechnet, mit der die Standardmenge verglichen wird.

#### <a name="filler-ingredient-example"></a>Beispiel für Füllsubstanz

Sie haben ein Produkt formuliert, die Zutaten A, B, C und D für eine Formelgröße von 100 Litern enthält. Sie besitzen die ausgeglichene Menge aller Substanztypen außer der *Füller*-Substanztyp, der in einer Position verwendet wird.
Ausgeglichene Menge der Füllsubstanz wird als Unterschied zwischen der Chargengröße von 100 Litern und der Summe der Inhaltsstoffe A, B und C berechnet:

100 – (20 + 25.71 + 14.72) = 39.57

## <a name="the-batch-balancing-process"></a>De Chargenausgleichprozess anzeigen

Der Chargenausgleichprozess wird durch den **Chargenausgleich** ausgeführt.
Wählen Sie **Kostenverwaltung \> Chargenaufträge** und dann auf der Registerkarte **Prozess** **Chargenausgleich** aus. Chargenausgleich ist verfügbar für Chargenaufträge, die den Status **Gestartet** besitzen.

Im Allgemeinen kann der Chargenausgleich in den Chargenaufträgen angewendet werden, wenn die Formel mindestens eine Formelposition mit dem **Typ der Substanz** *Aktiv* hat. (Für die Ausnahme von dieser Regel, lesen Sie "Chargenaufträge, die nicht für Chargenausgleich gelten im Abschnitt weiter unten in diesem Artikel).

Der Chargenausgleichprozess kann in zwei Unterprozesse unterteilt werden:

1. Chargensubstanzausgleich
1. Bestätigen und Formel eingeben

### <a name="balance-batch-ingredients"></a>Chargensubstanzausgleich

Im Chargenausgleichprozess wird der Betrag der Substanz zur Verwendung innerhalb einer Produktionscharge von der aus Wirksubstanzen in ausgewählten Produktchargen berechnet. Normalerweise kann die Berechnung abgeschlossen werden, wenn es eine vollständig Deckung aller Inhaltsstoffe gibt. Sie können nur einen Teil der Charge nicht ausgeglichen, für den der Chargenauftrag für die Produktion eingerichtet ist.

> [!NOTE]
> Sie können eine Berechnung nicht speichern und den Chargenausgleichprozess später abschließen. Wenn Sie die Detailebene **Chargenausgleich** schließen, müssen Sie die Berechnung wiederholen, damit der entsprechende Vorgang abgeschlossen werden kann.

### <a name="confirm-and-release-the-formula"></a>Bestätigen und Formel eingeben

Nachdem die Inhaltsstoffmengen berechnet wurden, können Sie die Formel bestätigen und freigeben. Der Freigabeprozess unterscheidet sich, je nachdem, ob die Produkte für Lagerverwaltungsprozesse (WMS) aktiviert sind:

- Wenn ein Produkt für WMS aktiviert ist, wird die Formelzeile gemäß den Grundsätzen für WMS für das Lager freigegeben. Die Formelposition wird anhand der produzierten Produktmengen freigegeben, die den ausgeglichenen Mengen entsprechen und für die Primärressource sowie für bestimmte Chargen freigegeben wird, die für die Wirksubstanzen ausgewählt werden.

    > [!NOTE]
    > Formelpositionen können zum Lagerort nur als Teil des Chargenausgleichprozesses freigegeben werden. Obwohl es andere Optionen bei der gemeinsamen Nutzung von Material für Produktion in Lagerort gibt, können diese Optionen nicht für Formelpositionen verwendet werden.

- Wenn ein Produkt nicht für WMS aktiviert ist, wird eine Produktions-Kommissionierliste für das Produkt erstellt, wenn Sie die Formel bestätigen und freigeben.

In einer einzelnen Formel können Sie Produkte kombinieren, die für die Lagerortverwaltungsprozesse aktiviert sind und Produkte, die nicht für die Lagerortverwaltung verarbeitet, aktiviert werden. Wenn die beiden Produkttypen in einer Formel enthalten sind, werden die Produkte, die für das WMS aktiviert sind, für das Lager freigegeben. Für die Produkte, die nicht für WMS aktiviert sind, wird eine Kommissionierliste erstellt, wenn die Formel bestätigt und freigegeben wird.

### <a name="batch-orders-that-arent-applicable-for-batch-balancing"></a>Chargenaufträge, die nicht für Chargenausgleich gelten

Es gibt zwei Ausnahmen zur Regel, dass Chargenausgleiche in den Chargenaufträgen angewendet werden, wenn die Formel mindestens eine Formelposition mit dem **Typ der Substanz** *Aktiv* hat.

1. Wenn eine Formel einen Wirkstoff für ein Produkt enthält, das für das WMS aktiviert ist, aber die Batch-Nummer in der Reservierungshierarchie unter dem Ort steht, ist der Batch-Auftrag nicht für den Batch-Abgleich geeignet.
1. Wenn sich die Formelmaßeinheit von der Lagermaßeinheit der Wirksubstanz unterscheidet, gilt der Chargenauftrag nicht für den Chargenausgleich.

Ein Chargenauftrag, der nicht für Chargenausgleich anwendbar ist, durchläuft den normalen Prozesszyklus für Chargenaufträge.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]