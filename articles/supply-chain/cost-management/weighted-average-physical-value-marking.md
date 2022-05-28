---
title: Gewichteter Durchschnitt mit physischem Wert und Markierung
description: Beim gewichteten Durchschnitt handelt es sich um ein auf dem Prinzip des gewichteten Durchschnitts basierendes Lagermodell. Für dieses Modell werden Abgänge aus dem Bestand mit dem Durchschnittswert der Artikel, die im Rahmen der Lagerabschlussperiode in den Bestand eingehen, sowie des gesamten verfügbaren Bestands der vorangegangenen Periode bewertet.
author: JennySong-SH
ms.date: 02/21/2022
ms.topic: article
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 65501
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 41c80dcdc08432bb68478827c8763735e644aa4a
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2022
ms.locfileid: "8675262"
---
# <a name="weighted-average-with-physical-value-and-marking"></a>Gewichteter Durchschnitt mit physischem Wert und Markierung

[!include [banner](../includes/banner.md)]

Der gewichtete Durchschnitt ist ein Bestandsmodell, das auf einem Durchschnitt basiert, der sich aus der Multiplikation jeder Komponente (Element-Transaktion) mit einem Faktor (Einstandspreis) ergibt, der ihre Bedeutung (Menge) widerspiegelt. Eine andere Möglichkeit, dies zu sagen, ist, dass der gewichtete Durchschnitt ein Bestandsmodell ist, das die Kosten für Ausgabetransaktionen auf der Grundlage des Mittelwerts aller während der Periode eingegangenen Bestände zuzüglich aller Lagerbestände aus der Vorperiode zuweist.

Wenn Sie einen Bestandsabschluss nach dem Modell des gewichteten Durchschnittsbestands ausführen, gibt es zwei Möglichkeiten, eine Abrechnung zu erstellen. Normalerweise werden alle Eingänge mit einer virtuellen Ausgabe verrechnet, die die gesamte eingegangene Menge und den Wert enthält. Für diesen virtuellen Abgang ist auch ein entsprechender virtueller Zugang vorhanden, von dem aus die Abgänge ausgeglichen werden. Auf diese Weise erhalten alle Abgänge die gleichen Durchschnittskosten. Der virtuelle Warenausgang und -eingang ist als virtuelle Übertragung zu sehen, die *Gewichteter durchschnittlicher Bestand Abschlussübertragung* genannt wird. Diese Abrechnungsmethode wird als *Gewichteter Durchschnitt zusammengefasste Abrechnung* bezeichnet. Ist lediglich ein Zugang vorhanden, können alle Abgänge anhand dieses Zugangs ausgeglichen werden, und es wird kein virtueller Übertrag erstellt. Diese Abrechnungsmethode wird als *direkte Abrechnung* bezeichnet. Jeder Bestand, der nach dem Abschluss der Inventur vorhanden ist, wird mit dem gewichteten Durchschnitt der Vorperiode bewertet und in der nächsten Periode in die Berechnung des gewichteten Durchschnitts einbezogen.

Sie können das Prinzip des gewichteten Durchschnitts außer Kraft setzen, indem Sie Transaktionen im Bestand so markieren, dass ein bestimmter Wareneingang mit einem bestimmten Warenausgang verrechnet wird. Ein periodischer Bestandsabschluss ist erforderlich, wenn Sie das Modell des gewichteten Durchschnittsbestands verwenden, um Abrechnungen zu erstellen und den Wert von Ausgaben nach dem Prinzip des gewichteten Durchschnitts anzupassen. Bis Sie den Bestandsabschlussprozess ausführen, werden Ausgabetransaktionen zum laufenden Durchschnitt bewertet, wenn die physischen und finanziellen Aktualisierungen erfolgt sind. Sofern Sie nicht die Markierung verwenden, wird der laufende Durchschnitt berechnet, wenn die physische oder finanzielle Aktualisierung ausgeführt wird.

Die Lagernachkalkulationsmethode für den gewichteten Durchschnitt wird nach folgender Formel berechnet:

