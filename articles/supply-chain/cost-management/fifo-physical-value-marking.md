---
title: FIFO mit physischem Wert und Markierung
description: Bei FIFO (First in, First out) handelt es sich um eine Lagersteuerung, bei der die zuerst erworbenen Zugänge das Lager als Erstes wieder verlassen. Wertmäßig aktualisierte Abgänge aus dem Lager werden mit dem ältesten wertmäßig aktualisierten Zugang zu einem Lagerbestand ausgeglichen, der auf dem wertmäßigen Datum der Lagerbuchung basiert.
author: JennySong-SH
ms.date: 02/02/2022
ms.topic: article
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 54682
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 663dce9f871e96fec7017616732428c49b1224a0
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2022
ms.locfileid: "8676242"
---
# <a name="fifo-with-physical-value-and-marking"></a>FIFO mit physischem Wert und Markierung

[!include [banner](../includes/banner.md)]


First in, first out (FIFO) ist eine Methode der Lagerverwaltung und -bewertung, bei der die zuerst produzierten oder erworbenen Bestände zuerst verkauft, verwendet oder entsorgt werden. Während des Bestandsabschlusses in Microsoft Dynamics 365 Supply Chain Management erstellt das System Abrechnungen, bei denen der erste Zugang mit dem ersten Abgang abgeglichen wird, und so weiter.

Die Abrechnungen und das Abgleichsprinzip beruhen auf dem Finanzdatum der Transaktionen im Bestand. Eine vorläufige Bewertung der Abrechnungen und Anpassungen kann durch Ausführen der Bestandsneuberechnung vorgenommen werden.

Sie können das FIFO-Prinzip außer Kraft setzen, indem Sie Transaktionen im Bestand so markieren, dass ein bestimmter Artikel-Eingang mit einer bestimmten Ausgabe verrechnet wird. Ein periodischer Bestandsabschluss ist erforderlich, wenn Sie das FIFO-Bestandsmodell verwenden, um Abrechnungen zu erstellen und den Wert von Ausgaben nach dem FIFO-Prinzip anzupassen. Bis Sie den Bestandsabschlussprozess ausführen, werden Ausgabetransaktionen zum laufenden Durchschnitt bewertet, wenn die physischen und finanziellen Aktualisierungen erfolgt sind. Sofern Sie nicht die Markierung verwenden, wird der laufende Durchschnitt berechnet, wenn die physische oder finanzielle Aktualisierung ausgeführt wird. In den folgenden Beispielen werden die Auswirkungen der Verwendung von FIFO anhand von drei unterschiedlichen Konfigurationen veranschaulicht:

- FIFO ohne die Option **Physischen Wert einbeziehen**
- FIFO mit der Option **Physischen Wert einbeziehen**
- FIFO mit Markierung

## <a name="fifo-without-the-include-physical-value-option"></a>FIFO ohne die Option "Physischen Wert einbeziehen"

In diesem Beispiel ist das Kontrollkästchen **Physikalischen Wert einbeziehen** in der Artikelmodellgruppe für das zugelassene Produkt deaktiviert. Die folgende Abbildung zeigt diese Buchungen an:

- 1a. Physischer Lagerzugang für die Menge "1" zu jeweils EUR 10,00 (Kosten).
- 1b. Wertmäßiger Lagerzugang für die Menge "1" zu jeweils EUR 10,00 (Kosten).
- 2a. Physischer Lagerzugang für die Menge "1" zu jeweils EUR 20,00 (Kosten).
- 2b. Wertmäßiger Lagerzugang für die Menge "1" zu jeweils EUR 22,00 (Kosten).
- 3a. Physischer Bestandsabgang für eine Menge von 1 zu einem Einstandspreis von USD 16,00 (laufender Durchschnitt der finanziell gebuchten Transaktionen).
- 3b. Bestandsfinanzausgang für eine Menge von 1 zu einem Einstandspreis von USD 16,00 (laufender Durchschnitt der finanziell gebuchten Transaktionen).
- 4a. Physischer Lagerzugang für die Menge "1" zu jeweils EUR 25,00 (Kosten).
- 5a. Physischer Lagerzugang für die Menge "1" zu jeweils EUR 30,00 (Kosten).
- 5b. Wertmäßiger Lagerzugang für die Menge "1" zu jeweils EUR 30,00 (Kosten).
- 6a. Inventarabgang für eine Menge von 1 zu einem Einstandspreis von USD 23,00 (laufender Durchschnitt der finanziell gebuchten Transaktionen)
- 7\. Lagerabschluss wird vorgenommen. Basierend auf der FIFO-Methode wird die erste finanziell aktualisierte Ausgabe mit der ersten finanziell aktualisierten Einnahme verrechnet, usw. In diesem Beispiel wird eine Abrechnung zwischen 1b und 3b erstellt. Auf 3b wird eine Anpassung von USD -6,00 vorgenommen, sodass die endgültigen Kosten USD 10,00 betragen.

