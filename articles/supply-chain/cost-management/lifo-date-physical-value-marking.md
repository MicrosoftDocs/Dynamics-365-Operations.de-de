---
title: LIFO-Datum mit physischem Wert und Markierung
description: Last in, First out Date (LIFO-Datum) ist ein Bestandsmodell, das auf dem LIFO-Prinzip basiert. Abgänge aus dem Lager werden mit den neuesten Zugängen im Lager auf der Grundlage des Datums der Lagerbuchung abgeglichen. Durch die Verwendung des LIFO-Datums wird die Ausgabe mit allen Eingängen verrechnet, die nach dem Ausgabedatum erfolgen, wenn es vor der Ausgabe keinen Eingang gibt. Mehrere Abgänge am gleichen Datum können in der Reihenfolge "Neuester Abgang, neuester Zugang" ausgeglichen werden.
author: AndersGirke
ms.date: 02/21/2022
ms.topic: article
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 51592
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f6f5f447724ace473bece3007a96c4b56e90a908
ms.sourcegitcommit: addae271ddfc5a8b0721c23337f69916153db4cd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/21/2022
ms.locfileid: "8330275"
---
# <a name="lifo-date-with-physical-value-and-marking"></a>LIFO-Datum mit physischem Wert und Markierung

[!include [banner](../includes/banner.md)]

Last in, first out date (LIFO-Datum) ist eine Methode zur Verwaltung und Bewertung von Beständen, bei der die zuletzt produzierten oder erworbenen Bestände zuerst verkauft, verwendet oder entsorgt werden. Während des Bestandsabschlusses in Microsoft Dynamics 365 Supply Chain Management erstellt das System Abrechnungen, bei denen der letzte Zugang mit der ersten Ausgabe für jedes gegebene Datum abgeglichen wird, beginnend mit dem ältesten Datum zuerst, usw. Wenn Sie das LIFO-Datum (last in, first out date) Bestandsmodell verwenden, wird die Ausgabe mit allen Eingängen verrechnet, die nach dem Ausgabedatum erfolgen, wenn es vor der Ausgabe keinen Eingang gibt. Die Abrechnungen und das Abgleichsprinzip beruhen auf dem Finanzdatum der Transaktionen im Bestand. Wenn es mehrere Ausgaben am gleichen Tag gibt, werden sie in der Reihenfolge der letzten Ausgabe und des letzten Eingangs abgerechnet. Eine vorläufige Bewertung der Abrechnungen und Anpassungen kann durch Ausführen der Bestandsneuberechnung vorgenommen werden.

Sie können das LIFO-Datumsprinzip außer Kraft setzen, indem Sie Transaktionen im Bestand so markieren, dass ein bestimmter Element-Eingang mit einem bestimmten Ausgang verrechnet wird. Ein periodischer Bestandsabschluss ist erforderlich, wenn Sie das LIFO-Datumsbestandsmodell verwenden, um Abrechnungen zu erstellen und den Wert von Ausgaben nach dem LIFO-Prinzip anzupassen. Bis Sie den Bestandsabschlussprozess ausführen, werden Ausgabetransaktionen zum laufenden Durchschnitt bewertet, wenn die physischen und finanziellen Aktualisierungen erfolgt sind. Sofern Sie nicht die Markierung verwenden, wird der laufende Durchschnitt berechnet, wenn die physische oder finanzielle Aktualisierung ausgeführt wird.

Wir empfehlen einen periodischen Bestandsabschluss, wenn Sie das LIFO-Datum-Bestandsmodell verwenden.

Die folgenden Beispiele zeigen die Auswirkungen der Verwendung des LIFO-Datums in drei Konfigurationen:

- LIFO-Datum ohne die Option **Physikalischen Wert einbeziehen**
- LIFO-Datum mit der Option **Physikalischen Wert einbeziehen**
- LIFO-Datum mit Markierung

## <a name="lifo-date-without-the-include-physical-value-option"></a>LIFO-Datum ohne die Option Physikalischen Wert einbeziehen

In diesem Beispiel ist die Artikelmodellgruppe so konfiguriert, dass der physische Wert nicht einbezogen wird. Die folgende Abbildung zeigt diese Buchungen an:

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
- 7\. Lagerabschluss wird vorgenommen. Basierend auf der LIFO-Datum-Methode wird die erste finanziell aktualisierte Ausgabe gegen den letzten finanziell aktualisierten Eingang ab dem ersten Datum verrechnet, und so weiter. In diesem Beispiel wird eine Abrechnung zwischen 3b und 2b erstellt. Eine Anpassung von USD 6,00 wird an 3b vorgenommen, und die daraus resultierenden endgültigen Kosten werden USD 22,00 betragen.

