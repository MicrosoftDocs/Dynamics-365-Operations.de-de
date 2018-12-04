---
title: Chargenausgleich
description: In diesem Thema wird der Chargenausgleichprozess beschrieben.
author: johanhoffmann
manager: AnnBe
ms.date: 03/15/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 7d00df6263530ba9fff4c246cb3593cd607f6719
ms.contentlocale: de-de
ms.lasthandoff: 04/13/2018

---

# <a name="batch-balancing"></a>Chargenausgleich

[!include [banner](../includes/banner.md)]

In diesem Thema wird der Chargenausgleichprozess unterstützt. 

Sehen Sie ein [Video über den Chargenausgleich in Microsoft Dynamics 365 for Finance and Operations](https://www.youtube.com/watch?v=4SNLWsU9KyI&feature=youtu.be) an

Im Chargenausgleichprozess wird der Betrag der Substanz zur Verwendung innerhalb einer Produktionscharge von der aus Wirksubstanzen in ausgewählten Produktchargen berechnet.

<a name="products-that-have-an-active-ingredient"></a>Produkte, die eine Wirksubstanz haben
---------------------------------------

Ein Produkt kann durch seine Konzentration einer Wirksubstanz definiert werden. Die Wirksubstanz eines Produkts wird modelliert, indem ein produktspezifisches Chargenattribut verwendet wird, das einen Mindestwert, einen Höchstwert und eine Zielstufe hat.

Die Zielstufe eines Chargenattributs stellt den Prozentsatz einer Wirksubstanz in einem Produkt dar. Die Mindest- und Höchstwerte entsprechen der akzeptierten Abweichung von der Zielstufe. Sie können z. B. am Toleranz für Chargen am Produktzugang verwendet werden.

Ein Produkt darf nur eine Wirksubstanz haben. Wenn Sie die Wirksubstanz eines Produkt definieren möchten, müssen Sie ein produktspezifisches Chargenattribut zuerst definieren. Sie ordnen Attributs als Basisattribut des Produkts zu.

Auf der Produktebene müssen Sie auch angeben, ob die Ebene der Wirksubstanz für eine Charge des Fertigprodukts erfasst werden soll: als Teil des Bestellungsempfangsprozesses von oder als Bestandteil eines Qualitätsprüfungsauftragprozesses.

Wenn Sie ein Basisattribut einem einzelnen Produkt zuzuordnen, müssen die folgenden Elemente eingerichtet werden:

-   Das Produkt muss in der Charge enthalten sein. Wenn ein Produkt von einer Charge kontrolliert wird, müssen Sie eine Rückverfolgungsangabengruppe dem Produkt zuweisen, das eine aktive Chargendimension hat.

-   Das Attribut, das die Inhaltsstoffebene angibt, muss als produktspezifisches Chargenattributs für das fertig gestellte Produkt definiert werden.

Sie können den tatsächlichen Wert der Wirksubstanz für eine Charge auf der Seite **Lagerchargenattribute** suchen und bearbeiten. 

-  Wählen Sie **Bestandmanagement** \> **Anfragen und Berichte** \> **Nachverfolgungsdimension** \> **Chargen** \> **Bestand-Chargen-Attribute**.

<a name="ingredient-types-and-how-they-interact-in-the-batch-balancing-process"></a>Inhaltsstofftypen und wie sie im Chargenausgleichprozess interagieren
---------------------------------------------------------------------

Eine Formelposition, die erstellt wird, kann eine dieser Inhaltsstofftypen haben:

-   None

-   Aktiv

-   Kompensation

-   Füller

Der Rest dieses Abschnitts enthält Beispiele, die zeigen, wie jeder Inhaltsstofftyp arbeitet. Die Beispiele basieren auf der folgenden Formel, die eine vollständige Chargengröße von 100 Litern hat.

| **Typ des Inhaltsstoffs** | **Artikelnummer** | **Formelzeilenmenge** | **Einheit** |
|---------------------|-----------------|---------------------------|----------|
| None                | H               | 20                        | Liter    |
| Aktiv              | b               | 30                        | Liter    |
| Kompensation        | k               | 10                        | Liter    |
| Füller              | u               | 40                        | Liter    |

### <a name="active"></a>Aktiv

Wenn einem Produkt, das ein Basisattribut hat, eine Formelposition hinzugefügt wird, wird es als *Wirksubstanz* der Formel. Chargenaufträge, die Formeln haben, die Wirksubstanzen enthalten, können für den Chargenausgleichprozess verwendet werden. Für jede Substanz in der Formel schätzt der Chargenausgleichprozess den Betrag, der erforderlich ist, um das Produkt herzustellen. Die Vorkalkulation von Beträgen basiert auf der Konzentration der Wirksubstanzen in der ausgewählten Charge.

**Beispiel**

Ihaltsstoff B hat Basisattribut X und Zielstufe von 30 und ist in einer Formel enthalten, die 30 Liter des Inhaltsstoffs B für alle 100 Liter des Produkts benötigt. Ein Chargenauftrag wird erstellt, der die Chargengröße von 100 Litern hat. Der Chargenauftrag wird gestartet und während dem gesamten Chargenausgleichprozesses wählt der Benutzer eine Charge des Inhaltsstoffs B aus, der ein Stärkeniveau von 35 hat. Da das Stärkeniveau von 35 höher ist als die Zielstufe 30, wird die ausgeglichene Menge des Inhaltsstoffs B verringert, indem das Verhältnis des Stärkewerts der Zielstufe der Charge verwendet, die von der vorkalkulierten Menge multipliziert wird. Die Berechnung der ausgeglichenen Menge sieht wie folgt aus:

(30 ÷ 35) × 30 Liter = 25,71 Liter

| **Artikelnummer** | **Typ des Inhaltsstoffs** | **Vorkalkulierte Menge** | **Saldomenge** | **Aktive Menge** | **Einheit** | **Basiswert** |
|-----------------|---------------------|------------------------|-----------------------|---------------------|----------|----------------|
| H               | None                | 20                     | 20                    |                     | Liter    |                |
| b               | Aktiv              | 30                     | 25.71                 | 9:00                | Liter    | 30,00          |
| k               | Kompensation        | 10                     | 14.72                 |                     | Liter    |                |
| u               | Füller              | 40                     | 39.57                 |                     | Liter    |                |

### <a name="none"></a>None

Wenn Sie den Chargenausgleichprozess anwenden, wenn der Inhaltsstofftyp ist **Kein** sind die vorkalkulierte Menge und die ausgeglichene Menge der Formelposition im Chargenauftrag identisch.

**Beispiel**

Substanz A ist einer Substanz im Typ **Keine** zugewiesen und hinzugefügt einer Formel für ein Produkt. Die Formel erfordert 10 Liter Inhaltsstoff von A für alle 100 Liter des Produkts. Erfordert ein Chargenauftrag 200 Liter, werden die vorkalkulierte Menge und die ausgeglichene Menge als 20 Liter berechnet.

### <a name="compensating"></a>Kompensation

Eine Kompensationssubstanz kann entweder die Auswirkungen der Wirksubstanz in einem Produkt ergänzen oder ausgleichen. Daher hängt die Menge einer Kompensationssubstanz, die verbraucht wird, von der Stärke des Produkts ab:

-   **Gegenüberliegende Auswirkungen** – Wenn der Betrag der Wirksubstanz höher ist als angenommen, müssen Sie weniger von der Kompensationssubstanz hinzufügen.

-   **Ergänzende Auswirkungen** – Wenn der Betrag der Wirksubstanz kleiner ist als angenommen, müssen Sie mehr von der Kompensationssubstanz hinzufügen.

Die Beziehung zwischen einer Wirksubstanz und einer ergänzenden Substanz wird auf der Seite **Kompensierendes Prinzip** eingerichtet.

Folgen Sie diesen Schritten, um die Beziehungen zwischen Substanzen einzurichten.

1.  Wählen Sie **Produktinformationsverwaltung** \> **Rechnungen und Material und Formeln** \> **Formeln** aus, öffnen Sie eine Formelposition, und wählen Sie dann **Substanzen**, um die Seite **Kompensierendes Prinzip** zu öffnen.

2.  Wählen Sie die Position aus, die ein kompensierendes Prinzip darstellt, und wählen Sie dann zum Ausgleichen Wirksubstanz aus.

>   Im kompensierenden Prinzip geben Sie auch einen positiven oder negativen kompensierenden Faktor ein, um anzugeben wie viel zu entschädigen ist und ob das Prinzip entgegensetzend oder ergänzend ist. Ein positiver Faktor zeigt eine ergänzenden Auswirkungen an, und ein negativer Faktor zeigt eine umgekehrte Auswirkung an.

**Beispiel**

Inhaltsstoff B ist eine Wirksubstanz, die Basisattribut X und eine Zielstufe von 30 an hat. Die Formel erfordert 30 Liter Substanz von A für alle 100 Liter des Produkts. Inhaltsstoff C ist eine Kompensationssubstanz, und die Menge 10 ist in der gleichen Formel aufgenommen. Ein kompensierender Faktor von 1.10 wird für das kompensierende Prinzip eingerichtet. Daher wird die ausgeglichene Menge der Kompensationssubstanz reduziert um den Unterschied der Differenz zwischen der Menge der Wirksubstanz und der vorkalkulierten Menge verringert, die mit 1,10 multipliziert wird.

Im Beispiel für den **Aktiven** Substanztyp wurde die ausgeglichene Menge der erforderlichen Wirksubstanz als 25,71 berechnet und die erforderliche vorkalkulierte Menge wurde als 30 berechnet. In diesem Fall wird die ausgeglichene Menge der Kompensationssubstanz so berechnet:

1.  Die Differenz zwischen der erwarteten und ausgeglichenen Menge wird bestimmt:

>   25.71 – 30 = –4.29

2.  Das Ergebnis wird dann mit dem Jahresbetrag multipliziert.

>   4.29 × 1.10 = –4.72

3.  Die vorkalkulierte kompensierte Menge wird durch – 4,72 verringert, um die ausgeglichene kompensierende Menge zu bestimmen:

>   10 – (–4.72) = 14.72

Da 1.10 ein positiver kompensierender Faktor ist, hat dieses kompensierende Prinzip eine zusätzliche Auswirkung. In diesem Fall ist die Wirksubstanz stärker als angenommen. Daher ist der Kompensationssubstanz erforderlich.

### <a name="filler"></a>Füller

*Füllsubstanz* ist eine neutrale Substanz, die verwendet wird, um die gewünschte Berechnung des Produkts zu geben. Änderungen an Füllermengen werden auf Grundlage der Schwankungen der Wirksubstanz und der Kompensationssubstanz berechnet, mit der die Standardmenge verglichen wird.

**Beispiel**

Sie haben ein Produkt formuliert, die Zutaten A, B, C und D für eine Formelgröße von 100 Litern enthält. Sie besitzen die ausgeglichene Menge aller Substanztypen außer der **Füller**-Substanztyp, der in einer Position verwendet wird.
Ausgeglichene Menge der Füllsubstanz wird als Unterschied zwischen der Chargengröße von 100 Litern und der Summe der Inhaltsstoffe A, B und C berechnet:

100 – (20 + 25.71 + 14.72) = 39.57

<a name="the-batch-balancing-process"></a>De Chargenausgleichprozess anzeigen
---------------------------

Der Chargenausgleichprozess wird durch den **Chargenausgleich** ausgeführt.
Wählen Sie **Kostenmanagement**, und dann \> **Chargenaufträge**, auf der Registerkarte **Prozess** wählen Sie **Chargenausgleich** aus. Chargenausgleich ist verfügbar für Chargenaufträge, die den Status **Gestartet** besitzen.

Im Allgemeinen kann Chargenausgleich in den Chargenaufträgen angewendet werden, wenn die Formel mindestens eine Formelposition mit Inhaltsstofftyp **Aktiv** hat. (Für die Ausnahme von dieser Regel, lesen Sie "Chargenaufträge, die nicht für Chargenausgleich gelten im Abschnitt weiter unten in diesem Thema).

Der Chargenausgleichprozess kann in zwei Unterprozesse unterteilt werden:

1.  Chargensubstanzausgleich

2.  Bestätigen und Formel eingeben

### <a name="balance-batch-ingredients"></a>Chargensubstanzausgleich

Im Chargenausgleichprozess wird der Betrag der Substanz zur Verwendung innerhalb einer Produktionscharge von der aus Wirksubstanzen in ausgewählten Produktchargen berechnet. Normalerweise kann die Berechnung abgeschlossen werden, wenn es eine vollständig Deckung aller Inhaltsstoffe gibt. Sie können nur einen Teil der Charge nicht ausgeglichen, für den der Chargenauftrag für die Produktion eingerichtet ist.

[!NOTE]
Sie können eine Berechnung nicht speichern und den Chargenausgleichprozess später abschließen. Wenn Sie die Detailebene **Chargenausgleich** schließen, müssen Sie die Berechnung wiederholen, damit der entsprechende Vorgang abgeschlossen werden kann.

### <a name="confirm-and-release-the-formula"></a>Bestätigen und Formel eingeben

Nachdem die Inhaltsstoffmengen berechnet wurden, können Sie die Formel bestätigen und freigeben. Der Freigabeprozess variiert, abhängig davon, ob die Produkte der Lagerortverwaltungsprozesse aktiviert werden:

-   Wenn ein Produkt für die Lagerortverwaltungsprozesse aktiviert ist, wird die Formelposition der Lagerorte anhand der Prinzipien für die Lagerortverwaltungsprozesse freigegeben. Die Formelposition wird anhand der produzierten Produktmengen freigegeben, die den ausgeglichenen Mengen entsprechen und für die Primärressource sowie für bestimmte Chargen freigegeben wird, die für die Wirksubstanzen ausgewählt werden.

> [!NOTE]
>   Formelpositionen können zum Lagerort nur als Teil des Chargenausgleichprozesses freigegeben werden. Obwohl es andere Optionen bei der gemeinsamen Nutzung von Material für Produktion in Lagerort gibt, können diese Optionen nicht für Formelpositionen verwendet werden.

-   Wenn das Produkt nicht für die Lagerortverwaltungsprozesse aktiviert ist, wird eine Produktionskommissionierliste für das Produkt erstellt, wenn Sie bestätigen und die Formel freigeben.

In einer einzelnen Formel können Sie Produkte kombinieren, die für die Lagerortverwaltungsprozesse aktiviert sind und Produkte, die nicht für die Lagerortverwaltung verarbeitet, aktiviert werden. Wenn die beiden Arten von Produkten in einer Formel enthalten sind, werden die Produkte, die für die Lagerortverwaltungsprozesse aktiviert sind, für den Lagerort freigegeben. Wenn das Produkt nicht für die Lagerortverwaltungsprozesse aktiviert ist, wird eine Produktionskommissionierliste für das Produkt erstellt, wenn Sie die Formel bestätigen und freigeben.

### <a name="batch-orders-that-arent-applicable-for-batch-balancing"></a>Chargenaufträge, die nicht für Chargenausgleich gelten

Es gibt eine Ausnahme zur Regel, dass Chargenausgleiche in den Chargenaufträgen angewendet werden, wenn die Formel mindestens eine Formelposition mit Substanztyp **Aktiv** hat.

Falls eine Formel eine Wirksubstanz für ein Produkt enthält, das für die Lagerortverwaltungsprozesse aktiviert ist, jedoch die Chargennummer unterhalb der Position in der Reservierungshierarchie ist, ist der Chargenauftrag für Chargenausgleich nicht verfügbar.

Ein Chargenauftrag, der nicht für Chargenausgleich anwendbar ist, durchläuft den normalen Prozesszyklus für Chargenaufträge.

