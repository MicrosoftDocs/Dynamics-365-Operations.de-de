---
title: Lagerchargen zusammenführen
description: Dieses Thema enthält Informationen, wie zwei oder mehr Lagerchargen in einer zusammengeführte Charge konsolidiert werden.
author: pjacobse
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventBatchJournalListPage, InventBatchJournalMerge
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 39782
ms.assetid: 07c5e98b-10fd-4f5c-b471-41d2150f47b0
ms.search.region: Global
ms.author: pjacobse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 83d969fcc59af87da3921225974ebc2ae41d9fa1
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250989"
---
# <a name="merge-inventory-batches"></a>Lagerchargen zusammenführen

[!include [banner](../includes/banner.md)]

Dieses Thema enthält Informationen, wie zwei oder mehr Lagerchargen in einer zusammengeführte Charge konsolidiert werden.

Wenn Sie Chargen zusammenführen, können Berechnungen dabei helfen, die Merkmale und die Chargenattribute der zusammengeführten Charge zu optimieren. Nachdem Sie die Quellchargen ausgewählt haben, können Sie die zusammengeführte Charge prüfen und ändern, bevor Sie sie buchen. Sie können auch die Chargenzusammenführung in eine Lagererfassung zur Genehmigung übertragen. Der Bestand kann direkt aus der Lagererfassung reserviert oder gebucht werden. Wenn Sie eine zusammengeführte Charge buchen, wird der Bestand für die Quellchargen und die zusammengeführte Charge angepasst.

## <a name="are-there-any-prerequisites"></a>Gibt es Vorbedinguungen?
Ja, gibt es mehrere Dinge, die Sie einrichten müssen, bevor Sie die Zusammenführungschargentools verwenden können. Die Vorbedingungen werden in der folgenden Tabelle näher erläutert.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Seite</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Journale, Lager</td>
<td>Sie müssen einen Journalname des Tpys Stücklisten erstellen, das standardmäßig verwendet wird, wenn Sie Chargenzusammenführungen in Bestandserfassungen buchen. Optional aber empfohlen: Sie können angeben, dass Reservierungen automatisch vorgenommen werden, wenn die Chargenzusammenführung in die Bestandserfassung übertragen wird. Andernfalls besteht ein Risiko, dass der verfügbare Bestand nach der Einrichtung und Buchung der Chargenzusammenführungsdetails geändert wird. Um automatische Reservierungen für die Erfassung zu aktivieren, wählen Sie im Feld <strong><strong>Reservierung</strong></strong> den Wert <strong>Automatisch</strong> aus.</td>
</tr>
<tr class="even">
<td>Parameter für Lager- und Lagerortverwaltung</td>
<td>Sie müssen den Standarderfassungsnamen für die Lagererfassung angeben.</td>
</tr>
<tr class="odd">
<td>Freigegebene Produkte</td>
<td>Die empfohlenen Einstellungen für den Artikel sind wie folgt:
<ul>
<li>Um Chargennummern für zusammengeführte Chargen automatisch zu generieren, müssen Sie das freigegebene Produkt einer Chargennummerngruppe zuweisen. Sie können eine Chargennummer auch manuell eingeben, wenn Sie eine zusammengeführte Charge erstellen, oder wählen Sie eine vorhandene Chargennummer. Wenn Sie eine vorhandene Chargennummer auswählen, müssen Sie sicherstellen, dass die ausgewählte Charge in keine Bestandstransaktion einbezogen wurde.</li>
<li>Wenn Sie Haltbarkeits- oder Mindesthaltbarkeits-Datumsangaben für das freigegebene Produkt verwenden, werden die Datumsangaben für eine zusammengeführte Charge basierend auf der Auswahl im Feld <strong>Datumsberechnung für Chargenzusammenführung</strong> berechnet. Die folgenden Optionen sind verfügbar:
<ul>
<li><strong>Frühester Zeitpunkt</strong> - Die Berechnung basiert auf dem frühesten Datum, das für eine Quellcharge angegeben wird, die für die Chargenzusammenführung ausgewählt ist.</li>
<li><strong>Spätester Zeitpunkt</strong> - Die Berechnung basiert auf dem spätesten Datum, das für eine Quellcharge angegeben wird, die für die Chargenzusammenführung ausgewählt ist.</li>
<li><strong>Manuell</strong> - Es wird keine Berechnung vorgenommen. Wenn ein Datum für alle Quellchargen gleich ist, wird ein Datum vorgeschlagen. Dieses Datum kann geändert werden. Wenn das Datum auf den Quellchargen nicht gleich ist, können Sie es manuell eingeben.</li>
</ul></li>
</ul></td>
</tr>
<tr class="even">
<td>Chargennummerngruppe</td>
<td>Optional: Um eine Chargennummer zu generieren, wenn Sie eine zusammengeführte Charge erstellen, müssen Sie dem freigegebenen Produkt eine Chargennummerngruppe zuweisen. Andernfalls können Sie eine Chargennummer manuell eingeben.</td>
</tr>
</tbody>
</table>