- Gewichteter Durchschnitt = (\[Q1 × P1\] + \[Q2 × P2\] + \[Q *n* × P *n*\]) ÷ (Q1 + Q2 + Q *n*)

Q = Menge der Transaktion  
P = Preis der Transaktion

Bei einem Ausgleich handelt es sich um eine Lagerabschlussbuchung zur Anpassung der Abgänge an den korrekten gewichteten Durchschnitt des Abschlussdatums. In den folgenden Beispielen werden die Auswirkungen der Verwendung des gewichteten Durchschnitts anhand von fünf unterschiedlichen Konfigurationen veranschaulicht:

- Gewichtete durchschnittliche Direktabrechnung ohne die Option **Physikalischen Wert einbeziehen**
- Gewichteter Durchschnitt zusammengefasste Abrechnung ohne die Option **Physikalischen Wert einbeziehen**.
- Gewichtete durchschnittliche Direktabrechnung mit der Option **Physikalischen Wert einbeziehen**
- Gewichtete durchschnittliche zusammengefasste Abrechnung mit der Option **Physikalischen Wert einbeziehen**
- Gewichteter Durchschnitt mit Markierung

## <a name="weighted-average-direct-settlement-without-include-physical-value"></a>Direkter Ausgleich mit gewichtetem Durchschnitt ohne "Physischen Wert einbeziehen"

Das Prinzip der direkten Abrechnung erstellt Abrechnungen direkt zwischen Zu- und Abgängen, ohne zusätzliche Transaktionen im Bestand zu erstellen. Das System verwendet dieses Prinzip der direkten Abrechnung in den folgenden Situationen:

- Ein Beleg und eine oder mehrere Ausgaben wurden in der Periode gebucht.
- Nur Ausgaben wurden in der Periode gebucht und der Bestand enthält Lagerbestände aus einem früheren Abschluss.

In diesem Beispiel ist das Kontrollkästchen **Physikalischen Wert einbeziehen** auf der **Elementmodellgruppe** für das zugelassene Produkt deaktiviert. Die folgende Abbildung zeigt diese Buchungen an:

- 1a. Physischer Lagerzugang für die Menge "10" zu jeweils EUR 10,00 (Kosten).
- 1b. Wertmäßiger Lagerzugang für die Menge "10" zu jeweils EUR 10,00 (Kosten).
- 2a. Physischer Lagerzugang für die Menge "10" zu jeweils EUR 20,00 (Kosten).
- 3a. Physischer Bestandsabgang für eine Menge von 1 zu einem Einstandspreis von USD 10,00 (laufender Durchschnitt der finanziell gebuchten Transaktionen).
- 3b. Bestandsfinanzausgang für eine Menge von 1 zu einem Einstandspreis von USD 10,00 (laufender Durchschnitt der finanziell gebuchten Transaktionen).
- 4a. Physischer Bestandsabgang für eine Menge von 1 zu Kosten von jeweils USD 10,00 (laufender Durchschnitt der finanziell gebuchten Transaktionen).
- 4b. Finanzielle Bestandsausgabe für eine Menge von 1 zu einer Kalkulation von jeweils USD 10,00 (laufender Durchschnitt der finanziell gebuchten Transaktionen).
- 5a. Physischer Bestandsabgang für eine Menge von 1 zu Kosten von jeweils USD 10,00 (laufender Durchschnitt der finanziell gebuchten Transaktionen).
- 6\. Lagerabschluss wird vorgenommen. Basierend auf der Methode des gewichteten Durchschnitts verwendet das System die Methode der direkten Abrechnung, da nur ein Beleg in der Periode finanziell fortgeschrieben wird. In diesem Beispiel wird eine Abrechnung zwischen 1b und 3b erstellt, eine weitere zwischen 1b und 4b. Es wird keine Anpassung vorgenommen, da der laufende Durchschnitt gleich dem gewichteten Durchschnitt ist.

Das folgende Diagramm veranschaulicht diese Reihe von Transaktionen mit den Auswirkungen der Wahl des Modells des gewichteten Durchschnittsbestands und des Prinzips der direkten Abrechnung ohne die Option **Physikalischen Wert einbeziehen**.

