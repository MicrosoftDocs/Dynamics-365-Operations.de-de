---
title: Beispiele und Logik für Inventarfäligkeitsberichte
description: In diesem Thema werden einige Beispiele vorgestellt, die zeigen, wie die Ergebnisse eines Inventaralterungsberichts interpretiert werden.
author: RichardLuan
manager: AnnBe
ms.date: 5/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: riluan
ms.search.validFrom: 2020-5-29
ms.dyn365.ops.version: ''
ms.openlocfilehash: 6c165599c11b84e4064a9303d8b1f59558fc6b9d
ms.sourcegitcommit: 6bf8602333191e5161ba3a9ceecf160c85ff7e79
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2020
ms.locfileid: "3484529"
---
# <a name="inventory-aging-report-examples-and-logic"></a>Beispiele und Logik für Inventarfäligkeitsberichte

[!include [banner](../includes/banner.md)]

In diesem Thema werden einige Beispiele vorgestellt, die zeigen, wie die Ergebnisse eines **Inventarfälligkeitsberichts** interpretiert werden. In diesem Bericht werden die verfügbaren Mengen- und Bestandswerte für einen ausgewählten Artikel oder eine Artikelgruppe in mehrere Periodenbereiche unterteilt. Dieses Thema zeigt auch die interne Logik des Berichts.

Die Beispiele in diesem Thema zeigen Ergebnisse, die auf einem Standard **Fälligkeit des Inventar** Berichts dargestellt werden. Im Allgemeinen empfehlen wir jedoch die Verwendung der Version [Speicherung von Inventarfälligkeitsberichten](inventory-aging-report-storage.md) dieses Berichts, insbesondere wenn Sie viele Artikel und Lager haben, die verarbeitet werden müssen. Durch die Speicherung von Inventarfälligkeitsberichten wird jeder von Ihnen erstellte Bericht gespeichert, die Ergebnisse als interaktive Seite und als Diagramm angezeigt und Sie können jeden gespeicherten Bericht exportieren.

## <a name="sample-data-that-is-used-in-these-examples"></a>Beispieldaten, die in diesen Beispielen verwendet werden

Die Beispiele in diesem Thema basieren auf den in diesem Abschnitt beschriebenen Beispieltransaktionsdaten für das Inventar.

### <a name="storage-dimension-setup"></a>Lagerdimensionsgruppe einrichten

Das Beispielsystem enthält die folgenden Einstellungen für die Speicherabmessungen.

| Name      | Aktiv | Physischer Bestand | Wertmäßiger Bestand |
|-----------|--------|--------------------|---------------------|
| Site      | Ja    | Ja                | Ja                 |
| Lagerort | Ja    | Ja                | Nr.                  |

### <a name="inventory-model"></a>Lagermodell

Für das Beispielsystem lautet das Bestandsmodell für die freigegebenen Produkte *FIFO*, und die **Selbstkostenpreis** Einstellung für das Bestandsmodell ist auf *Physischen Wert einschließen* festgelegt.

### <a name="inventory-transactions"></a>Lagerbuchungen

Das Beispielsystem enthält die folgenden Inventurtransaktionen für ein freigegebenes Produkt mit der Artikelnummer *1000*.

| Referenz      | Site | Lagerort | Zugang   | Abgang | Physisches Datum | Finanzdatum | Leistung | Betrag KORE | Phys. Einstandsbetrag |
|----------------|------|-----------|-----------|-------|---------------|----------------|----------|-------------|----------------------|
| Bestellung | 1    | 11        | Eingekauft |       | 15. März      | 15. März       | 10       | 1.000       | 1.000                |
| Bestellung | 2    | 21        | Eingekauft |       | 15. März      | 15. März       | 10       | 2,000       | 2,000                |
| Bestellung | 1    | 11        | Eingegangen  |       | April 15      |                | 5        |             | 375                  |
| Umlagerungsauftrag | 1    | 11        |           | Verkauft  | Mai 2         | Mai 2          | -5       | -458.33     | -458.33              |
| Umlagerungsauftrag | 1    | 12        | Eingekauft |       | Mai 2         | Mai 2          | 5        | 458.33      | 458.33               |
| Auftrag    | 1    | 12        |           | Verkauft  | Mai 3         | Mai 3          | -1       | -91.67      | -91.67               |

## <a name="how-quantities-and-amounts-in-each-period-bucket-are-calculated"></a>Wie Mengen und Beträge in jedem Periodenbereich berechnet werden

Mithilfe der in den vorherigen Abschnitten beschriebenen Beispieldaten können Sie einen Bericht **Alterung des Inventars** mit folgenden Einstellungen ausführen:

- **Stand:** *9. Mai 2020*
- **Seite:** *Aussicht*
- **Lagerort:** *Nein*
- **Artikelnummer:** *Gesamt*
- **Alterungsdauer:** Legen Sie dieses Feld fest, um monatliche Bereiche zu generieren.