## <a name="when-might-i-want-to-merge-batches-of-inventory"></a>Wann würde ich Bestandschargen zusammenführen wollen?
Die folgenden Beispiele sind Szenarien, in denen es sinnvoll sein kann, Chargen zusammenzuführen.

-   Thomas geht durch das Lager und stellt fest, dass mehrere Chargen desselben Artikels in geringen Mengen vorhanden sind. Er erwartet, mehrere neue Lieferungen zu erhalten, und als er realisiert, dass er Bodenfläche freimachen kann, indem er die einzelnen Mengen in einer neuen Charge zusammenführt.
-   Thomas erhält Bestand und möchte die neue Charge mit einer bereits vorhandenen zusammenfassen, um den Chargenattributwert der bestehenden Charge zu verbessern. Dadurch erstellen Sie einen neue Charge.

## <a name="can-i-merge-batches-across-sites-and-legal-entities"></a>Kann ich Chargen standort- und juristische Personen übergreifend zusammenführen?
Nein, können Sie nur Chargen zusammenführen, die die gleichen Standort- und Lagerortlagerdimensionen einer juristischen Personen haben. Allerdings können Sie eine anderen Lagerplatz- und Palettenkennung für die zusammengeführte Charge angeben.

## <a name="can-i-merge-partial-quantities"></a>Kann ich Teilmengen zusammenführen?
Nein, können Sie nur die gesamte Menge von Chargen zusammenführen. Die Chargenzusammenführungsfunktionen sind als eine Lagerbestandsfunktion und nicht als Produktionsfunktion vorgesehen.

## <a name="what-if-the-batches-have-different-batch-attribute-values"></a>Was ist, wenn die Chargen verschiedene Chargenattributwerte haben?
Wenn Sie die Quellchargen auswählen, um sie in der zusammengeführten Charge zu kombinieren, überprüft Supply Chain Management, ob alle Chargen die Merkmale oder Attributwerte aufweisen. Wenn ein Attributwert der gleiche ist, wird ein Wert für die zusammengeführte Charge vorgeschlagen. Dieser Wert kann geändert werden. Attributwerte, die nicht identisch sind, werden für die zusammengeführte Chargen nicht ausgefüllt, und Sie können diese Werte manuell eingeben. Wenn der Chargenattributtyp für den Attributwert eine ganze Zahl oder eine Bruchzahl ist und die Werte nicht identisch für alle Quellchargen sind, wird der Wert durch die Berechnung des gewichteten Durchschnitts ermittelt. Der berechnete Wert wird auf das nächsten Inkrement auf- oder abgerundet. Wenn der Wert für eine Quellcharge leer ist, werden die Charge und die Menge nicht in die Berechnung einbezogen. **Beispiel** Das folgende Beispiel zeigt eine Berechnung des gewichteten Durchschnitts für eine zusammengeführte Charge. Zwei der Quellchargen haben einen leerer Wert für einen Chargenattributtyp, der eine ganze Zahl ist. Folgendes Attribut wird den Quellchargen zugewiesen.

| Attribut | Minimum | Inkrement | Maximum |
|-----------|---------|-----------|---------|
| Klasse     | 3       | 3         | 30      |

Die Quellchargen haben folgende Attributwerte für das Chargenattribut **Klasse**.

| Stapel | Menge | Attribut | Attributwert |
|-------|----------|-----------|-----------------|
| B1    | 10       | Klasse     | Leer           |
| B2    | 15       | Klasse     | 15              |
| B3    | 20       | Klasse     | 20              |
| B4    | 25       | Klasse     | Leer           |
| B5    | 30       | Klasse     | 25              |

Wenn Sie diese Chargen als Quellchargen hinzufügen, werden die folgenden Werte der zusammengeführten Charge zugewiesen.

| Stapel | Menge | Attribut | Attributwert |
|-------|----------|-----------|-----------------|
| B6    | 100      | Klasse     | 21              |

Die Werte und Mengen für Chargen B1 und B4 werden nicht in die Berechnung des gewichteten Durchschnitts einbezogen. Daher wird der Wert für die zusammengeführte Charge wie folgt berechnet.

| Wert | Menge (Gewicht)                              | Relatives Gewicht | Relatives Gewicht × Wert                                               |
|-------|------------------------------------------------|-----------------|-----------------------------------------------------------------------|
| 15    | 15                                             | 0.230769231     | 3.461538462                                                           |
| 20    | 20                                             | 0.307692308     | 6.153846154                                                           |
| 25    | 30                                             | 0.461538462     | 11.53846154                                                           |
|       | **Summe:** 65, die Summe der Gewichte |                 | **Summe:** 21,5384615, gerundet auf 21 (das nächste Inkrement). |