![WeightedAverage DS ohne Include physical value.](media/weighted-average-direct-settlement-without-include-physical-value.png)

**Diagrammschlüssel**

- Lagerbuchungen sind durch vertikale Pfeile dargestellt.
- Physische Transaktionen werden durch kürzere hellgraue Pfeile dargestellt.
- Finanzielle Transaktionen werden durch längere schwarze Pfeile dargestellt.
- Eingänge in den Bestand werden durch vertikale Pfeile oberhalb der Achse dargestellt.
- Ausgaben, die nicht im Bestand sind, werden durch vertikale Pfeile unterhalb der Achse dargestellt.
- Jede neue Zugangs- oder Abgangsbuchung wird mit einer neuen Beschriftung versehen.
- Jeder vertikale Pfeil ist mit einer Sequenzkennung (beispielsweise *1a*) versehen. Mit dieser Kennung wird die Reihenfolge der Lagerbuchungen auf der Zeitachse angegeben.
- Jedes Datum im Diagramm ist durch eine dünne schwarze vertikale Linie getrennt. Das Datum ist am unteren Rand des Diagramms vermerkt.
- Bestandsabschlüsse werden durch eine rote vertikale gestrichelte Zeile dargestellt.
- Ein durch einen Lagerabschluss vorgenommener Ausgleich ist durch rote diagonale gestrichelte Pfeile dargestellt, die von einem Zugang zu einem Abgang verlaufen.

## <a name="weighted-average-summarized-settlement-without-the-include-physical-value-option"></a>Zusammengefasster Ausgleich mit gewichtetem Durchschnitt ohne die Option "Physischen Wert einbeziehen"

Wenn es mehrere Eingänge in einer Periode gibt, verwendet der gewichtete Durchschnitt das Prinzip der zusammengefassten Abrechnung, bei dem alle Eingänge innerhalb einer Abschlussperiode in einer Transaktion namens *gewichteter durchschnittlicher Bestand Abschluss* zusammengefasst werden. Alle Eingänge für den Zeitraum werden mit der Ausgabe der neu erstellten Bestandstransaktion verrechnet. Alle Ausgaben für die Periode werden mit dem Eingang der neuen Transaktion für den Bestand verrechnet. Wenn nach dem Inventarabschluss noch ein Lagerbestand vorhanden ist, wird dieser in die Eingangstransaktion der gewichteten durchschnittlichen Inventarabschluss-Transaktionen aufgenommen.

Die folgenden Transaktionen sind in der folgenden Grafik dargestellt:

- 1a. Physischer Lagerzugang für die Menge "1" zu jeweils EUR 10,00 (Kosten).
- 1b. Wertmäßiger Lagerzugang für die Menge "1" zu jeweils EUR 10,00 (Kosten).
- 2a. Physischer Lagerzugang für die Menge "1" zu jeweils EUR 20,00 (Kosten).
- 2b. Wertmäßiger Lagerzugang für die Menge "1" zu jeweils EUR 22,00 (Kosten).
- 3a. Physischer Bestandsabgang für eine Menge von 1 zu einem Einstandspreis von USD 16,00 (laufender Durchschnitt der finanziell gebuchten Transaktionen).
- 3b. Bestandsfinanzausgang für eine Menge von 1 zu einem Einstandspreis von USD 16,00 (laufender Durchschnitt der finanziell gebuchten Transaktionen).
- 4a. Physischer Lagerzugang für die Menge "1" zu jeweils EUR 25,00 (Kosten).
- 5a. Physischer Lagerzugang für die Menge "1" zu jeweils EUR 30,00 (Kosten).
- 5b. Wertmäßiger Lagerzugang für die Menge "1" zu jeweils EUR 30,00 (Kosten).
- 6a. Physischer Bestandsabgang für eine Menge von 1 zu einem Einstandspreis von USD 23,00 (laufender Durchschnitt der finanziell gebuchten Transaktionen).
- 7\. Lagerabschluss wird vorgenommen.
- 7a. Der gewichtete durchschnittliche Finanzausgang der Transaktion zum Abschluss des Bestands wird erstellt, um die Abrechnungen aller finanziellen Eingänge des Bestands zu summieren.
  - Transaktion 1b wird für eine Menge von 1 mit einem Betrag von USD 10,00 abgerechnet.
  - Transaktion 2b wird für eine Menge von 1 mit einem Abrechnungsbetrag von USD 22,00 abgerechnet.
  - Transaktion 5b wird für eine Menge von 1 mit einem Abrechnungsbetrag von USD 30,00 abgerechnet.
  - Transaktion 7a. wird für eine Menge von 3 mit einem beglichenen Betrag von USD 62,00 erstellt. Diese Transaktion gleicht die Summe der drei Eingangstransaktionen aus, die in der Periode finanziell fortgeschrieben werden.
