---
title: Bestandslisten
description: In diesem Thema wird beschrieben, wie Sie auf der Seite „Bestandsliste“ die vorhandenen Bestandsdaten überprüfen können. Es zeigt einige Möglichkeiten, wie die verschiedenen Filter- und Sortieroptionen zusammenarbeiten, und wie diese Optionen manchmal zu unerwarteten Ergebnissen führen können, wenn sie kombiniert werden.
author: sherry-zheng
manager: tfehr
ms.date: 07/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventOnhandItem, InventOnHandItemListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-07-07
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 275a37cd76715ab9909e057ec759c66c4f9c617b
ms.sourcegitcommit: 8cbaeb6443ce47a4c4bc02b5e1a1212eb0056b38
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/22/2020
ms.locfileid: "3829848"
---
# <a name="inventory-on-hand-list"></a>Bestandslisten

[!include [banner](../includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie auf der Seite **Bestandsliste** die vorhandenen Bestandsdaten überprüfen können. Es zeigt einige Möglichkeiten, wie die verschiedenen Filter- und Sortieroptionen zusammenarbeiten, und wie diese Optionen manchmal zu unerwarteten Ergebnissen führen können, wenn sie kombiniert werden.

## <a name="query-your-on-hand-inventory"></a>Abfrage Ihres verfügbaren Lagerbestands

Um die Bestandsverfügbarkeit zu überprüfen, gehen Sie zu **Bestandsverwaltung \> Anfragen und Berichte \> Bestandsliste**.

Die Seite **Bestandsliste** wird automatisch aktualisiert, wenn Buchungen im Bestand durchgeführt werden. Dabei kann es sich um geplante, physische und Finanzbuchungen handeln.

Verwenden Sie die folgenden Tools, um die gesuchten Produkte zu finden:

- Wählen Sie im Aktionsbereich [**Dimensionen**](#dimensions) aus, um ein Dialogfeld zu öffnen, wo Sie Spalten hinzufügen oder entfernen können, die im Raster **Verfügbar** angezeigt werden.
- Im [Bereich **Filter**](#filters-pane) geben Sie Werte für bestimmte Felder ein, um nur Datensätze anzeigen zu lassen, die diesen Werten entsprechen. Beachten Sie, dass Filter, die Sie hier festlegen, für Quelltabellen gelten, die möglicherweise später gemäß den von Ihnen ausgewählten Dimensionen aggregiert werden. Informationen darüber, wie sich dieses Verhalten auf Ihre Ergebnisse auswirken kann, finden Sie weiter unten unter [Beispiele](#examples).
- Im Bereich **Filter** wählen Sie **Anwenden**, um die Liste der passenden Lagerbestände im Raster **Verfügbar** zu generieren.
- Im Raster **Verfügbar** wählen Sie eine beliebige Spaltenüberschrift aus, die nach den Werten in dieser Spalte sortiert oder gefiltert werden soll. Ein QuickFilter am oberen Rand des Rasters enthält zusätzliche Filteroptionen. Diese Filter gelten für die Ergebnisse, nicht für die Quelltabellen. Informationen darüber, wie sich dieses Verhalten auf Ihre Ergebnisse auswirken kann, finden Sie weiter unten unter [Beispiele](#examples).

Für jeden passenden Artikel enthält das Raster **Verfügbar** die folgenden Spalten mit Bestandsinformationen.

| Spalte | Beschreibung |
|---|---|
| Physischer Bestand | Physische Menge, die in dem Bestand verfügbar ist. |
| Physisch reserviert | Die gesamte physisch reservierte Menge. |
| Physisch verfügbar | Die verfügbare (nicht reservierte) Menge, die im physischen Bestand verfügbar ist.<p>**Physisch verfügbar** ist ein berechnetes Feld. Der Wert entspricht dem Wert des **physischen Bestands** minus dem **Physisch reserviert**-Wert.</p> |
| Bei zusätzlichen Dimensionen physisch verfügbar | Die verfügbare physische Menge für alle Dimensionen, die im Raster angezeigt werden. |
| Insgesamt bestellt | Die Gesamtmenge, die in eingehenden Aufträgen enthalten ist oder die in verschiedenen Bestandserfassungen eine positive Menge aufweist. |
| In Auftrag | Die Gesamtmenge, die in ausgehenden Aufträgen enthalten ist oder die in verschiedenen Bestandserfassungen eine negative Menge aufweist. |
| Bestellt reserviert | Die gesamte für bestellte Zugänge reservierte Menge. Der Wert in diesem Feld gibt die Gesamtmenge der Artikel in ausgehenden Buchungen mit dem Status _Bestellt reserviert_ an. Artikel, die wie bestellt reserviert sind, sind physisch nicht im Bestand verfügbar. Daher können sie nicht direkt kommissioniert und geliefert werden. |
| Zur Reservierung verfügbar | Die insgesamt verfügbare Bestandsmenge, die reserviert werden kann.<p>**Hinweis:** Wenn das Kontrollkästchen **Bestellte Artikel reservieren** auf der Seite **Bestands- und Lagerverwaltungsparameter** aktiviert ist, enthält der Wert in diesem Feld erwartete Zugänge. Wenn das Kontrollkästchen deaktiviert ist, enthält der Wert keine erwarteten Zugänge.</p> |
| Verfügbare Menge | Die insgesamt verfügbare Menge.<p>**Verfügbare Menge** ist ein berechnetes Feld. Der Wert entspricht dem Wert **Physisch verfügbar** plus dem Wert **Insgesamt bestellt** minus dem Wert **In Auftrag**.</p> |

## <a name="apply-filters-to-find-the-records-that-youre-looking-for"></a><a name="filters-pane"></a>Mit Filtern die Datensätze finden, nach denen Sie suchen

Verwenden Sie den Bereich **Filter**, um die Bestandsliste zu filtern, sodass nur Datensätze enthalten sind, deren Feldwerte den Filterkriterien entsprechen. Legen Sie einen Filter wie folgt fest:

1. Suchen Sie im Bereich **Filter** das Feld, nach dem Sie filtern möchten.
2. Wählen Sie im Feld unter dem Namen des Zielfelds einen logischen Operator aus (z. B. *beginnt mit*, *gleich* oder *größer als*).
3. Geben Sie den Wert ein, nach dem Sie suchen.

> [!IMPORTANT]
> Die Seite **Bestandsliste** wird aus einer detaillierten Bestandstabelle zusammengestellt, die alle verfügbaren Dimensionen enthält. Die Liste auf dieser Seite ist jedoch eine Zusammenfassung. Daher können Zeilen aus der Quelltabelle kombiniert werden, indem Werte gemäß den angezeigten Dimensionen aggregiert werden.
>
> Die Filter, die Sie im Bereich **Filter** festlegen, gelten für die Quelltabelle und nicht für die aggregierte Liste. Dieses Verhalten kann manchmal zu unerwarteten Ergebnissen führen. Informationen darüber, wie sich dieses Verhalten auf Ihre Ergebnisse auswirken kann, finden Sie weiter unten unter [Beispiele](#examples).
> 
> Die [Filter, die im Raster bereitgestellt werden,](#grid-filters) *gelten jedoch* für die aggregierte Liste. Diese Filter enthalten sowohl QuickFilter am oberen Rand des Rasters als auch den Filter für jede Spaltenüberschrift.

Sie können die im Bereich **Filter** verfügbaren Filter wie folgt ändern:

- Um einen Filter aus dem Bereich zu entfernen, wählen Sie dessen **Schließen**-Schaltfläche (**X**).
- Um einen Filter hinzuzufügen, wählen Sie **Hinzufügen** oben im Bereich **Filter**. Das Dialogfeld **Filterfelder hinzufügen** enthält eine Liste der verfügbaren Felder. Außerdem werden Informationen über den Datentyp und die Tabelle für jedes Feld angezeigt. Verwenden Sie die Spaltenüberschriften, um die Liste nach Bedarf zu filtern und zu sortieren, und aktivieren Sie dann das Kontrollkästchen für jedes Feld, das Sie dem Bereich **Filter** hinzufügen möchten. Wenn Sie fertig sind, wählen Sie **Einfügen**, um Ihre Änderungen zu übernehmen.

## <a name="select-which-dimensions-to-show"></a><a name="dimensions"></a>Anzuzeigende Dimensionen auswählen

Die Dimensionen verraten mehr über jeden Artikel in der Bestandsliste und bieten Ihnen damit mehr Möglichkeiten, die Liste zu sortieren und zu filtern. Die Dimensionen, die Sie anzeigen lassen, wirken sich auch darauf aus, wie Zeilen auf der Seite **Bestandsliste** aggregiert werden. Diese Aggregation kann sich wiederum darauf auswirken, wie Zeilen aus den Quelltabellen in den angezeigten Ergebnissen kombiniert werden. Informationen darüber, wie sich dieses Verhalten auf Ihre Ergebnisse auswirken kann, finden Sie weiter unten unter [Beispiele](#examples).

Passen Sie die angezeigte Auswahl der Bestandsdimensionen wie folgt an.

1. Wählen Sie im Aktionsbereich **Dimensionen** aus.

    Das erscheinende Dialogfeld **Dimensionsanzeige** zeigt alle Dimensionen an.

2. Aktivieren Sie für alle in das Raster einzubeziehenden Dimensionen das entsprechende Kontrollkästchen.
3. Wenn Sie möchten, dass Ihre Auswahl beim nächsten Öffnen der Seite **Bestandsliste** standardmäßig verwendet wird, setzen Sie die Option **Einstellungen speichern** auf **Ja**. Wenn Sie diese Option auf **Nein** setzen, wird Ihre Auswahl nur während der aktuellen Sitzung verwendet. Daher wird beim nächsten Öffnen der Seite die aktuelle Standardauswahl verwendet.
4. Wählen Sie **OK** aus, um das Dialogfeld zu schließen und Ihre Änderung zu übernehmen.

## <a name="filter-on-the-output-of-the-inventory-on-hand-list"></a><a name="grid-filters"></a>Die Ausgabe der Bestandsliste filtern

Wählen Sie im Raster **Verfügbar** eine beliebige Spaltenüberschrift aus, die nach den Werten in dieser Spalte sortiert oder gefiltert werden soll. Ein QuickFilter am oberen Rand des Rasters enthält zusätzliche Filteroptionen. Diese Filter gelten für die Ergebnisse, nicht für die Quelltabellen. Informationen darüber, wie sich dieses Verhalten auf Ihre Ergebnisse auswirken kann, finden Sie weiter unten unter [Beispiele](#examples).

> [!NOTE]
> Sie können nicht nach allen Spalten filtern und sortieren. Die meisten Mengenspalten enthalten keine Sortier- und Filtersteuerelemente, da es sich um berechnete Felder handelt. Die Spalte **Verfügbar** ist eine Ausnahme.

## <a name="examples"></a><a name="examples"></a>Beispiele

Ihr System enthält eine detaillierte (nicht aggregierte) Bestandstabelle, in der die folgenden verfügbaren Bestände aufgeführt sind.

| Artikelnummer | Site | Lagerort | Physischer Bestand | Physisch verfügbar |
|---|---|---|---|---|
| IA0001 | 1 | 1 | 1 | 1 |
| IA0001 | 1 | 2 | 2 | 2 |
| IA0001 | 1 | 3 | 1 | 1 |

### <a name="scenario-1"></a>Szenario 1

Die Seite **Bestandsliste** ist so eingerichtet, dass die folgenden endgültigen Dimensionen angezeigt werden:

- Artikelnummer
- Site
- Lagerort

In dem Bereich **Filter** sind die folgenden Filterkriterien eingerichtet:

- **Artikelnummer** \| **ist genau** \| _IA0001_
- **Physisch verfügbar** \| **weniger als oder gleich** \| _1_

Hier ist die dazugehörige Ausgabe.

| Artikelnummer | Site | Lagerort | Physischer Bestand | Physisch verfügbar |
|---|---|---|---|---|
| IA0001 | 1 | 1 | 1 | 1 |
| IA0001 | 1 | 3 | 1 | 1 |

### <a name="scenario-2"></a>Szenario 2

Die Seite **Bestandsliste** ist so eingerichtet, dass die folgenden endgültigen Dimensionen angezeigt werden:

- Artikelnummer
- Site

In dem Bereich **Filter** sind die folgenden Filterkriterien eingerichtet:

- **Artikelnummer** \| **ist genau** \| _IA0001_
- **Physisch verfügbar** \| **weniger als oder gleich** \| _1_

Hier ist die dazugehörige Ausgabe.

| Artikelnummer | Site | Physischer Bestand | Physisch verfügbar |
|---|---|---|---|
| IA0001 | 1 | 2 | 2 |

Beachten Sie, dass die Einstellungen im Bereich **Filter** für die detaillierte (nicht aggregierte) Bestandstabelle gelten, die am Anfang dieses Abschnitts angezeigt wird. Daher findet das Kriterium **Physisch verfügbar** \| **weniger als oder gleich** \| _1_ zwei Zeilen aus dieser Tabelle (die erste und dritte Zeile, von denen jede einen Wert für **Physisch verfügbar** von _1_ hat). In diesem Szenario ist jedoch die Seite **Bestandsliste** nicht eingerichtet, um die **Lagerort**dimensionen anzuzeigen. Daher werden die beiden ursprünglichen Zeilen zu einer einzigen Zeile aggregiert, da beide in allen angezeigten Dimensionen identische Werte haben. Diese Zeile scheint das Filterkriterium zu verletzen, da der Wert **Physisch verfügbar** als _2_ angezeigt wird. Das Ergebnis ist jedoch korrekt, da die Einstellungen im Bereich **Filter** für die Quelltabelle und nicht für die aggregierte Tabelle gelten, die in der Tabelle auf der Seite **Verfügbar** angezeigt wird.
