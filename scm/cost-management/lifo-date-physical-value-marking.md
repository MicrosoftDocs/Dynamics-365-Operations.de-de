---
title: LIFO-Datum mit physischem Wert und Markierung
description: "Beim LIFO-Datum (Last In, First Out) handelt es sich um ein Lagermodell, das auf dem LIFO-Prinzip basiert. Abgänge aus dem Lager werden mit den neuesten Zugängen im Lager auf der Grundlage des Datums der Lagerbuchung abgeglichen. Bei Verwendung des LIFO-Datums wird der Abgang mit beliebigen Zugängen ausgeglichen, die nach dem Datum des Artikelabgangs liegen, wenn vor dem Abgang kein Zugang zu verzeichnen ist. Mehrere Abgänge am gleichen Datum können in der Reihenfolge &quot;Neuester Abgang, neuester Zugang&quot; ausgeglichen werden."
author: YuyuScheller
manager: AnnBe
ms.date: 2016-02-23 23 - 07 - 14
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 51592
ms.assetid: d9f13274-3268-444f-85c8-b686fd39286d
ms.search.region: Global
ms.search.industry: Retail
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 7a2430de79cd56441c8101336992d4a10889a126
ms.lasthandoff: 03/29/2017


---

# <a name="lifo-date-with-physical-value-and-marking"></a>LIFO-Datum mit physischem Wert und Markierung

Beim LIFO-Datum (Last In, First Out) handelt es sich um ein Lagermodell, das auf dem LIFO-Prinzip basiert. Abgänge aus dem Lager werden mit den neuesten Zugängen im Lager auf der Grundlage des Datums der Lagerbuchung abgeglichen. Bei Verwendung des LIFO-Datums wird der Abgang mit beliebigen Zugängen ausgeglichen, die nach dem Datum des Artikelabgangs liegen, wenn vor dem Abgang kein Zugang zu verzeichnen ist. Mehrere Abgänge am gleichen Datum können in der Reihenfolge "Neuester Abgang, neuester Zugang" ausgeglichen werden. 

Bei Verwendung des LIFO-Lagermodells (Last In, First Out) wird der Abgang mit beliebigen Zugängen ausgeglichen, die nach dem Datum des Artikelabgangs liegen, wenn vor dem Abgang kein Zugang zu verzeichnen ist. Mehrere Abgänge am gleichen Datum können in der Reihenfolge "Neuester Abgang, neuester Zugang" ausgeglichen werden. Wenn Sie das LIFO-Datum verwenden, müssen Sie die LIFO-Datumsregel nicht verwenden. Stattdessen können Lagerbuchungen markiert werden, damit ein bestimmter Artikelzugang mit einem bestimmten Abgang ausgeglichen wird. Es wird empfohlen, einen regelmäßigen Lagerabschluss durchzuführen, wenn Sie das Lagermodell "LIFO-Datum" verwenden. In den folgenden Beispielen werden die Auswirkungen der Verwendung des LIFO-Datums anhand von drei unterschiedlichen Konfigurationen veranschaulicht:

-   LIFO-Datum ohne die Option **Physischen Wert einbeziehen**
-   LIFO-Datum mit der Option **Physischen Wert einbeziehen**
-   LIFO-Datum mit Markierung

## <a name="lifo-date-without-the-include-physical-value-option"></a>LIFO-Datum ohne die Option "Physischen Wert einbeziehen"
In diesem Beispiel ist die Artikelmodellgruppe so konfiguriert, dass der physische Wert nicht einbezogen wird. Die folgende Abbildung zeigt diese Buchungen an:

-   1a. Physischer Lagerzugang für die Menge "1" zu jeweils EUR 10,00 (Kosten).
-   1b. Wertmäßiger Lagerzugang für die Menge "1" zu jeweils EUR 10,00 (Kosten).
-   2a. Physischer Lagerzugang für die Menge "1" zu jeweils EUR 20,00 (Kosten).
-   2b. Wertmäßiger Lagerzugang für die Menge "1" zu jeweils EUR 20,00 (Kosten).
-   3a. Physischer Lagerzugang für die Menge "1" zu jeweils EUR 25,00 (Kosten).
-   4a. Physischer Lagerabgang für die Menge "1" zu einem Einstandspreis von EUR 15,00 (laufender Durchschnitt wertmäßig aktualisierter Buchungen).
-   4b. Wertmäßiger Lagerabgang für die Menge "1" zu einem Einstandspreis von EUR 15,00 (laufender Durchschnitt wertmäßig aktualisierter Buchungen).
-   5a. Physischer Lagerzugang für die Menge "1" zu jeweils EUR 30,00 (Kosten).
-   5b. Wertmäßiger Lagerzugang für die Menge "1" zu jeweils EUR 30,00 (Kosten).
-   6. Lagerabschluss wird vorgenommen. Der letzte wertmäßig aktualisierte Abgang wird auf Basis der Methode "LIFO-Datum" mit dem letzten wertmäßig aktualisierten Zugang nach Datum ausgeglichen. Für die Abgangsbuchung erfolgt eine Regulierung in Höhe von EUR 5,00. Diese Buchungen werden gegenseitig ausgeglichen.