- 7b. Der gewichtete durchschnittliche finanzielle Eingang der Transaktion zum Bestandsabschluss wird als Ausgleich für die finanziell gebuchten Ausgaben erstellt.
  - Die Transaktion 3b wird für eine Menge von 1 mit einem Abrechnungsbetrag von USD 20,67 abgerechnet. Diese Transaktion wird um USD 4,67 korrigiert, um den ursprünglichen Wert von USD 16,00 auf 20,67 zu bringen, was dem gewichteten Durchschnitt der finanziell gebuchten Transaktionen für den Zeitraum entspricht.
  - Transaktion 7b. wird für eine Menge von 1 mit einem Rechnungsbetrag von USD 20,67 erstellt, um 3b auszugleichen. Diese Transaktion gleicht die Summe der einen Emissionstransaktion aus, die in der Periode finanziell verbucht wird.

Das folgende Diagramm veranschaulicht diese Reihe von Transaktionen mit den Auswirkungen der Wahl des Modells des gewichteten Durchschnittsbestands und des Prinzips der summarischen Abrechnung ohne die Option **Physikalischen Wert einbeziehen**.

![Gewichteter Durchschnitt SS ohne Einbeziehung des physischen Wertes.](media/weighted-average-summarized-settlement-without-include-physical-value.png)

**Diagrammschlüssel**

- Lagerbuchungen sind durch vertikale Pfeile dargestellt.
- Physische Transaktionen werden durch kürzere hellgraue Pfeile dargestellt.
- Finanzielle Transaktionen werden durch längere schwarze Pfeile dargestellt.
- Eingänge in den Bestand werden durch vertikale Pfeile oberhalb der Achse dargestellt.
- Ausgaben, die nicht im Bestand sind, werden durch vertikale Pfeile unterhalb der Achse dargestellt.
- Jede neue Zugangs- oder Abgangsbuchung wird mit einer neuen Beschriftung versehen.
- Jeder vertikale Pfeil ist mit einer Sequenzkennung (beispielsweise *1a*) versehen. Mit dieser Kennung wird die Reihenfolge der Lagerbuchungen auf der Zeitachse angegeben.
- Jedes Datum im Diagramm ist durch eine dünne schwarze vertikale Linie getrennt. Das Datum ist am unteren Rand des Diagramms vermerkt.
- Bestandsabschlüsse werden durch eine rote vertikale gestrichelte Zeile dargestellt.
- Ein durch einen Lagerabschluss vorgenommener Ausgleich ist durch rote diagonale gestrichelte Pfeile dargestellt, die von einem Zugang zu einem Abgang verlaufen.

## <a name="weighted-average-direct-settlement-with-the-include-physical-value-option"></a>Direkter Ausgleich mit gewichtetem Durchschnitt und der Option "Physischen Wert einbeziehen"

Der Parameter **Physikalischen Wert einbeziehen** funktioniert mit dem Modell für den gewichteten durchschnittlichen Bestand anders als in früheren Versionen des Produkts. Wenn Sie die Option **Physikalischen Wert einbeziehen** für ein Element im Formular **Elementmodellgruppe** wählen, verwendet das System bei der Berechnung des geschätzten Ausgabepreises oder des laufenden Durchschnitts physisch aktualisierte Belege. Die Buchung der Abgänge während der Periode erfolgt auf Basis dieses vorkalkulierten Einstandspreises. Beim Lagerabschluss werden wertmäßig aktualisierte Zugänge ausschließlich in der Berechnung des gewichteten Durchschnitts berücksichtigt.