In dem neuen laufenden Durchschnittseinstandspreis ist der Durchschnitt der wertmäßig aktualisierten Buchungen berücksichtigt. Die folgenden Abbildungen zeigen die Auswirkungen des Lagermodells FIFO auf diese Buchungsserie an, wenn die Option **Physischen Wert einbeziehen** nicht verwendet wird.

![FIFO ohne die Option Physischen Wert einbeziehen.](./media/fifo-without-include-physical-value.png)

**Diagrammschlüssel**

- Lagerbuchungen sind durch vertikale Pfeile dargestellt.
- Physische Transaktionen werden durch kürzere hellgraue Pfeile dargestellt.
- Finanzielle Transaktionen werden durch längere schwarze Pfeile dargestellt.
- Zugänge zum Lager sind als vertikale Pfeile über der Zeitachse dargestellt.
- Abgänge aus dem Lager sind als vertikale Pfeile unter der Zeitachse dargestellt.
- Jede neue Zugangs- oder Abgangsbuchung wird mit einer neuen Beschriftung versehen.
- Jeder vertikale Pfeil ist mit einer Sequenzkennung (beispielsweise *1a*) versehen. Mit dieser Kennung wird die Reihenfolge der Lagerbuchungen auf der Zeitachse angegeben.
- Jedes Datum im Diagramm ist durch eine dünne schwarze vertikale Linie getrennt. Das Datum ist am unteren Rand des Diagramms vermerkt.
- Bestandsabschlüsse werden durch eine rote vertikale gestrichelte Zeile dargestellt.
- Ein durch einen Lagerabschluss vorgenommener Ausgleich ist durch rote diagonale gestrichelte Pfeile dargestellt, die von einem Zugang zu einem Abgang verlaufen.

## <a name="fifo-with-the-include-physical-value-option"></a>FIFO mit der Option "Physischen Wert einbeziehen"

Wenn das Kontrollkästchen **Physikalischen Wert einbeziehen** für einen Artikel auf der Seite **Artikelmodellgruppe** aktiviert ist, verwendet das System sowohl physische als auch finanzielle Zugangstransaktionen, um die laufende durchschnittliche Kalkulation zu berechnen. Falls zutreffend, passt das System auch die physisch aktualisierte Ausgabe-Transaktion an. Bestandsabschlüsse, die das FIFO-Bestandsmodell verwenden, rechnen nur mit Transaktionen ab, die finanziell aktualisiert werden. Die folgende Abbildung zeigt diese Buchungen an:

- 1a. Physischer Lagerzugang für die Menge "1" zu jeweils EUR 10,00 (Kosten).
- 1b. Wertmäßiger Lagerzugang für die Menge "1" zu jeweils EUR 10,00 (Kosten).
- 2a. Physischer Lagerzugang für die Menge "1" zu jeweils EUR 20,00 (Kosten).
- 2b. Wertmäßiger Lagerzugang für die Menge "1" zu jeweils EUR 22,00 (Kosten).
- 3a. Inventarabgang für eine Menge von 1 zu einem Einstandspreis von USD 16,00 (laufender Durchschnitt der physisch und finanziell gebuchten Transaktionen).
- 3b. Finanzieller Bestandsabgang für eine Menge von 1 zu einem Einstandspreis von USD 16,00 (laufender Durchschnitt der physisch und finanziell gebuchten Transaktionen).
- 4a. Physischer Lagerzugang für die Menge "1" zu jeweils EUR 25,00 (Kosten).
- 5a. Physischer Lagerzugang für die Menge "1" zu jeweils EUR 30,00 (Kosten).
- 5b. Wertmäßiger Lagerzugang für die Menge "1" zu jeweils EUR 30,00 (Kosten).
- 6a. Physischer Bestandsabgang für eine Menge von 1 zu einem Einstandspreis von USD 23,67 (laufender Durchschnitt der physisch und finanziell gebuchten Transaktionen).
- 7\. Lagerabschluss wird vorgenommen. Basierend auf der FIFO-Methode wird die erste finanziell aktualisierte Ausgabe mit der ersten finanziell aktualisierten Einnahme verrechnet, usw. In diesem Beispiel wird eine Abrechnung zwischen 1b und 3b erstellt. Auf 3b wird eine Anpassung von USD -6,00 vorgenommen, sodass die endgültigen Kosten USD 10,00 betragen. Außerdem wird die Transaktion 6a an die Kalkulation der Quittungstransaktion von 2b angepasst. Diese Buchungen werden vom System nicht ausgeglichen, da der Zugang nur physisch, nicht aber wertmäßig aktualisiert wurde. Stattdessen wird nur eine Anpassung von USD -1,67 auf die physische Emissionstransaktion gebucht, und die angepassten Kosten betragen USD 22,00.