Die folgende Abbildung zeigt die Auswirkungen des LIFO-Datumsbestandsmodells, wenn die Option **Physikalischen Wert einbeziehen** nicht verwendet wird.

![LIFO-Datum ohne die Option Physikalischen Wert einbeziehen.](media/lifo-date-without-include-physical-value.png)

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

## <a name="lifo-date-with-the-include-physical-value-option"></a>LIFO-Datum mit der Option Physischen Wert einbeziehen

Wenn das Kontrollkästchen **Physikalischen Wert einbeziehen** für einen Artikel auf der Seite **Artikelmodellgruppen** markiert ist, verwendet das System sowohl physische als auch finanzielle Zugangstransaktionen, um die laufende durchschnittliche Kalkulation auszuführen. Falls zutreffend, passt das System auch die physisch aktualisierte Ausgabe-Transaktion an. Wenn das Kontrollkästchen **Physikalischen Wert einbeziehen** deaktiviert ist, nimmt der Bestandsabschluss, der das LIFO-Datumsbestandsmodell verwendet, nur Abrechnungen mit Transaktionen vor, die finanziell aktualisiert werden.

In diesem Beispiel ist die Artikelmodellgruppe so konfiguriert, dass der physische Wert einbezogen wird. 

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
- 7\. Lagerabschluss wird vorgenommen. Basierend auf der LIFO-Datum-Methode wird die erste finanziell aktualisierte Ausgabe mit der letzten finanziell aktualisierten Einnahme für jedes Datum ab dem ersten Datum verrechnet, usw. In diesem Beispiel wird eine Abrechnung zwischen 2b und 3b erstellt. Eine Anpassung von USD 6,00 wird an 3b vorgenommen, und die daraus resultierenden endgültigen Kosten werden USD 22,00 betragen. Außerdem wird die Transaktion 6a an die Kosten der Quittungstransaktion von 5b angepasst. Das System wird diese Transaktionen nicht abrechnen, da der Bon zwar physisch, aber nicht finanziell aktualisiert wird. Stattdessen wird nur eine Anpassung von USD 6,33 auf die physische Ausgabetransaktion gebucht, und die daraus resultierenden angepassten Kosten betragen USD 30,00.

Die folgende Abbildung zeigt die Auswirkungen des LIFO-Lagermodells LIFO an, wenn die Option **Physischen Wert einbeziehen** verwendet wird.

![LIFO-Datum mit der Option Physikalischen Wert einbeziehen.](media/lifo-date-with-include-physical-value.png)

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

## <a name="lifo-date-with-marking"></a>LIFO-Datum mit Markierung

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
- 3c. Der finanzielle Bestandsabgang für 3b wird als finanzieller Bestandsabgang für 1b markiert.
- 4a. Physischer Lagerzugang für die Menge "1" zu jeweils EUR 25,00 (Kosten).
- 5a. Physischer Lagerzugang für die Menge "1" zu jeweils EUR 30,00 (Kosten).
- 5b. Wertmäßiger Lagerzugang für die Menge "1" zu jeweils EUR 30,00 (Kosten).
- 6a. Inventarabgang für eine Menge von 1 zu einem Einstandspreis von USD 23,00 (laufender Durchschnitt der finanziell gebuchten Transaktionen)
- 7\. Lagerabschluss wird vorgenommen. Basierend auf dem Markierungsprinzip, das die LIFO-Datumsmethode verwendet, werden die markierten Transaktionen gegeneinander abgerechnet. In diesem Beispiel wird 3b gegen 1b abgerechnet und eine Korrektur von -6,00 USD auf 3b gebucht, um den Wert auf 10,00 USD zu bringen. In diesem Beispiel werden keine weiteren Abrechnungen vorgenommen, da der Abschluss nur Abrechnungen für finanziell aktualisierte Transaktionen erstellt.

Die folgende Abbildung zeigt die Auswirkungen des LIFO-Datumsbestandsmodells, wenn die Markierung zwischen Ausgaben und Eingängen verwendet wird. 

![LIFO-Datum mit Markierung.](media/lifo-date-with-marking.png)

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