Die folgenden Transaktionen sind in der folgenden Grafik dargestellt:

- 1a. Physischer Lagerzugang für die Menge "10" zu jeweils EUR 10,00 (Kosten).
- 1b. Wertmäßiger Lagerzugang für die Menge "10" zu jeweils EUR 10,00 (Kosten).
- 2a. Physischer Lagerzugang für die Menge "10" zu jeweils EUR 20,00 (Kosten).
- 3a. Inventarabgang für eine Menge von 1 zu einem Einstandspreis von USD 15,00 (laufender Durchschnitt der physisch und finanziell gebuchten Transaktionen).
- 3b. Finanzieller Bestandsabgang für eine Menge von 1 zu einem Einstandspreis von USD 15,00 (laufender Durchschnitt der physisch und finanziell gebuchten Transaktionen).
- 4a. Physischer Bestandsabgang für eine Menge von 1 zu Kosten von jeweils USD 15,00 (laufender Durchschnitt der physisch und finanziell gebuchten Transaktionen).
- 4b. Finanzieller Bestandsabgang für eine Menge von 1 zu einem Preis von jeweils USD 15,00 (laufender Durchschnitt der physisch und finanziell gebuchten Transaktionen).
- 5a. Physischer Bestandsabgang für eine Menge von 1 zu Kosten von jeweils USD 15,00 (laufender Durchschnitt der physisch und finanziell gebuchten Transaktionen).
- 6\. Lagerabschluss wird vorgenommen. Basierend auf der Methode des gewichteten Durchschnitts verwendet das System die Methode der direkten Abrechnung, da nur ein Beleg in der Periode finanziell fortgeschrieben wird. In diesem Beispiel wird eine Abrechnung zwischen 1b und 3b erstellt, eine weitere zwischen 1b und 4b. Die Transaktionen 3b und 4b werden jeweils um USD -5,00 korrigiert, um den Wert auf USD 10,00 zu bringen.

Das folgende Diagramm veranschaulicht diese Reihe von Transaktionen mit den Auswirkungen der Wahl des Modells für den gewichteten durchschnittlichen Bestand und des Prinzips der direkten Abrechnung mit der Option **Physikalischen Wert einbeziehen**.

![Gewichteter Durchschnitt DS mit Include physical value.](media/weighted-average-direct-settlement-with-include-physical-value.png)

**Diagrammschlüssel**

- Lagerbuchungen sind durch vertikale Pfeile dargestellt.
- Physische Transaktionen werden durch kürzere hellgraue Pfeile dargestellt.
- Finanzielle Transaktionen werden durch längere schwarze Pfeile dargestellt.
- Eingänge in den Bestand werden durch vertikale Pfeile oberhalb der Achse dargestellt.
- Ausgaben, die nicht im Bestand sind, werden durch vertikale Pfeile unterhalb der Achse dargestellt.
- Jede neue Zugangs- oder Abgangsbuchung wird mit einer neuen Beschriftung versehen.
- Jeder vertikale Pfeil ist mit einer Sequenzkennung (beispielsweise *1a*) versehen. Mit dieser Kennung wird die Reihenfolge der Lagerbuchungen auf der Zeitachse angegeben.
- Jedes Datum im Diagramm ist durch eine dünne schwarze vertikale Linie getrennt. Das Datum ist am unteren Rand des Diagramms vermerkt.
- Bestandsabschlüsse werden durch eine rote vertikale gestrichelte Zeile dargestellt.
- Ein durch einen Lagerabschluss vorgenommener Ausgleich ist durch rote diagonale gestrichelte Pfeile dargestellt, die von einem Zugang zu einem Abgang verlaufen.

## <a name="weighted-average-summarized-settlement-with-the-include-physical-value-option"></a>Zusammengefasster Ausgleich mit gewichtetem Durchschnitt und der Option "Physischen Wert einbeziehen"