![FIFO mit der Option Physikalischen Wert einbeziehen.](./media/fifo-with-include-physical-value.png)

Beachten Sie, dass das Ergebnis des Ausführens des Bestandsabschlusses dasselbe ist, unabhängig davon, ob Sie die Option **Physikalischen Wert einbeziehen** auf der Seite **Artikelmodellgruppe** auswählen. Die Option **Physikalischen Wert einbeziehen** wirkt sich nur auf den laufenden Durchschnitt aus.

**Diagrammschlüssel**

- Lagerbuchungen sind durch vertikale Pfeile dargestellt.
- Physische Transaktionen werden durch kürzere hellgraue Pfeile dargestellt.
- Finanzielle Transaktionen werden durch längere schwarze Pfeile dargestellt.
- Zugänge zum Lager sind als vertikale Pfeile über der Zeitachse dargestellt.
- Abgänge aus dem Lager sind als vertikale Pfeile unter der Zeitachse dargestellt.
- Jede neue Zugangs- oder Abgangsbuchung wird mit einer neuen Beschriftung versehen.
- Jeder vertikale Pfeil ist mit einer Sequenzkennung (beispielsweise *1a*) versehen. Mit dieser Kennung wird die Reihenfolge der Lagerbuchungen auf der Zeitachse angegeben.
- Jedes Datum im Diagramm ist durch eine dünne schwarze vertikale Linie getrennt. Das Datum ist am unteren Rand des Diagramms vermerkt.
- Bestandsabschlüsse werden durch eine rote vertikale gestrichelte Zeile dargestellt.
- Ein durch einen Lagerabschluss vorgenommener Ausgleich ist durch rote diagonale gestrichelte Pfeile dargestellt, die von einem Zugang zu einem Abgang verlaufen.

## <a name="fifo-with-marking"></a>FIFO mit Markierung

Der Begriff "Markierung" bezeichnet ein Verfahren zum Verknüpfen (oder Markieren) einer Abgangsbuchung mit einer Zugangsbuchung. Eine Markierung kann entweder vor oder nach Ausführung der Buchung erfolgen. Durch die Verwendung einer Markierung lassen sich bei der Ausführung der Buchung oder des Lagerabschlusses die exakten Kosten des Lagers ermitteln.

Beispiel: In der Kundendienstabteilung wurde der Eilauftrag eines wichtigen Debitors angenommen. Da es sich bei dieser Bestellung um eine Eilbestellung handelt, müssen Sie für diesen Artikel mehr bezahlen, um den Wunsch Ihres Debitors zu erfüllen. Sie müssen sicherstellen, dass sich die Kosten des Artikels im Bestand in der Marge oder den Kosten der verkauften Waren (COGS) für die Verkaufsrechnung widerspiegeln. Bei der Buchung der Bestellung erhält das Lager einen Zugang in Höhe von EUR 120,00 (Kosten). Wenn der Verkaufsauftragsbeleg zur Bestellung markiert wird, bevor der Lieferschein oder die Rechnung ausgeführt wird, betragen die COGS USD 120,00 und nicht die aktuellen laufenden Durchschnittskosten für den Artikel. Wird der Lieferschein oder die Rechnung des Auftrags gebucht, bevor die Markierung vorgenommen wird, erfolgt die Buchung des Wareneinsatzes (COGS) zum laufenden Durchschnittseinstandspreis. Die Markierung der beiden Buchungen kann noch bis zur Ausführung des Lagerabschlusses nachgeholt werden.

