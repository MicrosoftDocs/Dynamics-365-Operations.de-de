---
title: LIFO mit physischem Wert und Markierung
description: Bei LIFO (Last in, First out) handelt es sich um ein Lagermodell, bei dem die zuletzt eingegangenen Zugänge das Lager als Erstes wieder verlassen. Abgänge aus dem Lager werden mit den neuesten Zugängen im Lager auf der Grundlage des Datums der Lagerbuchung abgeglichen.
author: AndersGirke
ms.date: 02/02/2022
ms.topic: article
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 55021
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fd57d58aa91aa87b1c2feff52a568296fc18ed9b
ms.sourcegitcommit: fefe93f3f44d8aa0b7e6d54cc4a3e5eca6e64feb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2022
ms.locfileid: "8092163"
---
# <a name="lifo-with-physical-value-and-marking"></a>LIFO mit physischem Wert und Markierung

[!include [banner](../includes/banner.md)]

Last in, first out (LIFO) ist eine Methode der Bestandsverwaltung und -bewertung, bei der die zuletzt produzierten oder erworbenen Bestände zuerst verkauft, verwendet oder entsorgt werden. Während des Bestandsabschlusses in Microsoft Dynamics 365 Supply Chain Management erstellt das System Abrechnungen, bei denen der letzte Zugang mit dem ersten Abgang abgeglichen wird, und so weiter. Die Abrechnungen und das Abgleichsprinzip beruhen auf dem Finanzdatum der Transaktionen im Bestand. Eine vorläufige Bewertung der Abrechnungen und Anpassungen kann durch Ausführen der Bestandsneuberechnung vorgenommen werden.

Sie können das LIFO-Prinzip außer Kraft setzen, indem Sie Bestandstransaktionen so markieren, dass ein bestimmter Artikelzugang mit einer bestimmten Ausgabe verrechnet wird. Ein periodischer Bestandsabschluss ist erforderlich, wenn Sie das LIFO-Bestandsmodell verwenden, um Abrechnungen zu erstellen und den Wert von Ausgaben nach dem LIFO-Prinzip anzupassen. Bis Sie den Bestandsabschlussprozess ausführen, werden Ausgabetransaktionen zum laufenden Durchschnitt bewertet, wenn die physischen und finanziellen Aktualisierungen erfolgt sind. Sofern Sie nicht die Markierung verwenden, wird der laufende Durchschnitt berechnet, wenn die physische oder finanzielle Aktualisierung ausgeführt wird.

In den folgenden Beispielen werden die Auswirkungen der Verwendung von LIFO anhand von drei unterschiedlichen Konfigurationen veranschaulicht:

- LIFO ohne die Option **Physischen Wert einbeziehen**
- LIFO mit der Option **Physischen Wert einbeziehen**
- LIFO mit Markierung

## <a name="lifo-without-the-include-physical-value-option"></a>LIFO ohne die Option "Physischen Wert einbeziehen"

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
- 7\. Lagerabschluss wird vorgenommen. Auf der Grundlage der LIFO-Methode wird die erste finanziell aktualisierte Emission mit dem letzten finanziell aktualisierten Eingang verrechnet usw. In diesem Beispiel wird eine Abrechnung zwischen 5b und 3b erstellt. Eine Anpassung von USD 14,00 wird an 3b vorgenommen, und die daraus resultierenden endgültigen Kosten werden USD 30,00 betragen.

Die folgende Abbildung zeigt die Auswirkungen des Lagermodells FIFO auf diese Buchungsserie an, wenn die Option **Physischen Wert einbeziehen** nicht verwendet wird.

![LIFO ohne die Option Physischen Wert einbeziehen.](./media/lifo-without-including-physical-value.png)

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

## <a name="lifo-with-the-include-physical-value-option"></a>LIFO mit der Option "Physischen Wert einbeziehen"

Wenn das Kontrollkästchen **Physikalischen Wert einbeziehen** für einen Artikel auf der Seite **Artikelmodellgruppen** markiert ist, verwendet das System sowohl physische als auch finanzielle Zugangstransaktionen, um die laufende durchschnittliche Kalkulation auszuführen. Falls zutreffend, passt das System auch die physisch aktualisierte Ausgabe-Transaktion an. Wenn das Kontrollkästchen **Physikalischen Wert einbeziehen** deaktiviert ist, nimmt der Bestandsabschluss, der das LIFO-Bestandsmodell verwendet, nur Abrechnungen für Transaktionen vor, die finanziell fortgeschrieben werden.