Der Parameter **Physikalischen Wert einbeziehen** funktioniert mit gewichtetem Durchschnitt anders als in früheren Versionen. Markieren Sie das Kontrollkästchen **Physikalischen Wert einbeziehen** für ein Element auf der Seite **Elementmodellgruppe**. Vom System werden zur Berechnung des vorkalkulierten Einstandspreises (oder des laufenden Durchschnitts) physisch aktualisierte Zugänge verwendet. Die Buchung der Abgänge während der Periode erfolgt auf Basis dieses vorkalkulierten Einstandspreises. Beim Lagerabschluss werden wertmäßig aktualisierte Zugänge ausschließlich in der Berechnung des gewichteten Durchschnitts berücksichtigt. Wenn Sie den gewichteten Durchschnitt verwenden, empfiehlt es sich, einen monatlichen Lagerabschluss durchzuführen. In diesem Beispiel für einen zusammengefassten Ausgleich mit gewichtetem Durchschnitt ist die Lagersteuerungsgruppe so konfiguriert, dass der physische Wert einbezogen wird.

Die folgenden Transaktionen sind in der folgenden Grafik dargestellt:

- 1a. Physischer Lagerzugang für die Menge "1" zu jeweils EUR 10,00 (Kosten).
- 1b. Wertmäßiger Lagerzugang für die Menge "1" zu jeweils EUR 10,00 (Kosten).
- 2a. Physischer Lagerzugang für die Menge "1" zu jeweils EUR 20,00 (Kosten).
- 2b. Wertmäßiger Lagerzugang für die Menge "1" zu jeweils EUR 22,00 (Kosten).
- 3a. Inventarabgang für eine Menge von 1 zu einem Einstandspreis von USD 16,00 (laufender Durchschnitt der physisch und finanziell gebuchten Transaktionen).
- 3b. Finanzieller Bestandsabgang für eine Menge von 1 zu einem Einstandspreis von USD 16,00 (laufender Durchschnitt der physisch und finanziell gebuchten Transaktionen).
- 4a. Physischer Lagerzugang für die Menge "1" zu jeweils EUR 25,00 (Kosten).
- 5a. Physischer Lagerzugang für die Menge "1" zu jeweils EUR 30,00 (Kosten).
- 5b. Wertmäßiger Lagerzugang für die Menge "1" zu jeweils EUR 30,00 (Kosten).
- 6a. Physischer Bestandsabgang für eine Menge von 1 zu einem Einstandspreis von USD 23,67 (laufender Durchschnitt der physisch und finanziell gebuchten Transaktionen).
- 7\. Lagerabschluss wird vorgenommen.
- 7a. Der gewichtete durchschnittliche Finanzausgang der Transaktion zum Abschluss des Bestands wird erstellt, um die Abrechnungen aller finanziellen Eingänge des Bestands zu summieren.
  - Transaktion 1b wird für eine Menge von 1 mit einem Betrag von USD 10,00 abgerechnet.
  - Transaktion 2b wird für eine Menge von 1 mit einem Abrechnungsbetrag von USD 22,00 abgerechnet.
  - Transaktion 5b wird für eine Menge von 1 mit einem Abrechnungsbetrag von USD 30,00 abgerechnet.
  - Transaktion 7a. wird für eine Menge von 3 mit einem beglichenen Betrag von USD 62,00 erstellt.  
- 7b. Die gewichtete durchschnittliche Bestandsabschluss-Transaktion Finanzieller Eingang wird erstellt, um die Transaktionen des Finanziellen Ausgangs zu verrechnen.
  - Die Transaktion 3b wird für eine Menge von 1 mit einem Abrechnungsbetrag von USD 20,67 abgerechnet. Diese Transaktion wird um USD 4,67 korrigiert, um den ursprünglichen Wert von USD 16,00 auf 20,67 zu bringen, was dem gewichteten Durchschnitt der finanziell gebuchten Transaktionen für den Zeitraum entspricht.
  - Transaktion 7b. wird für eine Menge von 1 mit einem Rechnungsbetrag von USD 20,67 erstellt, um 3b auszugleichen.