In diesem Fall ähnelt der Inhalt des generierten Berichts dem folgenden Beispiel.

<table>
<thead>
<tr>
    <th rowspan="2">Artikelnummer</th>
    <th rowspan="2">Site</th>
    <th rowspan="2">Verfügbare Menge</th>
    <th rowspan="2">Verfügbarer Wert</th>
    <th rowspan="2">Lagerwertmenge</th>
    <th rowspan="2">Lagerwert</th>
    <th rowspan="2">Durchschnittliche Einheitenkosten</th>
    <th colspan="2">5/8/2020 - 5/1/2020</th>
    <th colspan="2">4/30/2020 - 4/1/2020</th>
    <th colspan="2">3/31/2020 - 3/1/2020</th>
</tr>
<tr>
    <th>P1: Menge</th>
    <th>P1:Betrag</th>
    <th>P2: Menge</th>
    <th>P2:Betrag</th>
    <th>P3: Menge</th>
    <th>P3:Betrag</th>
</tr>
</thead>
<tbody>
<tr>
    <td>1000</td>
    <td>1</td>
    <td>14</td>
    <td>1,283.33</td>
    <td>14</td>
    <td>1,283.33</td>
    <td>91.67</td>
    <td></td>
    <td></td>
    <td>5.00</td>
    <td>458.33</td>
    <td>9.00</td>
    <td>825.00</td>
</tr>
<tr>
    <td>1000</td>
    <td>2</td>
    <td>10</td>
    <td>2,000.00</td>
    <td>10</td>
    <td>2,000.00</td>
    <td>200.00</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td>10.00</td>
    <td>2,000.00</td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><strong>1000 Summen</strong></td>
    <td></td>
    <td><strong>24.00</strong></td>
    <td><strong>3,283.33</strong></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><strong>5.00</strong></td>
    <td><strong>458.33</strong></td>
    <td><strong>19</strong></td>
    <td><strong>2,825.00</strong></td>
</tr>
</tfoot>
</table>

Beachten Sie die folgenden Details in diesem Beispielbericht:

- Die Werte **Inventarwertmenge**, **Inventarwert** und **Durchschnittliche Stückkosten**, die im Bericht angezeigt werden, sind Werte für die Dimension des Finanzinventars (in diesem Fall **Seite**).

    Für Standort 1 enthält der Bericht beispielsweise die folgenden Informationen:

    - Den Wert **Inventarwertmenge** ist *14* (= 10 + 5 – 5 + 5 – 1).
    - Der Wert **Inventarwertmenge** ist *1,283.33* (= 1,000 + 375 – 458.33 + 458.33 – 91.67).
    - Der Wert **Durchschnittliche Stückkosten** ist *91,67*.
    - Der Wert **Lagerwert** und der Wert **Menge** in jedem Periodenbereich werden mithilfe vom Wert **Durchschnittliche Stückkosten** berechnet.

- Der Bericht ermittelt die verfügbare Menge für jeden Periodenbereich, indem die insgesamt erhaltene Bestandsmenge für jeden Periodenbereich zusammengefasst wird. Anschließend wird das Prinzip First In, First Out (FIFO)  angewendet, um die gesamte ausgegebene Menge abzuziehen, unabhängig vom verwendeten Bestandsmodell.

Wenn Sie denselben Bericht erneut ausführen, diesmal jedoch die Felder **Seite** und **Lagerort** auf *Anzeigen* festlegen, wird der neue Bericht dem folgenden Beispiel ähneln.

<table>
<thead>
<tr>
    <th rowspan="2">Artikelnummer</th>
    <th rowspan="2">Site</th>
    <th rowspan="2">Lagerort</th>
    <th rowspan="2">Verfügbare Menge</th>
    <th rowspan="2">Verfügbarer Wert</th>
    <th rowspan="2">Lagerwertmenge</th>
    <th rowspan="2">Lagerwert</th>
    <th rowspan="2">Durchschnittliche Einheitenkosten</th>
    <th colspan="2">5/8/2020 - 5/1/2020</th>
    <th colspan="2">4/30/2020 - 4/1/2020</th>
    <th colspan="2">3/31/2020 - 3/1/2020</th>
</tr>
<tr>
    <th>P1: Menge</th>
    <th>P1: Betrag</th>
    <th>P2: Menge</th>
    <th>P2: Betrag</th>
    <th>P3: Menge</th>
    <th>P3: Betrag</th>
</tr>
</thead>
<tbody>
<tr>
    <td>1000</td>
    <td>1</td>
    <td>11</td>
    <td>10</td>
    <td>916.67</td>
    <td>14</td>
    <td>1,283.33</td>
    <td>91.67</td>
    <td></td>
    <td></td>
    <td>5.00</td>
    <td>458.33</td>
    <td>5.00</td>
    <td>458.33</td>
