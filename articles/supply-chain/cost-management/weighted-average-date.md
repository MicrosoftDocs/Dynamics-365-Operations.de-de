---
title: Gewichteter Durchschnitt (Datum) enthält physischen Wert und Markierung
description: Das Datum für gewichteten Durchschnitt ist ein auf dem Prinzip des gewichteten Durchschnitts basierendes Lagermodell. Dabei werden Lagerabgänge mit dem durchschnittlichen Wert der Artikel bewertet, die an den einzelnen Tagen in der Lagerabschlussperiode im Lager entgegengenommen werden.
author: JennySong-SH
ms.date: 03/04/2022
ms.topic: article
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 28991
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1497cb08f4cc5a455c832b9bf125c309cd90aa3d
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2022
ms.locfileid: "8672121"
---
# <a name="weighted-average-date-with-include-physical-value-and-marking"></a>Gewichteter Durchschnitt (Datum) enthält physischen Wert und Markierung

[!include [banner](../includes/banner.md)]

*Gewichteter Durchschnitt (Datum)* ist ein Bestandsmodell, das auf einem Durchschnitt basiert, der mithilfe der Multiplikation jeder Komponente (Artikel-Transaktion) mit einem Faktor (Einstandspreis) berechnet wird, der ihre Bedeutung (Menge) an jedem Tag in der Periode widerspiegelt. Anders ausgedrückt weist dieses Bestandsmodell die Kosten für Abgangsbuchungen auf der Grundlage des Mittelwerts aller täglich eingehenden Bestände zuzüglich aller Lagerbestände vom Vortag zu.

Wenn Sie einen Lagerabschluss mit dem Bestandsmodell für den gewichteten Durchschnitt (Datum) ausführen, gibt es zwei Möglichkeiten, eine Abrechnung zu erstellen. Normalerweise werden alle Eingänge mit einem virtuellen Abgang verrechnet, der die gesamte eingegangene Menge und den Wert enthält. Für diesen virtuellen Abgang ist auch ein entsprechender virtueller Zugang vorhanden, von dem aus die Abgänge ausgeglichen werden. Auf diese Weise erhalten alle Abgänge die gleichen Durchschnittskosten jeden Tag. Der virtuelle Abgang und der virtuelle Zugang können als virtueller Übertrag betrachtet werden. Dieser virtuelle Übertrag wird als *Lagerabschlussübertrag mit gewichtetem Durchschnitt* bezeichnet. Daher ist diese Abrechnungsmethode als *Gewichteter Durchschnitt zusammengefasste Abrechnung* bekannt. Ist lediglich ein Zugang vorhanden, können alle Abgänge anhand dieses Zugangs ausgeglichen werden, und es wird kein virtueller Übertrag erstellt. Diese Abrechnungsmethode wird als *direkte Abrechnung* bezeichnet. Jeder Bestand, der nach Lagerabschluss vorhanden ist, wird mit dem gewichteten Durchschnitt des letzten Tags der Vorperiode bewertet und in der nächsten Periode in die Berechnung des gewichteten Durchschnitts (Datum) einbezogen.

Sie können das Prinzip des gewichteten Durchschnitts (Datum) außer Kraft setzen, indem Sie Transaktionen im Bestand so markieren, dass ein bestimmter Artikelzugang mit einem bestimmten Abgang verrechnet wird. Ein periodischer Lagerabschluss ist erforderlich, wenn Sie das Bestandsmodell des gewichteten Durchschnitts (Datum) verwenden, um Abrechnungen zu erstellen und den Wert von Abgängen nach dem Prinzip des gewichteten Durchschnitts (Datum) anzupassen. Bis Sie den Lagerabschluss ausführen, werden Abgangstransaktionen zum laufenden Durchschnitt bewertet, wenn die physischen und finanziellen Aktualisierungen erfolgt sind. Sofern Sie nicht die Markierung verwenden, wird der laufende Durchschnitt berechnet, wenn die physische oder finanzielle Aktualisierung ausgeführt wird.

Die Lagernachkalkulationsmethode für den gewichteten Durchschnitt (Datum) wird nach folgender Formel jeden Tag berechnet:

*Kosten* = \[(*Q*<sub>*b*</sub> × *P*<sub>*b*</sub>) + &#x2211;<sub>*n*</sub>(*Q*<sub>*n*</sub> × *P*<sub>*n*</sub>)\] ÷ (*Q*<sub>*b*</sub> + &#x2211;<sub>*n*</sub>*Q*<sub>*n*</sub>)

- *Q* = Menge der Transaktion
- *P* = Preis der Transaktion

Mit anderen Worten, die gewichteten Durchschnittskosten sind gleich der Anfangsmenge mal dem Anfangspreis plus der Summe jeder Zugangsmenge mal ihrem Zugangspreis, alles dividiert durch die Anfangsmenge plus der Summe der Zugangsmengen.

Während des Lagerabschlusses wird die Berechnung während der Abschlussperiode täglich ausgeführt.

> [!NOTE]
> Weitere Informationen zu Ausgleichen finden Sie unter [Lagerabschluss](inventory-close.md).

In den folgenden Beispielen werden die Auswirkungen der Verwendung des gewichteten Durchschnitts (Datum) anhand von fünf Konfigurationen gezeigt:

- Direkter Ausgleich für das Datum des gewichteten Durchschnitts, wenn die Option **Physischen Wert einbeziehen** nicht verwendet wird
- Zusammengefasster Ausgleich für das Datum des gewichteten Durchschnitts, wenn die Option **Physischen Wert einbeziehen** nicht verwendet wird
- Direkter Ausgleich für das Datum des gewichteten Durchschnitts, wenn die Option **Physischen Wert einbeziehen** verwendet wird
- Zusammengefasster Ausgleich für das Datum des gewichteten Durchschnitts, wenn die Option **Physischen Wert einbeziehen** verwendet wird
- Datum des gewichteten Durchschnitts, wenn Markierung verwendet wird

## <a name="weighted-average-date-direct-settlement-when-the-include-physical-value-option-isnt-used"></a>Direkter Ausgleich für das Datum des gewichteten Durchschnitts, wenn die Option Physischen Wert einbeziehen nicht verwendet wird

Das Prinzip der direkten Abrechnung erstellt Abrechnungen direkt zwischen Zu- und Abgängen, ohne zusätzliche Transaktionen im Bestand zu erstellen. Das System verwendet dieses Prinzip der direkten Abrechnung in den folgenden Situationen:

- Ein Beleg und eine oder mehrere Ausgaben wurden in der Periode gebucht.
- In der Periode wurden ausschließlich Abgänge gebucht, und der Lagerbestand enthält verfügbare Artikel aus einem früheren Abschluss.

In diesem Beispiel ist das Kontrollkästchen **Physischen Wert einbeziehen** auf der Seite **Artikelmodellgruppe** für das zugelassene Produkt deaktiviert. Das folgende Diagramm zeigt diese Transaktionen an:

**Tag 1:**

- 1a. Physischer Lagerzugang für die Menge "10" zu jeweils EUR 10,00 (Kosten).
- 1b. Wertmäßiger Lagerzugang für die Menge "10" zu jeweils EUR 10,00 (Kosten).
- 2a. Physischer Lagerzugang für die Menge "10" zu jeweils EUR 20,00 (Kosten).
- 3a. Physischer Bestandsabgang für eine Menge von 1 zu einem Einstandspreis von USD 10,00 (laufender Durchschnitt der finanziell gebuchten Transaktionen).
- 3b. Bestandsfinanzausgang für eine Menge von 1 zu einem Einstandspreis von USD 10,00 (laufender Durchschnitt der finanziell gebuchten Transaktionen).

**Tag 2:**

- 4a. Physischer Lagerzugang für die Menge "1" zu jeweils EUR 25,00 (Kosten).
- 5a. Physischer Lagerzugang für die Menge "1" zu jeweils EUR 30,00 (Kosten).
- 5b. Wertmäßiger Lagerzugang für die Menge "1" zu jeweils EUR 30,00 (Kosten).
- 6a. Finanzielle Bestandsausgabe für eine Menge von 1 zu einer Kalkulation von jeweils USD 20,00 (laufender Durchschnitt der finanziell gebuchten Transaktionen).

**Tag 3:**

- 7\. Lagerabschluss wird vorgenommen. Basierend auf der Methode des gewichteten Durchschnitts (Datum) verwendet das System die Methode der direkten Abrechnung für 30. Dezember (30.12.), da nur ein Zugang am 30.12. wertmäßig aktualisiert wird. In diesem Beispiel wird eine Abrechnung zwischen Transaktionen 1b und 3b erstellt. Eine Anpassung von USD 10,00 wird vorgenommen, um den Wert von Transaktion 3b auf 20,00 zu erhöhen. Am 31. Dezember (31.12.) wird keine Anpassung oder Abrechnung vorgenommen, da es am 31.12. keine wertmäßig aktualisierten Abgänge gibt.

Das folgende Diagramm zeigt diese Reihe von Transaktionen und die Auswirkungen der Verwendung des Bestandsmodells des gewichteten Durchschnitts und des Prinzips der direkten Abrechnung ohne die Option **Physischen Wert einbeziehen**.

![Direkter Ausgleich mit Datum für den gewichteten Durchschnitt und ohne die Option „Physischen Wert einbeziehen“.](media/weighted-average-date-direct-settlement-without-include-physical-value.png)

**Diagrammschlüssel:**

- Lagerbuchungen sind durch vertikale Pfeile dargestellt.
- Physische Transaktionen werden durch kürzere hellgraue Pfeile dargestellt.
- Finanzielle Transaktionen werden durch längere schwarze Pfeile dargestellt.
- Eingänge in den Bestand werden durch vertikale Pfeile oberhalb der Achse dargestellt.
- Ausgaben, die nicht im Bestand sind, werden durch vertikale Pfeile unterhalb der Achse dargestellt.
- Jede neue Zugangs- oder Abgangsbuchung wird mit einer neuen Beschriftung versehen.
- Jeder vertikale Pfeil ist mit einer Sequenzkennung (beispielsweise *1a*) versehen. Mit dieser Kennung wird die Reihenfolge der Lagerbuchungen auf der Zeitachse angegeben.
- Datumsangaben werden durch dünne schwarze vertikale Linien getrennt. Die Datumsangaben sind am unteren Rand des Diagramms vermerkt.
- Lagerabschlüsse werden durch rote vertikale gestrichelte Linien dargestellt.
- Ein durch einen Lagerabschluss vorgenommener Ausgleich ist durch rote diagonale gestrichelte Pfeile dargestellt, die von einem Zugang zu einem Abgang verlaufen.

## <a name="weighted-average-date-summarized-settlement-when-the-include-physical-value-option-isnt-used"></a>Zusammengefasster Ausgleich für das Datum des gewichteten Durchschnitts, wenn die Option "Physischen Wert einbeziehen" nicht verwendet wird

Wenn es mehrere Eingänge in einer Periode gibt, verwendet der gewichtete Durchschnitt (Datum) das Prinzip der zusammengefassten Abrechnung, bei der alle Eingänge an einem einzelnen Tag in einer Transaktion namens *Lagerabschluss mit gewichtetem Durchschnitt* zusammengefasst werden. Alle Eingänge für den Tag werden mit dem Abgang neu erstellten Bestandstransaktion verrechnet. Alle Abgänge für den Tag werden mit dem Eingang der neuen Transaktion für den Bestand verrechnet. Wenn nach dem Inventarabschluss noch ein Lagerbestand vorhanden ist, wird dieser in die Eingangstransaktion der gewichteten durchschnittlichen Inventarabschluss-Transaktionen aufgenommen.

Das folgende Diagramm zeigt diese Transaktionen an:

**Tag 1:**

- 1a. Physischer Lagerzugang für die Menge "1" zu jeweils EUR 10,00 (Kosten).
- 1b. Wertmäßiger Lagerzugang für die Menge "1" zu jeweils EUR 10,00 (Kosten).
- 2a. Physischer Lagerzugang für die Menge "1" zu jeweils EUR 20,00 (Kosten).
- 2b. Wertmäßiger Lagerzugang für die Menge "1" zu jeweils EUR 22,00 (Kosten).
- 3a. Physischer Bestandsabgang für eine Menge von 1 zu einem Einstandspreis von USD 16,00 (laufender Durchschnitt der finanziell gebuchten Transaktionen).
- 3b. Bestandsfinanzausgang für eine Menge von 1 zu einem Einstandspreis von USD 16,00 (laufender Durchschnitt der finanziell gebuchten Transaktionen).

**Tag 2:**

- 4a. Physischer Lagerzugang für die Menge "1" zu jeweils EUR 25,00 (Kosten).
- 5a. Physischer Lagerzugang für die Menge "1" zu jeweils EUR 30,00 (Kosten).
- 5b. Wertmäßiger Lagerzugang für die Menge "1" zu jeweils EUR 30,00 (Kosten).
- 6a. Physischer Bestandsabgang für eine Menge von 1 zu einem Einstandspreis von USD 23,00 (laufender Durchschnitt der finanziell gebuchten Transaktionen).

**Tag 3:**

- 7\. Lagerabschluss wird vorgenommen.
- 7a. Der gewichtete durchschnittliche Finanzausgang der Transaktion zum Abschluss des Bestands wird erstellt, um die Abrechnungen aller finanziellen Eingänge des Bestands zu summieren.

    - Transaktion 1b wird für eine Menge von 1 mit einem Ausgleichsbetrag von USD 10,00 abgerechnet.
    - Transaktion 2b wird für eine Menge von 1 mit einem Abrechnungsbetrag von USD 22,00 abgerechnet.
    - Transaktion 7a wird für eine Menge von 2 mit einem Abrechnungsbetrag von USD 32,00 erstellt. Diese Transaktion gleicht die Summe der zwei Eingangstransaktionen aus, die in der Periode wertmäßig aktualisiert werden.

- 7b. Der gewichtete durchschnittliche finanzielle Eingang der Transaktion zum Lagerabschluss wird als Ausgleich für die finanziell gebuchten Ausgaben erstellt.

    - Die Transaktion 3b wird für eine Menge von 1 mit einem Abrechnungsbetrag von USD 16,00 abgerechnet. Diese Transaktion wird nicht angepasst, da es sich um den gewichteten Durchschnitt der am 1. Dezember (1.12.) gebuchten Transaktionen handelt.
    - Transaktion 7b wird für eine Menge von 2 mit einem Finanzbetrag von USD 32,00 und einem Abrechnungsbetrag von USD 16,00 erstellt, um Transaktion 3b auszugleichen. Diese Transaktion gleicht die Summe der einen Emissionstransaktion aus, die in der Periode finanziell verbucht wird. Die Transaktion bleibt offen, da noch eine vorhanden ist.

Das folgende Diagramm zeigt eine Reihe von Transaktionen und die Auswirkungen der Verwendung des Lagermodells mit gewichtetem Durchschnitt und des Prinzips des zusammengefassten Ausgleichs, aber ohne Verwendung der Option **Physischen Wert einbeziehen**.

![Zusammengefasster Ausgleich mit Datum für den gewichteten Durchschnitt und ohne die Option „Physischen Wert einbeziehen“.](media/weighted-average-date-summarized-settlement-without-include-physical-value.png)

**Diagrammschlüssel:**

- Lagerbuchungen sind durch vertikale Pfeile dargestellt.
- Physische Transaktionen werden durch kürzere hellgraue Pfeile dargestellt.
- Finanzielle Transaktionen werden durch längere schwarze Pfeile dargestellt.
- Eingänge in den Bestand werden durch vertikale Pfeile oberhalb der Achse dargestellt.
- Ausgaben, die nicht im Bestand sind, werden durch vertikale Pfeile unterhalb der Achse dargestellt.
- Jede neue Zugangs- oder Abgangsbuchung wird mit einer neuen Beschriftung versehen.
- Jeder vertikale Pfeil ist mit einer Sequenzkennung (beispielsweise *1a*) versehen. Mit dieser Kennung wird die Reihenfolge der Lagerbuchungen auf der Zeitachse angegeben.
- Datumsangaben werden durch dünne schwarze vertikale Linien getrennt. Die Datumsangaben sind am unteren Rand des Diagramms vermerkt.
- Lagerabschlüsse werden durch rote vertikale gestrichelte Linien dargestellt.
- Ein durch einen Lagerabschluss vorgenommener Ausgleich ist durch rote diagonale gestrichelte Pfeile dargestellt, die von einem Zugang zu einem Abgang verlaufen.

## <a name="weighted-average-date-direct-settlement-when-the-include-physical-value-option-is-used"></a>Direkter Ausgleich für das Datum des gewichteten Durchschnitts, wenn die Option Physischen Wert einbeziehen verwendet wird

In der aktuellen Version des Produkts funktioniert die Option **Physischen Wert einbeziehen** mit dem Bestandsmodell für den gewichteten Durchschnitt (Datum) anders als in früheren Versionen. Wenn Sie das Kontrollkästchen **Physischen Wert einbeziehen** für einen Artikel auf der Seite **Artikelmodellgruppe** aktivieren, verwendet das System physisch aktualisierte Zugänge, wenn es den vorkalkulierten Artikeleinstandspreis berechnet, oder den laufenden Durchschnitt. Die Buchung der Abgänge während der Periode erfolgt auf Basis dieses vorkalkulierten Einstandspreises. Beim Lagerabschluss werden nur wertmäßig aktualisierte Zugänge in der Berechnung des gewichteten Durchschnitts berücksichtigt.

Das folgende Diagramm zeigt diese Transaktionen an:

**Tag 1:**

- 1a. Physischer Lagerzugang für die Menge "10" zu jeweils EUR 10,00 (Kosten).
- 1b. Wertmäßiger Lagerzugang für die Menge "10" zu jeweils EUR 10,00 (Kosten).
- 2a. Physischer Lagerzugang für die Menge "10" zu jeweils EUR 20,00 (Kosten).
- 3a. Inventarabgang für eine Menge von 1 zu einem Einstandspreis von USD 15,00 (laufender Durchschnitt der physisch und finanziell gebuchten Transaktionen).
- 3b. Finanzieller Bestandsabgang für eine Menge von 1 zu einem Einstandspreis von USD 15,00 (laufender Durchschnitt der physisch und finanziell gebuchten Transaktionen).

**Tag 2:**

- 4a. Physischer Lagerzugang für die Menge "1" zu jeweils EUR 25,00 (Kosten).
- 5a. Physischer Lagerzugang für die Menge "1" zu jeweils EUR 30,00 (Kosten).
- 5b. Wertmäßiger Lagerzugang für die Menge "1" zu jeweils EUR 30,00 (Kosten).
- 6a. Physischer Bestandsabgang für eine Menge von 1 zu Kosten von jeweils USD 21,25 (laufender Durchschnitt der physisch und finanziell gebuchten Transaktionen).

**Tag 3:**

- 7\. Lagerabschluss wird vorgenommen. Basierend auf der Methode des gewichteten Durchschnitts (Datum) verwendet das System die Methode der direkten Abrechnung für 30. Dezember (30.12.), da nur ein Zugang am 30.12. wertmäßig aktualisiert wird. In diesem Beispiel wird eine Abrechnung zwischen Transaktionen 1b und 3b erstellt. Der Abgang zum 30.12. wird nicht angepasst. Außerdem wird am 31. Dezember (31.12.) keine Anpassung oder Abrechnung vorgenommen, da es am 31.12. keine wertmäßig aktualisierten Abgänge gibt.

Das folgende Diagramm zeigt diese Reihe von Transaktionen und die Auswirkungen der Verwendung des Bestandsmodells des gewichteten Durchschnitts und des Prinzips der direkten Abrechnung mit der Option **Physischen Wert einbeziehen**.

![Direkter Ausgleich mit gewichtetem Durchschnitt mit „Physischen Wert einbeziehen“.](media/weighted-average-date-direct-settlement-with-include-physical-value.png)

**Diagrammschlüssel:**

- Lagerbuchungen sind durch vertikale Pfeile dargestellt.
- Physische Transaktionen werden durch kürzere hellgraue Pfeile dargestellt.
- Finanzielle Transaktionen werden durch längere schwarze Pfeile dargestellt.
- Eingänge in den Bestand werden durch vertikale Pfeile oberhalb der Achse dargestellt.
- Ausgaben, die nicht im Bestand sind, werden durch vertikale Pfeile unterhalb der Achse dargestellt.
- Jede neue Zugangs- oder Abgangsbuchung wird mit einer neuen Beschriftung versehen.
- Jeder vertikale Pfeil ist mit einer Sequenzkennung (beispielsweise *1a*) versehen. Mit dieser Kennung wird die Reihenfolge der Lagerbuchungen auf der Zeitachse angegeben.
- Datumsangaben werden durch dünne schwarze vertikale Linien getrennt. Die Datumsangaben sind am unteren Rand des Diagramms vermerkt.
- Lagerabschlüsse werden durch rote vertikale gestrichelte Linien dargestellt.
- Ein durch einen Lagerabschluss vorgenommener Ausgleich ist durch rote diagonale gestrichelte Pfeile dargestellt, die von einem Zugang zu einem Abgang verlaufen.

## <a name="weighted-average-date-summarized-settlement-when-the-include-physical-value-option-is-used"></a>Zusammengefasster Ausgleich für das Datum des gewichteten Durchschnitts, wenn die Option Physischen Wert einbeziehen verwendet wird

In der aktuellen Version des Produkts funktioniert die Option **Physischen Wert einbeziehen** mit dem gewichteten Durchschnitt anders als in früheren Versionen. Wenn Sie das Kontrollkästchen **Physischen Wert einbeziehen** für einen Artikel auf der Seite **Artikelmodellgruppe** aktivieren, verwendet das System physisch aktualisierte Zugänge, wenn es den vorkalkulierten Einstandspreis berechnet, oder den laufenden Durchschnitt. Die Buchung der Abgänge während der Periode erfolgt auf Basis dieses vorkalkulierten Einstandspreises. Beim Lagerabschluss werden nur wertmäßig aktualisierte Zugänge in der Berechnung des gewichteten Durchschnitts berücksichtigt. Wenn Sie das Bestandsmodell für den gewichteten Durchschnitt verwenden, empfiehlt es sich, einen monatlichen Lagerabschluss durchzuführen. In diesem Beispiel für einen zusammengefassten Ausgleich mit gewichtetem Durchschnitt (Datum) ist das Bestandsmodell so markiert, dass der physische Wert einbezogen wird.

Das folgende Diagramm zeigt diese Transaktionen an:

**Tag 1:**

- 1a. Physischer Lagerzugang für die Menge "1" zu jeweils EUR 10,00 (Kosten).
- 1b. Wertmäßiger Lagerzugang für die Menge "1" zu jeweils EUR 10,00 (Kosten).
- 2a. Physischer Lagerzugang für die Menge "1" zu jeweils EUR 20,00 (Kosten).
- 2b. Wertmäßiger Lagerzugang für die Menge "1" zu jeweils EUR 22,00 (Kosten).
- 3a. Inventarabgang für eine Menge von 1 zu einem Einstandspreis von USD 16,00 (laufender Durchschnitt der physisch und finanziell gebuchten Transaktionen).
- 3b. Finanzieller Bestandsabgang für eine Menge von 1 zu einem Einstandspreis von USD 16,00 (laufender Durchschnitt der physisch und finanziell gebuchten Transaktionen).

**Tag 2:**

- 4a. Physischer Lagerzugang für die Menge "1" zu jeweils EUR 25,00 (Kosten).
- 5a. Physischer Lagerzugang für die Menge "1" zu jeweils EUR 30,00 (Kosten).
- 5b. Wertmäßiger Lagerzugang für die Menge "1" zu jeweils EUR 30,00 (Kosten).
- 6a. Physischer Bestandsabgang für eine Menge von 1 zu einem Einstandspreis von USD 23,67 (laufender Durchschnitt der physisch und finanziell gebuchten Transaktionen).

**Tag 3:**

- 7\. Lagerabschluss wird vorgenommen.
- 7a. Der gewichtete durchschnittliche Finanzausgang der Transaktion zum Abschluss des Bestands wird erstellt, um die Abrechnungen aller finanziellen Eingänge des Bestands zu summieren.

    - Transaktion 1b wird für eine Menge von 1 mit einem Ausgleichsbetrag von USD 10,00 abgerechnet.
    - Transaktion 2b wird für eine Menge von 1 mit einem Abrechnungsbetrag von USD 22,00 abgerechnet.
    - Transaktion 7a wird für eine Menge von 2 mit einem Abrechnungsbetrag von USD 32,00 erstellt. Diese Transaktion gleicht die Summe der zwei Eingangstransaktionen aus, die in der Periode wertmäßig aktualisiert werden.

- 7b. Der gewichtete durchschnittliche finanzielle Eingang der Transaktion zum Lagerabschluss wird als Ausgleich für die finanziell gebuchten Ausgaben erstellt.

    - Die Transaktion 3b wird für eine Menge von 1 mit einem Abrechnungsbetrag von USD 16,00 abgerechnet. Diese Transaktion wird nicht angepasst, da es sich um den gewichteten Durchschnitt der am 1. Dezember (1.12.) gebuchten Transaktionen handelt.
    - Transaktion 7b wird für eine Menge von 2 mit einem Finanzbetrag von USD 32,00 und einem Abrechnungsbetrag von USD 16,00 erstellt, um Transaktion 3b auszugleichen. Diese Transaktion gleicht die Summe der einen Emissionstransaktion aus, die in der Periode finanziell verbucht wird. Die Transaktion bleibt offen, da noch eine vorhanden ist.

Das folgende Diagramm zeigt diese Reihe von Transaktionen und die Auswirkungen der Verwendung des Bestandsmodells des gewichteten Durchschnitts und des Prinzips der zusammengefassten Abrechnung ohne die Option **Physischen Wert einbeziehen**.

![Zusammengefasster Ausgleich mit gewichtetem Durchschnitt und der Option „Physischen Wert einbeziehen“.](media/weighted-average-date-summarized-settlement-with-include-physical-value.png)

**Diagrammschlüssel:**

- Lagerbuchungen sind durch vertikale Pfeile dargestellt.
- Physische Transaktionen werden durch kürzere hellgraue Pfeile dargestellt.
- Finanzielle Transaktionen werden durch längere schwarze Pfeile dargestellt.
- Eingänge in den Bestand werden durch vertikale Pfeile oberhalb der Achse dargestellt.
- Ausgaben, die nicht im Bestand sind, werden durch vertikale Pfeile unterhalb der Achse dargestellt.
- Jede neue Zugangs- oder Abgangsbuchung wird mit einer neuen Beschriftung versehen.
- Jeder vertikale Pfeil ist mit einer Sequenzkennung (beispielsweise *1a*) versehen. Mit dieser Kennung wird die Reihenfolge der Lagerbuchungen auf der Zeitachse angegeben.
- Datumsangaben werden durch dünne schwarze vertikale Linien getrennt. Die Datumsangaben sind am unteren Rand des Diagramms vermerkt.
- Lagerabschlüsse werden durch rote vertikale gestrichelte Linien dargestellt.
- Ein durch einen Lagerabschluss vorgenommener Ausgleich ist durch rote diagonale gestrichelte Pfeile dargestellt, die von einem Zugang zu einem Abgang verlaufen.

## <a name="weighted-average-date-when-marking-is-used"></a>Datum des gewichteten Durchschnitts, wenn Markierung verwendet wird

Der Begriff "Markierung" bezeichnet ein Verfahren zum Verknüpfen (oder Markieren) einer Abgangsbuchung mit einer Zugangsbuchung. Eine Markierung kann entweder vor oder nach Ausführung der Buchung erfolgen. Durch die Verwendung einer Markierung lassen sich bei der Ausführung der Buchung oder des Lagerabschlusses die exakten Kosten des Lagers ermitteln.

Beispiel: In der Kundendienstabteilung wurde der Eilauftrag eines wichtigen Debitors angenommen. Da es sich um eine Eilbestellung handelt, müssen Sie für diesen Artikel mehr bezahlen, um den Wunsch Ihres Kunden zu erfüllen. Deshalb müssen Sie sicher sein, dass bei dieser Auftragsrechnung die Kosten für diesen Lagerartikel in der Gewinnspanne bzw. im Wareneinsatz (COGS/cost of goods sold) berücksichtigt werden.

Bei der Buchung der Bestellung erhält das Lager einen Zugang in Höhe von EUR 120,00 (Kosten). Wenn das Auftragsdokument für die Bestellung markiert wird, bevor der Lieferschein oder die Rechnung gebucht wird, beträgt der COGS USD 120,00 und nicht die aktuellen laufenden Durchschnittskosten für den Artikel. Wenn die Markierung vorgenommen wird, nachdem der Lieferschein oder die Rechnung des Auftrags gebucht wird, erfolgt die Buchung des Wareneinsatzes zum laufenden Durchschnittseinstandspreis.

Die Markierung der beiden Buchungen kann noch bis zur Ausführung des Lagerabschlusses nachgeholt werden.

Wenn eine Zugangsbuchung für eine Abgangsbuchung markiert wird, wird die Bewertungsmethode, die für die Artikelmodellgruppe des Artikels ausgewählt ist, nicht berücksichtigt, und das System rechnet diese Transaktionen miteinander ab.

Sie können vor der Ausführung der Buchung eine Abgangsbuchung für einen Zugang markieren. Dieses Markieren kann von einer Auftragsposition auf der Seite **Auftragsdetails** aus erfolgen. Die offenen Quittungstransaktionen werden auf der Seite **Markierung** angezeigt.

Sie können auch nach der Buchung der Transaktion eine Abgangsbuchung für einen Zugang markieren. Sie können eine Abgangsbuchung für eine offene Zugangsbuchung für einen gelagerten Artikel aus einer gebuchten Lagerregulierungserfassung abgleichen oder markieren.

Das folgende Diagramm zeigt diese Transaktionen an:

**Tag 1:**

- 1a. Physischer Lagerzugang für die Menge "1" zu jeweils EUR 10,00 (Kosten).
- 1b. Wertmäßiger Lagerzugang für die Menge "1" zu jeweils EUR 10,00 (Kosten).
- 2a. Physischer Lagerzugang für die Menge "1" zu jeweils EUR 20,00 (Kosten).
- 2b. Wertmäßiger Lagerzugang für die Menge "1" zu jeweils EUR 22,00 (Kosten).
- 3a. Physischer Bestandsabgang für eine Menge von 1 zu einem Einstandspreis von USD 16,00 (laufender Durchschnitt der finanziell gebuchten Transaktionen).
- 3b. Bestandsfinanzausgang für eine Menge von 1 zu einem Einstandspreis von USD 16,00 (laufender Durchschnitt der finanziell gebuchten Transaktionen).
- 3c. Der wertmäßige Bestandsabgang für Transaktion 3b wird mit dem wertmäßigen Bestandsabgang für Transaktion 2b markiert.

**Tag 2:**

- 4a. Physischer Lagerzugang für die Menge "1" zu jeweils EUR 25,00 (Kosten).
- 5a. Physischer Lagerzugang für die Menge "1" zu jeweils EUR 30,00 (Kosten).
- 5b. Wertmäßiger Lagerzugang für die Menge "1" zu jeweils EUR 30,00 (Kosten).
- 6a. Physischer Bestandsabgang für eine Menge von 1 zu einem Einstandspreis von USD 23,00 (laufender Durchschnitt der finanziell gebuchten Transaktionen).

**Tag 3:**

- 7\. Lagerabschluss wird vorgenommen. Beim Markierungsprinzip nach der Methode des gewichteten Durchschnitts werden die markierten Transaktionen miteinander verrechnet. In diesem Beispiel wird Transaktion 3b gegen Transaktion 2b abgerechnet und eine Korrektur von 6,00 USD auf Transaktion 3b gebucht, um den Wert auf 22,00 USD zu bringen. In diesem Beispiel werden keine weiteren Abrechnungen vorgenommen, da der Abschluss nur Abrechnungen für finanziell aktualisierte Transaktionen erstellt.

Das folgende Diagramm zeigt diese Reihe von Transaktionen und die Auswirkungen der Verwendung des Lagermodells für den gewichteten Durchschnitt mit Markierung.

![Gewichteter Durchschnitt mit Markierung.](media/weighted-average-date-with-marking.png)

**Diagrammschlüssel:**

- Lagerbuchungen sind durch vertikale Pfeile dargestellt.
- Physische Transaktionen werden durch kürzere hellgraue Pfeile dargestellt.
- Finanzielle Transaktionen werden durch längere schwarze Pfeile dargestellt.
- Eingänge in den Bestand werden durch vertikale Pfeile oberhalb der Achse dargestellt.
- Ausgaben, die nicht im Bestand sind, werden durch vertikale Pfeile unterhalb der Achse dargestellt.
- Jede neue Zugangs- oder Abgangsbuchung wird mit einer neuen Beschriftung versehen.
- Jeder vertikale Pfeil ist mit einer Sequenzkennung (beispielsweise *1a*) versehen. Mit dieser Kennung wird die Reihenfolge der Lagerbuchungen auf der Zeitachse angegeben.
- Datumsangaben werden durch dünne schwarze vertikale Linien getrennt. Die Datumsangaben sind am unteren Rand des Diagramms vermerkt.
- Lagerabschlüsse werden durch rote vertikale gestrichelte Linien dargestellt.
- Ein durch einen Lagerabschluss vorgenommener Ausgleich ist durch rote diagonale gestrichelte Pfeile dargestellt, die von einem Zugang zu einem Abgang verlaufen.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