Das folgende Diagramm veranschaulicht diese Reihe von Transaktionen mit den Auswirkungen der Wahl des Modells des gewichteten Durchschnittsbestands und des Prinzips der summarischen Abrechnung ohne die Option **Physikalischen Wert einbeziehen**.

![WeightedAverage SS mit Include physical value.](media/weighted-average-summarized-settlement-with-include-physical-value.png)

**Diagrammschlüssel**

- Lagerbuchungen sind durch vertikale Pfeile dargestellt.
- Physische Transaktionen werden durch kürzere hellgraue Pfeile dargestellt.
- Finanzielle Transaktionen werden durch längere schwarze Pfeile dargestellt.
- Eingänge in den Bestand werden durch vertikale Pfeile oberhalb der Achse dargestellt.
- Ausgaben, die nicht im Bestand sind, werden durch vertikale Pfeile unterhalb der Achse dargestellt.
- Jede neue Zugangs- oder Abgangsbuchung wird mit einer neuen Beschriftung versehen.
- Jeder vertikale Pfeil ist mit einer Sequenzkennung (beispielsweise *1a*) versehen. Mit dieser Kennung wird die Reihenfolge der Lagerbuchungen auf der Zeitachse angegeben.
- Jedes Datum im Diagramm ist durch eine dünne schwarze vertikale Linie getrennt. Das Datum ist am unteren Rand des Diagramms vermerkt.
- Bestandsabschlüsse werden durch eine rote vertikale gestrichelte Zeile dargestellt.
- Ein durch einen Lagerabschluss vorgenommener Ausgleich ist durch rote diagonale gestrichelte Pfeile dargestellt, die von einem Zugang zu einem Abgang verlaufen.

## <a name="weighted-average-with-marking"></a>Gewichteter Durchschnitt mit Markierung

Der Begriff "Markierung" bezeichnet ein Verfahren zum Verknüpfen (oder Markieren) einer Abgangsbuchung mit einer Zugangsbuchung. Eine Markierung kann entweder vor oder nach Ausführung der Buchung erfolgen. Durch die Verwendung einer Markierung lassen sich bei der Ausführung der Buchung oder des Lagerabschlusses die exakten Kosten des Lagers ermitteln.

Beispiel: In der Kundendienstabteilung wurde der Eilauftrag eines wichtigen Debitors angenommen. Da es sich um eine Eilbestellung handelt, müssen Sie für dieses Element mehr bezahlen, um den Wunsch Ihres Kunden zu erfüllen. Deshalb möchten Sie sichergehen, dass bei der Auftragsrechnung die Kosten für diesen Lagerartikel in der Gewinnspanne (auch: Wareneinsatz, COGS) berücksichtigt werden.

Bei der Buchung der Bestellung erhält das Lager einen Zugang in Höhe von EUR 120,00 (Kosten). Beispielsweise wird dieses Auftragsdokument vor der Buchung des Lieferscheins oder der Rechnung für die Bestellung markiert. Der Wareneinsatz (COGS) beträgt anstelle der aktuellen laufenden Durchschnittskosten für den Artikel dann EUR 120,00. Wird der Lieferschein oder die Rechnung des Auftrags gebucht, bevor die Markierung vorgenommen wird, erfolgt die Buchung des Wareneinsatzes zum laufenden Durchschnittseinstandspreis.

Die Markierung der beiden Buchungen kann noch bis zur Ausführung des Lagerabschlusses nachgeholt werden.

Eine Zugangsbuchung wird für eine Abgangsbuchung markiert. Dann wird die für die Artikelmodellgruppe des Elements ausgewählte Bewertungsmethode nicht berücksichtigt und das System rechnet diese Transaktionen miteinander ab.

Sie können vor der Ausführung der Buchung eine Abgangsbuchung für einen Zugang markieren. Dies kann von einer Auftragsposition auf der Seite **Auftragsdetails** aus erfolgen. Die offenen Quittungstransaktionen werden auf der Seite **Markierung** angezeigt.