</tr>
<tr>
    <td>1000</td>
    <td>1</td>
    <td>12</td>
    <td>4</td>
    <td>366.67</td>
    <td>14</td>
    <td>1,283.33</td>
    <td>91.67</td>
    <td>4.00</td>
    <td>366.67</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td>1000</td>
    <td>2</td>
    <td></td>
    <td>10</td>
    <td>2,000.00</td>
    <td>10</td>
    <td>2,000.00</td>
    <td>200.00</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td>10.00</td>
    <td>2,000.00</td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><strong>1000 Summen</strong></td>
    <td></td>
    <td></td>
    <td><strong>24.00</strong></td>
    <td><strong>3,283.33</strong></td>
    <td></td>
    <td></td>
    <td></td>
    <td><strong>4.00</strong></td>
    <td><strong>366.67</strong></td>
    <td><strong>5.00</strong></td>
    <td><strong>458.33</strong></td>
    <td><strong>15</strong></td>
    <td><strong>2,458.33</strong></td>
</tr>
</tfoot>
</table>

Diesmal ist Site 1 in zwei Zeilen unterteilt, eine für Lager 11 und eine für Lager 12. Aber die Werte **Inventarwertmenge**, **Inventarwert** und **Durchschnittliche Stückkosten**, die im Bericht angezeigt werden, sind gleich weil der **Lagerort** keine Finanzdimension ist.

Beachten Sie außerdem, dass die Mengenverteilung von Standort 1 unterschiedlich ist. In dem ersten Bericht, den Sie ausgeführt haben, hat das System den Transportauftrag ignoriert, der an derselben Site aufgetreten ist, und die Menge der Verkaufsrechnung vom Zeitraumbereich **31.03.2020 – 01.03.2020** in Site 1 abgezogen. Im neuen Bericht zieht das System jedoch die Menge der Verkaufsrechnung vom Zeitraumbereich **08.05.2020 – 01.05.2020** im Lager 12 ab.

## <a name="effects-of-inventory-closing"></a>Effekte der Bestandschließung

Wenn Sie das Inventar für Mai schließen und dann den vorherigen Bericht erneut ausführen, aber das Feld **Stand Datum** auf *31. Mai 2020* festlegen, werden Sie folgende Ergebnisse feststellen:

- Der **Bestandwert** und der Wert **Durchschnittliche Stückkosten** werden aktualisiert.
- Der **verfügbare Wert** und der Wert **Betrag** in jedem Periodenbereich werden entsprechend aktualisiert.

Der neue Bericht sieht ähnlich aus wie das folgende Beispiel.

<table>
<thead>
<tr>
    <th rowspan="2">Artikelnummer</th>
    <th rowspan="2">Site</th>
    <th rowspan="2">Lagerort</th>
    <th rowspan="2">Verfügbare Menge</th>
    <th rowspan="2">Verfügbarer Wert</th>
    <th rowspan="2">Lagerwertmenge</th>
    <th rowspan="2">Lagerwert</th>
    <th rowspan="2">Durchschnittliche Einheitenkosten</th>
    <th colspan="2">5/31/2020 - 5/1/2020</th>
    <th colspan="2">4/30/2020 - 4/1/2020</th>
    <th colspan="2">3/31/2020 - 3/1/2020</th>
</tr>
<tr>
    <th>P1: Menge</th>
    <th>P1: Betrag</th>
    <th>P2: Menge</th>
    <th>P2: Betrag</th>
    <th>P3: Menge</th>
    <th>P3: Betrag</th>
</tr>
</thead>
<tbody>
<tr>
    <td>1000</td>
    <td>1</td>
    <td>11</td>
    <td>10</td>
    <td>910.70</td>
    <td>14</td>
    <td>1,275.00</td>
    <td>91.07</td>
    <td>0,00</td>
    <td></td>
    <td>5.00</td>
    <td>455.36</td>
    <td>5.00</td>
    <td>455.36</td>
</tr>
<tr>
    <td>1000</td>
    <td>1</td>
    <td>12</td>
    <td>4</td>
    <td>364.29</td>
    <td>14</td>
    <td>1,275.00</td>
    <td>91.07</td>
    <td>4.00</td>
    <td>364.29</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td>1000</td>
    <td>2</td>
    <td></td>
    <td>10</td>
    <td>2,000.00</td>
    <td>10</td>
    <td>2,000.00</td>
    <td>200.00</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td>10.00</td>
    <td>2,000.00</td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><strong>1000 Summen</strong></td>
    <td></td>
    <td></td>
    <td><strong>24.00</strong></td>
    <td><strong>3,275.00</strong></td>
    <td></td>
    <td></td>
    <td></td>
    <td><strong>4.00</strong></td>
    <td><strong>364.29</strong></td>
    <td><strong>5.00</strong></td>
    <td><strong>455.36</strong></td>
    <td><strong>15</strong></td>
    <td><strong>2,455.36</strong></td>
</tr>
</tfoot>
</table>