Wenn eine Bon-Transaktion zu einer Ausgabe-Transaktion markiert wird, wird die Bewertungsmethode, die in der Artikelmodellgruppe definiert ist, nicht berücksichtigt und das System rechnet diese Transaktionen miteinander ab. Sie können eine Transaktion gegen eine Verkaufsauftragszeile auf der Seite **Kaufauftragsdetails** manuell markieren, indem Sie auf dem Inforegister **Kaufauftragszeilen** die Option **Bestand \> Markierung** wählen. Sie können die offenen Zugangsbuchungen auf der Seite **Markierung** anzeigen. Sie können eine Ausgabetransaktion mit einer offenen Zugangstransaktion für einen inventarisierten Artikel aus einem gebuchten Lagererfassungs-Journal abgleichen oder markieren. Die folgende Abbildung zeigt diese Buchungen an:

- 1a. Physischer Lagerzugang für die Menge "1" zu jeweils EUR 10,00 (Kosten).
- 1b. Wertmäßiger Lagerzugang für die Menge "1" zu jeweils EUR 10,00 (Kosten).
- 2a. Physischer Lagerzugang für die Menge "1" zu jeweils EUR 20,00 (Kosten).
- 2b. Wertmäßiger Lagerzugang für die Menge "1" zu jeweils EUR 22,00 (Kosten).
- 3a. Physischer Bestandsabgang für eine Menge von 1 zu einem Einstandspreis von USD 16,00 (laufender Durchschnitt der finanziell gebuchten Transaktionen).
- 3b. Bestandsfinanzausgang für eine Menge von 1 zu einem Einstandspreis von USD 16,00 (laufender Durchschnitt der finanziell gebuchten Transaktionen).
- 3c. Der Bestandsfinanzausgang für 3b wird mit dem Bestandsfinanzausgang für 2b markiert.
- 4a. Physischer Lagerzugang für die Menge "1" zu jeweils EUR 25,00 (Kosten).
- 5a. Physischer Lagerzugang für die Menge "1" zu jeweils EUR 30,00 (Kosten).
- 5b. Wertmäßiger Lagerzugang für die Menge "1" zu jeweils EUR 30,00 (Kosten).
- 6a. Inventarabgang für eine Menge von 1 zu einem Einstandspreis von USD 23,00 (laufender Durchschnitt der finanziell gebuchten Transaktionen)
- 7\. Lagerabschluss wird vorgenommen. Basierend auf dem Markierungsprinzip, das die FIFO-Methode verwendet, werden die markierten Transaktionen gegeneinander abgerechnet. In diesem Beispiel wird 3b gegen 2b abgerechnet und eine Korrektur von 6,00 USD auf 3b gebucht, um den Wert auf 22,00 USD zu bringen. In diesem Beispiel werden keine weiteren Abrechnungen vorgenommen, da der Abschluss nur Abrechnungen für finanziell aktualisierte Transaktionen erstellt.

Die folgende Abbildung gibt Aufschluss über die Auswirkungen des FIFO-Lagermodells auf diese Reihe von Buchungen, die bei markierten Ab- und Zugängen anfallen.

![FIFO mit Markierung.](./media/fifo-with-marking.png)

**Diagrammschlüssel**

- Lagerbuchungen sind durch vertikale Pfeile dargestellt.
- Physische Transaktionen werden durch kürzere hellgraue Pfeile dargestellt.
- Finanzielle Transaktionen werden durch längere schwarze Pfeile dargestellt.
- Zugänge zum Lager sind als vertikale Pfeile über der Zeitachse dargestellt.
- Abgänge aus dem Lager sind als vertikale Pfeile unter der Zeitachse dargestellt.
- Jede neue Zugangs- oder Abgangsbuchung wird mit einer neuen Beschriftung versehen.
- Jeder vertikale Pfeil ist mit einer Sequenzkennung (beispielsweise *1a*) versehen. Mit dieser Kennung wird die Reihenfolge der Lagerbuchungen auf der Zeitachse angegeben.
- Jedes Datum im Diagramm ist durch eine dünne schwarze vertikale Linie getrennt. Das Datum ist am unteren Rand des Diagramms vermerkt.
- Bestandsabschlüsse werden durch eine rote vertikale gestrichelte Zeile dargestellt.
- Abrechnungen und Markierungen, die durch Bestandsabschluss durchgeführt werden, werden durch rote diagonal gestrichelte Pfeile dargestellt, die von einem Eingang zu einem Ausgang führen.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