Sie können nach der Ausführung der Buchung eine Abgangsbuchung für einen Zugang markieren. Sie können eine Abgangsbuchung für eine offene Zugangsbuchung für einen gelagerten Artikel aus einer gebuchten Lagerregulierungserfassung abgleichen oder markieren.

Die folgenden Transaktionen sind in der folgenden Grafik dargestellt:

- 1a. Physischer Lagerzugang für die Menge "1" zu jeweils EUR 10,00 (Kosten).
- 1b. Wertmäßiger Lagerzugang für die Menge "1" zu jeweils EUR 10,00 (Kosten).
- 2a. Physischer Lagerzugang für die Menge "1" zu jeweils EUR 20,00 (Kosten).
- 2b. Wertmäßiger Lagerzugang für die Menge "1" zu jeweils EUR 22,00 (Kosten).
- 3a. Physischer Bestandsabgang für eine Menge von 1 zu einem Einstandspreis von USD 16,00 (laufender Durchschnitt der finanziell gebuchten Transaktionen).
- 3b. Bestandsfinanzausgang für eine Menge von 1 zu einem Einstandspreis von USD 16,00 (laufender Durchschnitt der finanziell gebuchten Transaktionen).
- 3c. Der Bestandsfinanzausgang für 3b wird mit dem Bestandsfinanzausgang für 2b markiert.
- 4a. Physischer Lagerzugang für die Menge "1" zu jeweils EUR 25,00 (Kosten).
- 5a. Physischer Lagerzugang für die Menge "1" zu jeweils EUR 30,00 (Kosten).
- 5b. Wertmäßiger Lagerzugang für die Menge "1" zu jeweils EUR 30,00 (Kosten).
- 6a. Physischer Bestandsabgang für eine Menge von 1 zu einem Einstandspreis von USD 23,00 (laufender Durchschnitt der finanziell gebuchten Transaktionen).
- 7\. Lagerabschluss wird vorgenommen. Beim Markierungsprinzip nach der Methode des gewichteten Durchschnitts werden die markierten Transaktionen miteinander verrechnet. In diesem Beispiel wird 3b gegen 2b abgerechnet und eine Korrektur von 6,00 USD auf 3b gebucht, um den Wert auf 22,00 USD zu bringen. In diesem Beispiel werden keine weiteren Abrechnungen vorgenommen, da der Abschluss nur Abrechnungen für finanziell aktualisierte Transaktionen erstellt.

Das folgende Diagramm veranschaulicht diese Reihe von Transaktionen mit den Auswirkungen der Wahl des gewichteten durchschnittlichen Bestandsmodells mit Markierung.

![Gewichteter Durchschnitt mit Markierung.](media/weighted-average-with-marking.png)

**Diagrammschlüssel**

- Lagerbuchungen sind durch vertikale Pfeile dargestellt.
- Physische Transaktionen werden durch kürzere hellgraue Pfeile dargestellt.
- Finanzielle Transaktionen werden durch längere schwarze Pfeile dargestellt.
- Eingänge in den Bestand werden durch vertikale Pfeile oberhalb der Achse dargestellt.
- Ausgaben, die nicht im Bestand sind, werden durch vertikale Pfeile unterhalb der Achse dargestellt.
- Jede neue Zugangs- oder Abgangsbuchung wird mit einer neuen Beschriftung versehen.
- Jeder vertikale Pfeil ist mit einer Sequenzkennung (beispielsweise *1a*) versehen. Mit dieser Kennung wird die Reihenfolge der Lagerbuchungen auf der Zeitachse angegeben.
- Jedes Datum im Diagramm ist durch eine dünne schwarze vertikale Linie getrennt. Das Datum ist am unteren Rand des Diagramms vermerkt.
- Bestandsabschlüsse werden durch eine rote vertikale gestrichelte Zeile dargestellt.
- Ein durch einen Lagerabschluss vorgenommener Ausgleich ist durch rote diagonale gestrichelte Pfeile dargestellt, die von einem Zugang zu einem Abgang verlaufen.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