Im neuen laufenden Durchschnittseinstandspreis ist der Durchschnitt der wertmäßig aktualisierten Buchungen in Höhe von EUR 15,00 berücksichtigt. Die folgende Abbildung zeigt die Auswirkungen des Lagermodells LIFO-Datum an, wenn die Option **Physischen Wert einbeziehen** nicht verwendet wird. ![LIFO-Datum mit "Physischen Wert einbeziehen](./media/lifodatewithoutincludephysicalvalue.gif) **Diagrammschlüssel**

-   Lagerbuchungen sind durch vertikale Pfeile dargestellt.
-   Zugänge zum Lager sind als vertikale Pfeile über der Zeitachse dargestellt.
-   Abgänge aus dem Lager sind als vertikale Pfeile unter der Zeitachse dargestellt.
-   Über (oder unter) den einzelnen vertikalen Pfeil ist der Wert der Lagerbuchung im Format Quantity@Unitpriceangegeben.
-   Ein in Klammern gesetzter Lagerbuchungswert weist darauf hin, dass die Lagerbuchung physisch in das Lager gebucht wurde.
-   Ein nicht in Klammern gesetzter Lagerbuchungswert weist darauf hin, dass die Lagerbuchung wertmäßig in das Lager gebucht wurde.
-   Jede neue Zugangs- oder Abgangsbuchung wird mit einer neuen Beschriftung versehen.
-   Each vertical arrow is labeled with a sequential identifier, such as *1a*. Mit dieser Kennung wird die Reihenfolge der Lagerbuchungen auf der Zeitachse angegeben.
-   Lagerabschlüsse sind durch eine vertikale rote gestrichelte Linie und die Beschriftung *Lagerabschluss* gekennzeichnet.
-   Ein durch einen Lagerabschluss vorgenommener Ausgleich ist durch rote diagonale gestrichelte Pfeile dargestellt, die von einem Zugang zu einem Abgang verlaufen.

## <a name="lifo-date-with-the-include-physical-value-option"></a>LIFO-Datum mit der Option "Physischen Wert einbeziehen"
Sie können das Feld **Physischen Wert einbeziehen** für einen Artikel auf der Seite **Lagersteuerungsgruppe** aktivieren. In diesem Fall verwendete das System physische und wertmäßige Zugangsbuchungen verwendet, um den laufenden Durchschnittseinstandspreis zu berechnen. Gegebenenfalls werden auch Regulierungen an der physisch aktualisierten Abgangsbuchung vorgenommen. Ist das Kontrollkästchen **Physischen Wert einbeziehen** deaktiviert, werden bei einem Lagerabschluss mit dem Lagermodell "LIFO-Datum" lediglich die Transaktionen ausgeglichen, die wertmäßig aktualisiert sind. In diesem Beispiel ist die Artikelmodellgruppe so konfiguriert, dass der physische Wert einbezogen wird. Die folgende Abbildung zeigt diese Buchungen an:

-   1a. Physischer Lagerzugang für die Menge "1" zu jeweils EUR 10,00 (Kosten).
-   1b. Wertmäßiger Lagerzugang für die Menge "1" zu jeweils EUR 10,00 (Kosten).
-   2a. Physischer Lagerzugang für die Menge "1" zu jeweils EUR 20,00 (Kosten).
-   2b. Wertmäßiger Lagerzugang für die Menge "1" zu jeweils EUR 20,00 (Kosten).
-   3a. Physischer Lagerzugang für die Menge "1" zu jeweils EUR 25,00 (Kosten).
-   4a. Physischer Lagerabgang für die Menge "1" zu einem Einstandspreis von EUR 18,33 (laufender Durchschnitt wertmäßig aktualisierter Buchungen).
-   4b. Wertmäßiger Lagerabgang für die Menge "1" zu einem Einstandspreis von jeweils EUR 18,33 (laufender Durchschnitt wertmäßig aktualisierter Buchungen).
-   5a. Physischer Lagerzugang für die Menge "1" zu jeweils EUR 30,00 (Kosten).
-   5b. Wertmäßiger Lagerzugang für die Menge "1" zu jeweils EUR 30,00 (Kosten).
-   6. Lagerabschluss wird vorgenommen. Der letzte aktualisierte Abgang wird auf Basis der Methode "LIFO-Datum" mit dem letzten aktualisierten Zugang nach Datum reguliert oder ausgeglichen. Diese Buchungen werden nicht gegenseitig ausgeglichen, da die wertmäßige Zugangsbuchung mittels einer physischen Aktualisierungsbuchung reguliert wird. Stattdessen wird für die Abgangsbuchung lediglich eine Regulierung in Höhe von EUR 6,67 vorgenommen.

Im neuen laufenden Durchschnittseinstandspreis ist der Durchschnitt der wertmäßig aktualisierten Buchungen in Höhe von EUR 20,00 berücksichtigt. Die folgende Abbildung zeigt die Auswirkungen des LIFO-Lagermodells LIFO an, wenn die Option **Physischen Wert einbeziehen** verwendet wird. ![LIFO-Datum mit "Physischen Wert einbeziehen](./media/lifodatewithincludephysicalvalue.gif) **Diagrammschlüssel**

-   Lagerbuchungen sind durch vertikale Pfeile dargestellt.
-   Zugänge zum Lager sind als vertikale Pfeile über der Zeitachse dargestellt.
-   Abgänge aus dem Lager sind als vertikale Pfeile unter der Zeitachse dargestellt.
-   Über (oder unter) den einzelnen vertikalen Pfeil ist der Wert der Lagerbuchung im Format Quantity@Unitpriceangegeben.
-   Ein in Klammern gesetzter Lagerbuchungswert weist darauf hin, dass die Lagerbuchung physisch in das Lager gebucht wurde.
-   Ein nicht in Klammern gesetzter Lagerbuchungswert weist darauf hin, dass die Lagerbuchung wertmäßig in das Lager gebucht wurde.
-   Jede neue Zugangs- oder Abgangsbuchung wird mit einer neuen Beschriftung versehen.
-   Each vertical arrow is labeled with a sequential identifier, such as *1a*. Mit dieser Kennung wird die Reihenfolge der Lagerbuchungen auf der Zeitachse angegeben.
-   Lagerabschlüsse sind durch eine vertikale rote gestrichelte Linie und die Beschriftung *Lagerabschluss* gekennzeichnet.
-   Ein durch einen Lagerabschluss vorgenommener Ausgleich ist durch rote diagonale gestrichelte Pfeile dargestellt, die von einem Zugang zu einem Abgang verlaufen.

## <a name="lifo-date-with-marking"></a>LIFO-Datum mit Markierung
Markierung ist ein Prozess, der zum Verknüpfen (oder Markieren, einer Abgangsbuchung mit einer Zugangsbuchung. Eine Markierung kann entweder vor oder nach Ausführung der Buchung erfolgen. Durch die Verwendung einer Markierung lassen sich bei der Ausführung der Buchung oder des Lagerabschlusses die exakten Kosten des Lagers ermitteln. Beispiel: In der Kundendienstabteilung wurde der Eilauftrag eines wichtigen Debitors angenommen. Da es sich bei diesem Auftrag um einen Eilauftrag handelt, müssen Sie für diesen Artikel einen höheren Preis bezahlen, um den Wunsch des Debitors erfüllen zu können. Deshalb müssen Sie sicherstellen, dass bei dieser Auftragsrechnung die Kosten für diesen Lagerartikel in der Gewinnspanne bzw. im Wareneinsatz (COGS/cost of goods sold) berücksichtigt werden. Bei der Buchung des Auftrags erhält das Lager einen Zugang in Höhe von EUR 120,00 (Kosten). Wird dieses Auftragsdokument vor der Buchung des Lieferscheins oder der Rechnung für die Bestellung markiert, beträgt der Wareneinsatz EUR 120,00 (statt der aktuellen laufenden Durchschnittskosten für den Artikel). Wird der Lieferschein oder die Rechnung des Auftrags gebucht, bevor die Markierung vorgenommen wird, erfolgt die Buchung des Wareneinsatzes (COGS) zum laufenden Durchschnittseinstandspreis. Die Markierung der beiden Buchungen kann noch bis zur Ausführung des Lagerabschlusses nachgeholt werden. Beispiel: Eine Zugangsbuchung wird für eine Abgangsbuchung markiert. In diesem Fall wird die Bewertungsmethode, die in der Artikelmodellgruppe des Artikels definierte und das System diese Buchungen ausgeglichen gegeneinander ignoriert. Sie können vor der Ausführung der Buchung eine Abgangsbuchung für einen Zugang markieren. Dies kann von einer Auftragsposition auf der Seite **Auftragsdetails** aus erfolgen. Sie können die offenen Zugangsbuchungen auf der Seite **Markierung** anzeigen. Sie können auch nach der Buchung der Transaktion eine Abgangsbuchung für einen Zugang markieren. Sie können eine Abgangsbuchung für eine offene Zugangsbuchung für einen gelagerten Artikel aus einer gebuchten Lagerregulierungserfassung abgleichen oder markieren. Die folgende Abbildung zeigt diese Buchungen an:

-   1a. Physischer Lagerzugang für die Menge "1" zu jeweils EUR 10,00 (Kosten).
-   1b. Wertmäßiger Lagerzugang für die Menge "1" zu jeweils EUR 10,00 (Kosten).
-   2a. Physischer Lagerzugang für die Menge "1" zu jeweils EUR 20,00 (Kosten).
-   2b. Wertmäßiger Lagerzugang für die Menge "1" zu jeweils EUR 20,00 (Kosten).
-   3a. Physischer Lagerzugang für die Menge "1" zu jeweils EUR 25,00 (Kosten).
-   4a. Physischer Lagerzugang für die Menge "1" zu jeweils EUR 30,00 (Kosten).
-   4b. Wertmäßiger Lagerzugang für die Menge "1" zu jeweils EUR 30,00 (Kosten).
-   5a. Physischer Lagerabgang für die Menge "1" zu einem Einstandspreis von jeweils EUR 21,25 (laufender Durchschnitt wertmäßig und physisch aktualisierter Buchungen).
-   5b. Wertmäßiger Lagerabgang für die Menge "1" wird für den Lagerzugang aus 2b markiert, bevor die Buchung ausgeführt wird. Diese Buchung erfolgt zu einem Einstandspreis von jeweils EUR 20,00.
-   6a. Physischer Lagerabgang für die Menge "1" zu einem Einstandspreis von jeweils EUR 21,25.
-   7. Lagerabschluss wird vorgenommen. Da die wertmäßig aktualisierte FIFO-Buchung (First in, First out) für einen vorhandenen Zugang markiert ist, werden diese Buchungen gegenseitig ausgeglichen, und es ist keine Regulierung erforderlich.

Im neuen laufenden Durchschnittseinstandspreis ist der Durchschnitt der wertmäßig und physisch aktualisierten Buchungen in Höhe von EUR 27,50 berücksichtigt. Die folgende Abbildung gibt Aufschluss über die Auswirkungen der Auswahl des LIFO-Lagermodells mit markierten Ab- und Zugängen: ![LIFO-Datum mit Markierung](./media/lifodatewithmarking.gif) **Diagrammschlüssel**

-   Lagerbuchungen sind durch vertikale Pfeile dargestellt.
-   Zugänge zum Lager sind als vertikale Pfeile über der Zeitachse dargestellt.
-   Abgänge aus dem Lager sind als vertikale Pfeile unter der Zeitachse dargestellt.
-   Über (oder unter) den einzelnen vertikalen Pfeil ist der Wert der Lagerbuchung im Format Quantity@Unitpriceangegeben.
-   Ein in Klammern gesetzter Lagerbuchungswert weist darauf hin, dass die Lagerbuchung physisch in das Lager gebucht wurde.
-   Ein nicht in Klammern gesetzter Lagerbuchungswert weist darauf hin, dass die Lagerbuchung wertmäßig in das Lager gebucht wurde.
-   Jede neue Zugangs- oder Abgangsbuchung wird mit einer neuen Beschriftung versehen.
-   Each vertical arrow is labeled with a sequential identifier, such as *1a*. Mit dieser Kennung wird die Reihenfolge der Lagerbuchungen auf der Zeitachse angegeben.
-   Lagerabschlüsse sind durch eine vertikale rote gestrichelte Linie und die Beschriftung *Lagerabschluss* gekennzeichnet.
-   Ein durch einen Lagerabschluss vorgenommener Ausgleich ist durch rote diagonale gestrichelte Pfeile dargestellt, die von einem Zugang zu einem Abgang verlaufen.