## <a name="what-if-the-batches-have-different-batch-dates"></a>Was ist, wenn die Chargen unterschiedliche Chargendaten haben?
Wenn die Chargen verschiedene Chargendatumsangaben haben, werden einige der Daten anhand der Werte in der Gruppe **Chargendatumsangaben** auf dem Inforegister **Zusammengeführte Charge** der Seite **Chargenzusammenführung** berechnet. Das System berechnet die Feldwerte unter Verwendung der Gruppe **Chargendatumsangaben**. Zu diesen Werten zählen das Herstellungs-, Ablaufs-, Haltbarkeits- und Mindesthaltbarkeits-Datum. Die Datumsangaben werden nach den Einstellungen für den Artikel auf der Seite **Details für freigegebene Produkte** in der Feldgruppe **Artikeldaten** berechnet. Sie können die Werte ändern oder manuell eingeben. Bei allen anderen Datumsangaben wird keine Berechnung vorgenommen. Dasselbe Prinzip wird für Chargenattributwerte verwendet. Wenn ein Datum das gleiche für alle Quellchargen ist, wird dieses Datum für die zusammengeführte Charge vorgeschlagen. Wenn das Datum nicht das gleiche für alle Quellchargen ist, ist das Datum auf der zusammengeführten Charge leer und Sie können es manuell eingeben.

## <a name="what-if-the-dimensions-are-different-on-the-batches-that-i-want-to-merge"></a>Was ist, wenn die Dimensionen auf den Chargen, die ich zusammenführen möchte, unterschiedlich sind?
Im Folgenden wird gezeigt, wie Produktdimensionen, Rückverfolgungsangaben und Lagerdimensionen gehandhabt werden:

-   **Produktdimensionen** - Alle Produktdimensionen für den ausgewählten Artikel müssen gleich sein. Sie können keine Chargen über Produktdimensionen hinweg zusammenführen.
-   **Rückverfolgungsangaben** - Eine neue Chargennummer wird automatisch generiert, wenn eine Chargennummerngruppe für den Artikel angegeben ist. Wenn eine Chargennummerngruppe nicht einem Artikel zugeordnet ist, können Sie eine vorhandene Charge auswählen oder die Nummer manuell eingeben. Seriennummern werden aus der Quellcharge in die Lagererfassungspositionen für die zusammengeführte Charge übertragen.
-   **Lagerdimensionen** - Die Standort- und Lagerortlagerdimensionen müssen identisch für alle Quellchargen und die zusammengeführte Charge sein. Allerdings können Sie eine neuen Lagerplatz- und Palettenkennung für die zusammengeführte Charge angeben.

## <a name="how-does-posting-work"></a>Wie funktioniert die Buchung?
Das Buchen geschieht auf zwei Arten, je nachdem, ob Sie einen Genehmigungsprozess für Erfassungen verwenden. Sie können die Schaltflächen **In Erfassung übertragen** und **Chargenzusammenführung buchen** verwenden, um die Chargenzusammenführung in eine Erfassung zu übertragen, wo sie geprüft und gebucht werden kann, oder die Chargenzusammenführung direkt buchen. Der wesentliche Unterschied zwischen den zwei Aktivitäten ist, dass eine Umlagerung in eine Erfassung nicht die Chargenzusammenführung bucht. Beide Aktivitäten erstellen eine neue Charge, wenn keine vorhandene Charge aktiviert ist, aktualisieren alle Chargendetails sowie -Attributwerte und erstellen eine Bestandserfassung.

-   **In Erfassung übertragen** - Überträgt die Chargenzusammenführungsdetails in eine neue Lagererfassung. Wenn Sie automatische Reservierungen eingerichtet haben, werden die Mengen in den Quellchargen reserviert. Die Details der Chargenzusammenführung können nicht geändert werden. Um die Chargenzusammenführung zu ändern, müssen Sie die Erfassung löschen. Die Erfassung kann als Aufgabe verwendet werden, die ein anderer Mitarbeiter später ausführen muss. Die Reservierung der Chargenmenge in der Erfassungsposition ist geschützt. Diese Zuteilung ermöglicht einem Qualitätsplaner oder einem Lagerortleiter, Aufgaben für seine Mitarbeiter erstellen.
-   **Chargenzusammenführung buchen** - Direkte Buchung der Chargenzusammenführung. Diese Aktivität kann ausgeführt werden , nachdem die physische Zusammenführung erfolgt ist.

Sie können die Bestandserfassung für die Chargenzusammenführung auf der Listenseite **Alle Chargenzusammenführungen** genehmigen. Klicken Sie auf **Erfassung** &gt; **Buchen**. Nachdem eine Erfassung gebucht wurde, können Sie die Details in der zusammengeführten Charge nicht mehr ändern. Nachdem Sie eine Chargenzusammenführung zu einer Bestandserfassung übertragen haben, können Sie die Details nur ändern, wenn die Erfassung gelöscht wird.

## <a name="after-i-merged-a-catchweight-item-why-cant-i-see-the-catchweight-information-in-the-inventory-journal"></a>Warum kann ich, nachdem ich einen Artikelgewichtsartikel zusammengeführt habe, die Artikelgewichtsinformationen in der Lagererfassung nicht anzeigen?
Sie können Chargen von Artikelgewichtsartikeln ebenso wie alle anderen Artikel zusammenführen. Allerdings werden die Artikelgewichtsinformationen nicht in der Lagererfassung angezeigt. Es wird empfohlen, die Artikelgewichtsinformationen zu prüfen, bevor Sie die Chargenzusammenführung in die Bestandserfassung übertragen.