Die folgende Abbildung zeigt diese Buchungen an:

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
- 7\. Lagerabschluss wird vorgenommen. Auf der Grundlage der LIFO-Methode wird die erste finanziell aktualisierte Emission mit dem letzten finanziell aktualisierten Eingang verrechnet usw. In diesem Beispiel wird eine Abrechnung zwischen 3b und 5b erstellt. Eine Anpassung von USD 14,00 wird an 3b vorgenommen, und die daraus resultierenden endgültigen Kosten werden USD 30,00 betragen. Zusätzlich wird die Transaktion 6a an die Kosten der Transaktion für den Eingang von 4a angepasst. Diese Buchungen werden vom System nicht ausgeglichen, da der Zugang nur physisch, nicht aber wertmäßig aktualisiert wurde. Stattdessen wird nur eine Anpassung von USD 1,33 auf die physische Ausgabetransaktion gebucht, und die daraus resultierenden angepassten Kosten betragen USD 25,00.

Die folgende Abbildung zeigt die Auswirkungen des Lagermodells LIFO für diese Buchungsserie an, wenn die Option **Physischen Wert einbeziehen** verwendet wird.

![LIFO mit der Option Physischen Wert einbeziehen.](./media/lifo-with-included-physical-value.png)

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

## <a name="lifo-with-marking"></a>LIFO mit Markierung

Der Begriff "Markierung" bezeichnet ein Verfahren zum Verknüpfen (oder Markieren) einer Abgangsbuchung mit einer Zugangsbuchung. Eine Markierung kann entweder vor oder nach Ausführung der Buchung erfolgen. Durch die Verwendung einer Markierung lassen sich bei der Ausführung der Buchung oder des Lagerabschlusses die exakten Kosten des Lagers ermitteln. Beispiel: In der Kundendienstabteilung wurde der Eilauftrag eines wichtigen Debitors angenommen. Da es sich bei dieser Bestellung um eine Eilbestellung handelt, müssen Sie mehr für den Artikel bezahlen, um den Wunsch des Debitors zu erfüllen.

Sie müssen sicherstellen, dass sich die Kosten des Artikels im Bestand in der Marge oder den Kosten der verkauften Waren (COGS) für die Verkaufsrechnung widerspiegeln. Bei der Buchung der Bestellung erhält das Lager einen Zugang in Höhe von EUR 120,00 (Kosten). Wird dieses Auftragsdokument vor der Buchung des Lieferscheins oder der Rechnung für die Bestellung markiert, beträgt der Wareneinsatz EUR 120,00 (statt der aktuellen laufenden Durchschnittskosten für den Artikel). Wird der Lieferschein oder die Rechnung des Auftrags gebucht, bevor die Markierung vorgenommen wird, erfolgt die Buchung des Wareneinsatzes (COGS) zum laufenden Durchschnittseinstandspreis.

Die Markierung der beiden Buchungen kann noch bis zur Ausführung des Lagerabschlusses nachgeholt werden.

Sie können vor der Ausführung der Buchung eine Abgangsbuchung für einen Zugang markieren. Sie können diese Markierung von einer Verkaufsauftragszeile auf der Seite **Verkaufsauftragsdetails** aus vornehmen, indem Sie **Bestand \> Markierung** auf dem Inforegister **Kaufauftragszeilen** auswählen. Sie können die offenen Zugangsbuchungen auf der Seite **Markierung** anzeigen.

Sie können auch nach der Buchung der Transaktion eine Abgangsbuchung für einen Zugang markieren. Sie können eine Abgangsbuchung für eine offene Zugangsbuchung für einen gelagerten Artikel aus einer gebuchten Lagerregulierungserfassung abgleichen oder markieren.

Die folgende Abbildung zeigt diese Buchungen an:

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
- 7\. Lagerabschluss wird vorgenommen. Basierend auf dem Markierungsprinzip, das die LIFO-Methode verwendet, werden die markierten Transaktionen miteinander verrechnet. In diesem Beispiel wird 3b gegen 2b abgerechnet und eine Korrektur von 6,00 USD auf 3b gebucht, um den Wert auf 22,00 USD zu bringen. In diesem Beispiel werden keine weiteren Abrechnungen vorgenommen, da der Abschluss nur Abrechnungen für finanziell aktualisierte Transaktionen erstellt.

Im neuen laufenden Durchschnittseinstandspreis ist der Durchschnitt der wertmäßig und physisch aktualisierten Buchungen in Höhe von EUR 27,50 berücksichtigt.

Die folgende Abbildung gibt Aufschluss über die Auswirkungen des LIFO-Lagermodells auf diese Reihe von Buchungen, die bei markierten Ab- und Zugängen anfallen.

![LIFO mit Markierung.](./media/lifo-with-marking.png)

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
- Abrechnungen und Markierungen, die durch Bestandsabschluss durchgeführt werden, werden durch rote diagonal gestrichelte Pfeile dargestellt, die von einem Eingang zu einem Ausgang führen.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
