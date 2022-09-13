---
title: Rasterfunktionen
description: In diesem Artikel werden mehrere leistungsstarke Funktionen der Rastersteuerung beschrieben. Sie müssen die neue Rasterfunktion aktivieren, damit auf diese Fähigkeiten zugegriffen werden kann.
author: jasongre
ms.date: 08/29/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 096f441d39dde0f322ed117ab35a6a4641a38a93
ms.sourcegitcommit: 1d5cebea3e05b6d758cd01225ae7f566e05698d2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2022
ms.locfileid: "9405464"
---
# <a name="grid-capabilities"></a>Rasterfunktionen

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Die neue Rastersteuerung bietet eine Reihe nützlicher und leistungsfähiger Funktionen, mit denen Sie die Benutzerproduktivität steigern, interessantere Ansichten Ihrer Daten erstellen und aussagekräftige Einblicke in Ihre Daten gewinnen können. Dieser Artikel deckt die folgenden Funktionen ab: 

- Berechnete Werte anzeigen 
- Type-ahead
- Auswerten von mathematischen Ausdrücken 
- Gruppierung von Tabellendaten (separat aktiviert durch Verwendung der Funktion **Gruppierung in Rastern**)
- Spalten einfrieren (separat aktiviert über die Funktion **Spalten in Rastern einfrieren**)
- Spaltenbreite automatisch anpassen
- Dehnbare Spalten

## <a name="showing-calculated-values"></a>Berechnete Werte anzeigen
In Finanz- und Betriebs-Apps können Benutzer in einem Raster einen berechneten Wert für jede numerische Spalte anzeigen. Diese berechneten Werte werden in einem Fußzeilenbereich am unteren Rand des Rasters angezeigt.

[![Berechnete Werte in Rastern anzeigen.](./media/grids-aggregation.png)](./media/grids-aggregation.png)

In Versionen vor 10.0.29 ist die Summe der einzige unterstützte berechnete Wert. Ab Version 10.0.29, nachdem sie die Funktion **Erweiterte Aggregationsfunktionen für Raster** aktiviert haben, können Benutzer zwischen den folgenden vier berechneten Werten wählen:

- Minimum
- Maximum
- Gesamt
- Durchschnitt

Eine Spalte kann immer nur einen berechneten Wert eines einzigen Typs anzeigen. Jede Spalte im Raster kann jedoch so konfiguriert werden, dass sie einen berechneten Wert eines anderen Typs anzeigt.

### <a name="showing-the-grid-footer"></a>Anzeigen der Rasterfußzeile
Es gibt einen Fußzeilenbereich am unteren Rand jedes tabellarischen Rasters in Finanz- und Betriebs-Apps. In der Fußzeile können wertvolle Informationen angezeigt werden, die sich auf die im Gitter angezeigten Daten beziehen. Hier sind einige Beispiele für diese Informationen:

- Die Anzahl der ausgewählten Zeilen in der Tabelle (wenn Sie mehr als einen Datensatz auswählen)
- Berechnete Werte am unteren Ende konfigurierter, numerischer Spalten (zum Beispiel Gesamtsummen)
- Die Anzahl von Reihen in einem Dataset 

Diese Fußzeile ist standardmäßig ausgeblendet, aber Sie können sie einschalten. Um die Fußzeile für ein Raster anzuzeigen, wählen Sie die Schaltfläche **Rasteroptionen** in der Rasterübeschrift aus und wählen Sie dann die Option **Fußzeile anzeigen** aus. Nachdem Sie die Fußzeile für ein bestimmtes Raster aktiviert haben, wird diese Einstellung gespeichert, bis der Benutzer die Fußzeile ausblendet. Um die Fußzeile auszublenden, wählen Sie **Fußzeile ausblenden** im Menü **Rasteroptionen** aus.

### <a name="specifying-columns-with-calculated-values"></a>Spalten mit berechneten Werten festlegen
Derzeit werden in keiner Spalte standardmäßig berechnete Werte angezeigt. Stattdessen wird die Einrichtung als einmalige Aktivität betrachtet, ganz wie das Anpassen der Spaltenbreiten in Rastern. Nachdem Sie festgelegt haben, dass Sie für eine Spalte einen berechneten Wert sehen wollen, wird diese Einstellung für den nächsten Besuch dieser Seite gespeichert.

Es gibt zwei Möglichkeiten, eine Spalte so zu konfigurieren, dass ein berechneter Wert angezeigt wird:

- Wählen und halten Sie (oder klicken Sie mit der rechten Maustaste auf) die Spalte, für die Sie einen berechneten Wert anzeigen möchten. Wenn die Funktion **Erweiterte Aggregationsfunktionen für Raster** aktiviert ist, wählen Sie **Spaltensummen anzeigen** und dann den gewünschten berechneten Wert aus. Wenn diese Funktion nicht aktiviert ist, wählen Sie **Summe dieser Spalte**. Diese Aktion führt zu drei Ereignissen:

    1. Die Rasterfußzeile erscheint. 
    2. Ihre Einstellung zum Anzeigen eines berechneten Werts für die Spalte wird gespeichert. 
    3. Die gewünschte Berechnung für die Spalte und alle anderen Spalten, für die Sie zuvor die Anzeige als berechneter Wert konfiguriert haben, wird gestartet. Die Zeit, die benötigt wird, um die berechneten Werte anzuzeigen, hängt von der Größe des Datasets ab.

- Nachdem die Fußzeile sichtbar ist, wählen Sie **Summe anzeigen** (oder **Berechneten Wert auswählen**, wenn die Funktion **Erweiterte Aggregationsfunktionen für Raster** aktiviert ist) im Fußzeilenbereich unten in der Spalte aus, für die Sie einen berechneten Wert anzeigen möchten. Wenn es keine konfigurierten Spalten gibt, ist diese Schaltfläche in der Fußzeile in allen numerischen Spalten verfügbar.

    Nachdem mindestens eine Spalte so konfiguriert wurde, dass sie einen berechneten Wert anzeigt, wird die Schaltfläche **Summe anzeigen** (oder **Berechneten Wert auswählen**) ist nur beim Hovern oder Fokussieren verfügbar. Die Auswahl der Schaltfläche speichert nur Ihre Präferenz für das Anzeigen eines berechneten Wert in der Spalte, sodass diese Präferenz bei zukünftigen Besuchen der Seite angewendet wird. In der Fußzeile wird dieser Zustand durch einen Bindestrich in der Spalte angezeigt. (Beachten Sie, dass der berechnete Wert sofort angezeigt wird, wenn das Dataset klein genug ist.)

Wenn Sie einen Fehler machen und einen berechneten Wert in einer bestimmten Spalte nicht mehr anzeigen möchten, halten Sie die Spalte gedrückt (oder klicken Sie mit der rechten Maustaste darauf) und wählen Sie dann **Summe ausblenden** (oder **Spaltensummen anzeige \> Keine**, wenn die Funktion **Erweiterte Aggregationsfunktionen für Raster** aktiviert ist). Wählen Sie alternativ **Summe ausblenden** (oder **Berechneten Wert ausblenden**) in der Fußzeile dieser Spalte. Diese Einstellung wird ebenfalls für zukünftige Besuche der Seite gespeichert. 

### <a name="calculating-aggregate-values"></a>Aggregatwerte berechnen
Wenn Sie zu einer Seite wechseln, in der die Fußzeile sichtbar ist und Spalten bereits so konfiguriert sind, dass sie berechnete Werte anzeigen, werden diese Werte möglicherweise nicht in der Fußzeile angezeigt. Das Verhalten hängt von der Größe des Datasets auf der Seite ab. Wenn das Dataset ausreichend klein ist, werden automatisch die berechneten Werte sowie die Anzahl der Zeilen im Dataset gemeinsam angezeigt. Befinden sich in der Fußzeile unter den Spalten, die Sie für Gesamtsummen konfiguriert haben, Bindestriche, ist das Dataset zu groß und das System kann berechnete Werte nicht sofort anzeigen. In diesem Fall ist eine explizite Aktion erforderlich, um die Werte zu berechnen. Um die Werte zu berechnen, wählen Sie die Schaltfläche **Berechnen** in der Fußzeile aus. Halten Sie alternativ eine Spalte, deren Summe Sie anzeigen lassen möchten, gedrückt (oder klicken Sie mit der rechten Maustaste darauf) und wählen Sie dann **Summe dieser Spalte** aus (oder **Spaltensummen anzeigen** und dann den gewünschten berechneten Wert, wenn die Funktion **Erweiterte Aggregationsfunktionen für Raster** aktiviert ist).

Wenn die Berechnung sehr lange dauert, können Sie den Vorgang jederzeit durch Auswahl der Schaltfläche **Abbrechen** abbrechen. Manchmal ist das Dataset zu groß, um Aggregatwerte zu berechnen (die Grenze ist von Ihrer Organisation festgelegt). In diesem Fall werden Sie stattdessen aufgefordert, Ihre Daten stärker zu filtern.

> [!NOTE]
> Systemadministratoren können das Limit für die Anzahl der Datensätze, die für die Berechnung von Aggregaten zur Verfügung stehen, ändern, indem sie den Parameter **Maximale Anzahl lokaler Datensätze für jedes Raster** auf der Seite **Client-Leistungsoptionen** anpassen. Der Standardwert ist 25.000 Datensätze. Administratoren sollten bei der Anpassung dieses Wertes vorsichtig sein, da ein zu hoher Wert den verfügbaren Speicher auf dem Rechner des Benutzers erschöpfen kann. Der Wert sollte 50.000 Datensätze nicht überschreiten.

Berechnete Werte werden automatisch aktualisiert, wenn Sie Zeilen im Dataset aktualisieren, löschen oder erstellen.

## <a name="typing-ahead-of-the-system"></a>Type-ahead
In vielen Geschäftsszenarien ist die Möglichkeit, Daten schnell in das System einzugeben, sehr wichtig. Vor der Einführung der neuen Rastersteuerung konnten Benutzer Daten nur in der aktuellen Zeile ändern. Nachdem sie Änderungen in einer Zeile vorgenommen hatten, konnten Benutzer daher nicht zu einer anderen Zeile wechseln und keine neue Zeile erstellen, bis das System die Änderungen in der aktuellen Zeile erfolgreich überprüft und (im Fall der Zeilenerstellung) die gesamte Logik ausgeführt hat, die mit der Erstellung einer neuen Zeile zusammenhängt. Um die Zeit zu verringern, die Benutzern auf den Abschluss dieser Vorgänge warten, und die Benutzerproduktivität zu verbessern, passt das neue Raster diese Aktionen so an, dass sie asynchron sind. Benutzer können neue Zeilen erstellen oder zu anderen Zeilen wechseln, um Änderungen vorzunehmen, während die vorherigen Zeilenüberprüfungen oder Zeilenerstellungslogiken ausstehen. 

[![Type-ahead.](./media/gridFastEntry-07-25-2022.gif)](./media/gridFastEntry-07-25-2022.gif)

Um dieses neue Verhalten zu unterstützen, wurde rechts von der Zeilenauswahlspalte eine neue Spalte für den Zeilenstatus hinzugefügt, wenn sich das Raster im Bearbeitungsmodus befindet. Diese Spalte gibt einen der folgenden Status an:

- **Leer** – Kein Statusbild zeigt an, dass die Zeile vom System erfolgreich gespeichert wurde.
- **Verarbeitung ausstehend** – Dieser Status zeigt an, dass die Änderungen in der Zeile noch nicht vom Server gespeichert wurden, sondern sich in einer Warteschlange mit Änderungen befinden, die verarbeitet werden müssen. Bevor Sie außerhalb des Rasters Maßnahmen ergreifen, müssen Sie warten, bis alle ausstehenden Änderungen verarbeitet wurden. Darüber hinaus ist der Text in diesen Zeilen kursiv gedruckt, um den nicht gespeicherten Status der Zeilen anzuzeigen. 
- **Ungültiger Status** – Dieser Status zeigt an, dass während der Verarbeitung der Zeile eine Warnung oder Meldung ausgelöst wurde, und das System möglicherweise daran gehindert hat, die Änderungen in dieser Zeile zu speichern. Im alten Raster wurden erzwungen, das Problem sofort zu beheben, wenn der Speichervorgang fehlgeschlagen hat. Im neuen Raster werden Sie jedoch benachrichtigt, dass ein Validierungsproblem aufgetreten ist. Sie können dann entscheiden, wann Sie Probleme in der Zeile beheben möchten. Wenn Sie bereit sind, das Problem zu beheben, können Sie den Fokus manuell zurück in die Zeile verschieben. Alternativ können Sie die Aktion **Dieses Problem beheben** auswählen. Durch diese Aktion wird der Fokus sofort wieder auf die Zeile verschoben, in der das Problem auftritt, und Sie können Änderungen innerhalb oder außerhalb des Rasters vornehmen. Beachten Sie, dass die Verarbeitung nachfolgender ausstehender Zeilen gestoppt wird, bis diese Validierungswarnung behoben ist. 
- **Pause** – Dieser Status zeigt an, dass die Verarbeitung durch den Server angehalten wurde, da die Überprüfung der Zeile ein Popup-Dialogfeld auslöste, für das Benutzereingaben erforderlich sind. Da der Benutzer möglicherweise Daten in einer anderen Zeile eingibt, wird das Popup-Dialogfeld diesem Benutzer nicht sofort angezeigt. Stattdessen wird es angezeigt, wenn der Benutzer die Verarbeitung fortsetzt. Dieser Status wird von einer Benachrichtigung begleitet, die den Benutzer über die Situation informiert. Die Benachrichtigung enthält eine Aktion **Verarbeitung fortsetzen**, die das Popup-Dialogfeld auslöst.

### <a name="differences-when-entering-data-ahead-of-the-system"></a>Unterschiede bei der Eingabe vor dem Verarbeitungspunkt des Systems
Wenn Sie Daten vor dem Punkt der Verarbeitung durch das System eingeben, müssen Sie mit einigen Änderungen bei der Dateneingabe rechnen:

- Sie werden feststellen, dass es keine Such-Dropdownlisten gibt, Feldwerte nicht überprüft werden, nachdem Sie zu einer anderen Spalte in derselben Zeile wechseln, und Spalten anfangs keine Standardwerte anzeigen. Dieses Verhalten tritt auf, wenn Sie vor dem Verarbeitungspunkt des Systems erstellen oder aktualisieren. Nachdem das System jedoch die Stelle erreicht hat, die Sie gerade bearbeiten, wird das Standardvorgehen fortgesetzt. Wenn Sie Änderungen an einem Feld vorgenommen haben, das normalerweise einen Standardwert erhält, überschreiben Ihre Änderungen den Standardfeldwert, wenn der Server mit der Verarbeitung der Zeile beginnt.
- Wenn Sie eine neue Zeile erstellen, indem Sie die **Nach-unten**-Taste drücken, werden alle Spalten im Raster als bearbeitbar angezeigt. Standardmäßig wird der Fokus auf die erste Spalte in der neuen Zeile gesetzt. Diese Spalte ist möglicherweise nicht dieselbe Spalte, die den anfänglichen Fokus im Legacy-Raster erhalten hat, oder dieselbe Spalte, die den Fokus erhält, nachdem Sie die Schaltfläche **Neu** ausgewählt haben. Ihre Organisation kann das System anpassen und die Spalte ändern, die den anfänglichen Fokus erhält, wenn die **Nach-unten**-Taste ausgewählt ist. Weitere Informationen finden Sie im Abschnitt [Die Spalte festlegen, die den anfänglichen Fokus erhält, wenn neue Zeilen mithilfe der Nach-unten-Taste erstellt werden](#developer-specifying-the-column-that-receives-the-initial-focus-when-new-rows-are-created-by-using-the-down-arrow-key). Unabhängig davon können Sie die Personalisierung verwenden, um jedes Raster für die Dateneingabe zu optimieren. Sie können insbesondere Felder neu anordnen, sodass die erste Spalte diejenige ist, in der Sie mit der Dateneingabe beginnen möchten. Möglicherweise möchten Sie auch Felder für die Dateneingabe allgemein neu anordnen, um Tabstopps zu reduzieren und alle Felder auszublenden, die für die Dateneingabe in dieser bestimmten Ansicht nicht erforderlich sind.

### <a name="pasting-from-excel"></a>Einfügen aus Excel
Benutzer konnten schon immer Daten aus Rastern in Finanz- und Betriebs-Apps nach Microsoft Excel exportieren, indem sie den **Export nach Excel**-Mechanismus verwendeten. Dank der Möglichkeit, Daten vor dem System einzugeben, unterstützt das neue Raster jedoch das Kopieren von Tabellen aus Excel und das direkte Einfügen in Raster in Finanz- und Betriebs-Apps. Die Rasterzelle, von der aus der Einfügevorgang initiiert wird, bestimmt, wo die kopierte Tabelle eingefügt wird. Der Inhalt des Rasters wird durch den Inhalt der kopierten Tabelle überschrieben, außer in zwei Fällen:

- Wenn die Anzahl der Spalten in der kopierten Tabelle die Anzahl der im Raster verbleibenden Spalten überschreitet, wird der Benutzer benachrichtigt, dass die zusätzlichen Spalten ignoriert wurden. 
- Wenn die Anzahl der Zeilen in der kopierten Tabelle die Anzahl der Zeilen im Raster überschreitet, beginnend mit der Einfügeposition, werden die vorhandenen Zellen durch den eingefügten Inhalt überschrieben, und alle zusätzlichen Zeilen aus der kopierten Tabelle werden unten im raster als neue Zeilen eingefügt. 

## <a name="evaluating-math-expressions"></a>Auswerten von mathematischen Ausdrücken
Als Produktivitätssteigerung können Benutzer mathematische Formeln in numerische Zellen in einem Gitter eingeben. Sie müssen die Berechnung nicht in einer Anwendung außerhalb des Systems durchführen. Wenn Sie z.B. **=15\*4** eingeben und dann die Taste **Tab** drücken, um das Feld zu verlassen, wertet das System den Ausdruck aus und speichert einen Wert von **60** für das Feld.

[![Auswerten von mathematischen Ausdrücken.](./media/gridMathExpression-07-25-2022.gif)](./media/gridMathExpression-07-25-2022.gif)

Damit das System einen Wert als Ausdruck erkennt, müssen Sie vor dem Wert ein Gleichheitszeichen (**=**) angeben. Mehr Informationen zu den unterstützten Operatoren und zur Syntax finden Sie unter [Unterstützte mathematische Symbole](http://bugwheels94.github.io/math-expression-evaluator/#supported-maths-symbols).

Ab Version 10.0.29 wurde die Möglichkeit, mathematische Ausdrücke in numerischen Steuerelementen auszuwerten, erweitert und ist jetzt auch außerhalb des Rasters verfügbar.

## <a name="grouping-tabular-data"></a>Gruppieren von Tabellendaten
Geschäftsanwender müssen häufig Ad-hoc-Datenanalysen durchführen. Obwohl diese Analyse durch den Export von Daten nach Microsoft Excel und die Verwendung von Pivottabellen möglich ist, können Benutzer mit der Funktion **Gruppieren in Rastern**, die von der neuen Funktion Rastersteuerelement abhängt, ihre tabellarischen Daten innerhalb von Finanz- und Betriebs-Apps auf interessante Weise organisieren. Da diese Funktion die Funktion **Berechnete Werte** erweitert, erlaubt Ihnen die Funktion **Gruppieren** wichtige Einblicke in die Daten, indem Zwischensummen auf Gruppenebene bereitgestellt werden.

[![Gruppieren von Daten in einem Raster.](./media/grids-groupingWithTotals.png)](./media/grids-groupingWithTotals.png)

Um diese Funktion zu verwenden, klicken Sie mit der rechten Maustaste auf die Spalte, nach der Sie gruppieren möchten, und wählen die Option für **Nach dieser Spalte gruppieren** aus. Diese Aktion sortiert die Daten nach der ausgewählten Spalte, fügt eine neue Spalte **Gruppieren nach** am Anfang des Rasters hinzu und fügt „Kopfzeilen“ am Anfang jeder Gruppe ein. Diese Kopfzeilen enthalten die folgenden Informationen zu jeder Gruppe:

- Datenwert für die Gruppe 
- Spaltenname (Diese Information ist besonders nützlich, wenn mehrere Gruppierungsebenen unterstützt werden.)
- Anzahl der Datenzeilen in dieser Gruppe
- Berechnete Werte für jede konfigurierte Spalte (z. B. Zwischensummen, wenn die Spalte so konfiguriert ist, dass sie eine Summe anzeigt)

Wenn [Gespeicherte Ansichten](saved-views.md) aktiviert ist, können Sie die Gruppierung als Teil einer Ansicht auf Seiten speichern, auf denen Abfragen in Ansichten gespeichert werden können. Zum Beispiel solche mit großen Ansichtswählern. Ausführlichere Informationen finden Sie im Abschnitt [Wechsel zwischen Ansichten](saved-views.md#switching-between-views). 

### <a name="multiple-levels-of-grouping"></a>Mehrere Gruppierungsebenen
Nachdem Sie Daten nach einer einzelnen Spalte gruppiert haben, können Sie die Daten durch Auswahl von **Nach dieser Spalte gruppieren** für die gewünschte Spalte nach einer anderen Spalte gruppieren. Dieser Prozess kann wiederholt werden, bis Sie 5 verschachtelte Gruppierungsebenen haben. Dies ist die maximal unterstützte Tiefe. Ab diesem Zeitpunkt können Sie nicht mehr nach zusätzlichen Spalten gruppieren.

Sie können die Gruppierung für jede Spalte jederzeit entfernen, indem Sie mit der rechten Maustaste auf diese Spalte klicken und **Gruppierung aufheben** auswählen. Sie können die Gruppierung auch für alle Spalten entfernen, indem Sie **Rasteroptionen** und dann **Gruppierung für alle aufheben** auswählen.

### <a name="sorting-grouped-data"></a>Sortieren von gruppierten Daten
Nachdem Sie Daten nach einer oder mehreren Spalten gruppiert haben, können Sie die Sortierrichtung für jede Gruppierungsspalte über die entsprechende Spaltenüberschrift ändern. 

Wenn Sie nach einer nicht gruppierten Spalte sortieren, bleibt die Gruppierung erhalten. Die Daten werden innerhalb jeder Gruppe basierend auf der ausgewählten Spalte sortiert.

### <a name="expanding-and-collapsing-groups"></a>Gruppen erweitern und reduzieren
Bei der anfänglichen Gruppierung von Daten werden alle Gruppen erweitert. Sie können zusammengefasste Ansichten der Daten erstellen, indem Sie einzelne Gruppen reduzieren, oder Sie können das Erweitern und Reduzieren von Gruppen verwenden, um die Navigation durch die Daten zu erleichtern. Um eine Gruppe zu erweitern oder zu reduzieren, wählen Sie die Schaltfläche Chevron (>) in der entsprechenden Gruppenkopfzeile. Beachten Sie: Der Status zum Erweitern/Reduzieren einzelner Gruppen lautet: **nicht** in der Personalisierung gespeichert.

### <a name="selecting-and-unselecting-rows-at-the-group-level"></a>Auswählen und Aufheben der Auswahl von Zeilen auf Gruppenebene
Auf die gleiche Weise, wie Sie alle Zeilen im Raster auswählen (oder die Auswahl aufheben) können, indem Sie das Kontrollkästchen oben in der ersten Spalte des Rasters aktivieren, können Sie auch alle Zeilen in einer Gruppe schnell auswählen (oder die Auswahl aufheben), indem Sie das Kontrollkästchen in der entsprechenden Gruppenkopfzeile auswählen. Das Kontrollkästchen in der Gruppenkopfzeile gibt immer den aktuellen Auswahlstatus der Zeilen in dieser Gruppe wieder, unabhängig davon, ob alle Zeilen ausgewählt sind, keine Zeilen ausgewählt sind oder nur einige Zeilen ausgewählt sind.

### <a name="hiding-column-names"></a>Spaltennamen ausblenden
Beim Gruppieren von Daten wird standardmäßig der Spaltenname in der Gruppenkopfzeile angezeigt. Sie können den Spaltennamen in Gruppenkopfzeilen unterdrücken, indem Sie **Rasteroptionen** > **Gruppenspaltennamen ausblenden** auswählen.

### <a name="grouping-on-date-and-time-columns"></a>Gruppierung nach Datums‑ und Uhrzeitspalten
Wenn Sie nach Datums- oder DateTime-Feldern gruppieren, können Sie nach Jahr, Monat oder Tag gruppieren. Die Gruppe „Wert“ in der entsprechenden Kopfzeile entspricht dem Format aus diesem Feld. Außerdem können Sie bei DateTime- und Zeitfeldern nach Stunden, Minuten oder Sekunden gruppieren.

> [!IMPORTANT]
> Benutzer können derzeit keine Gruppierungsspalten hinzufügen, nachdem sie nach einem Segment einer Datums- oder Zeitspalte gruppiert haben.

## <a name="freezing-columns"></a>Spalten fixieren
Einige Spalten in einem Raster sind möglicherweise sehr wichtig für den Kontext, sodass sie nicht möchten, dass sie nicht mehr angezeigt werden. Stattdessen möchten Sie vielleicht, dass die Werte in diesen Spalten immer sichtbar sind. Die Funktion **Spalten im Raster einfrieren** bietet den Benutzern diese Flexibilität. 

[![Fixieren von Spalten in einem Raster.](./media/gridFreezingColumns-07-25-2022.gif)](./media/gridFreezingColumns-07-25-2022.gif)

Um eine Spalte zu fixieren, klicken Sie mit der rechten Maustaste in die Spaltenüberschrift und wählen Sie dann **Spalte fixieren**. Wenn Sie diesen Schritt zum ersten Mal ausführen, wird die ausgewählte Spalte zur ersten Spalte und wird nicht mehr aus der Ansicht gescrollt. Jede nachfolgende Spalte, die Sie fixieren, wird rechts von der letzten fixierten Spalte hinzugefügt. Sie können die Standardfunktion zum Verschieben verwenden, um fixierte Spalten nach Bedarf neu anzuordnen. Fixierte Spalten können jedoch nicht verschoben werden, sodass sie in der Gruppe der nicht fixierten Spalten angezeigt werden. Ebenso können nicht fixierte Spalten nicht verschoben werden, sodass sie in der Gruppe der fixierten Spalten angezeigt werden.

Um die Fixierung einer Spalte aufzuheben, klicken Sie mit der rechten Maustaste in die Überschrift der fixierten Spalte, und wählen Sie dann **Spaltenfixierung aufheben**. 

Beachten Sie, dass die Zeilenauswahl- und Zeilenstatusspalten im neuen Raster immer als die ersten beiden Spalten fixiert werden. Wenn diese Spalten in einem Raster enthalten sind, sind sie für Benutzer unabhängig von der horizontalen Bildlaufposition im Raster immer sichtbar. Diese beiden Spalten können nicht neu angeordnet werden.

## <a name="autofit-column-width"></a>Spaltenbreite automatisch anpassen
Wie in Excel können Benutzer automatisch die Größenänderung einer Spalte basierend auf dem momentan in dieser Spalte angezeigten Inhalt erzwingen. Doppeltippen (oder doppelklicken) Sie einfach auf die Dimensionierungspunkt in der Spalte. Setzen Sie alternativ den Fokus auf die Spaltenüberschrift und wählen Sie dann die die **A**-Taste (für „automatisch anpassen“).

## <a name="frequently-asked-questions"></a>Häufig gestellte Fragen
### <a name="how-do-i-enable-the-new-grid-control-in-my-environment"></a>Wie aktiviere ich die neue Rastersteuerung in meiner Umgebung? 

Die Funktion **Neue Rastersteuerung** ist in jeder Umgebung direkt in der Funktionsverwaltung verfügbar. Nachdem die Funktion in der Funktionsverwaltung aktiviert wurde, verwenden alle nachfolgenden Benutzersitzungen die neue Rastersteuerung. 

Diese Funktion wurde ab Version 10.0.21 standardmäßig aktiviert. Sie soll im Oktober 2022 obligatorisch werden.

## <a name="developer-topics"></a>Entwicklerthemen

### <a name="developer-opting-out-individual-pages-from-using-the-new-grid"></a>[Entwickler] Deaktivierung einzelner Seiten für die Verwendung des neuen Rasters 
Wenn Ihre Organisation eine Seite entdeckt, bei der Probleme bei der Verwendung des neuen Rasters auftreten, steht eine API zur Verfügung, mit der ein einzelnes Formular die Vorgängerrastersteuerung und der Rest des Systems weiterhin die neue Rastersteuerung verwenden kann. Fügen Sie den folgenden Aufruf `super()` in die `run()` Methode für das Formular ein, um das Raster für eine einzelne Seite zu deaktivieren.

```this.forceLegacyGrid();```

Diese API wird letztendlich veraltet, um das Entfernen des Legacy-Raster-Steuerelements zu ermöglichen. Sie bleibt jedoch mindestens 12 Monate nach Bekanntgabe der Einstellung verfügbar. Wenn Probleme die Verwendung dieser API erfordern, melden Sie diese an Microsoft.

#### <a name="forcing-a-page-to-use-the-new-grid-after-previously-opting-out-the-grid"></a>Erzwingen, dass eine Seite das neue Raster verwendet, nachdem das Raster zuvor deaktiviert wurde
Wenn Sie eine einzelne Seite von der Verwendung des neuen Rasters abgemeldet haben, möchten Sie das neue Raster möglicherweise später wieder aktivieren, nachdem die zugrunde liegenden Probleme behoben wurden. Dazu müssen Sie lediglich den Aufruf von `forceLegacyGrid()` entfernen. Die Änderung wird erst wirksam, wenn eine der folgenden Bedingungen eintritt:

- **Erneute Bereitstellung der Umgebung**: Wenn eine Umgebung aktualisiert und erneut bereitgestellt wird, wird die Tabelle, die die Seiten speichert, die sich aus dem neuen Raster abgemeldet haben (FormControlReactGridState), automatisch gelöscht.
- **Manuelles Löschen der Tabelleninhalte**: Für Entwicklungsszenarien müssen Sie SQL verwenden, um die Inhalte der FormControlReactGridState-Tabelle zu löschen und dann den AOS neu zu starten. Diese Kombination von Aktivitäten setzt die Zwischenspeicherung von Seiten zurück, die sich vom neuen Raster abgemeldet haben.

### <a name="developer-opting-individual-grids-out-of-the-typing-ahead-of-the-system-capability"></a>[Entwickler] Einzelne Raster aus der Funktionalität Typing ahead of the system herausnehmen
Es gibt einige Szenarien, die sich nicht gut für die *Typisierung vor dem System* Funktionalität des Rasters eignen. (Einige Codes, die bei der Validierung einer Zeile ausgelöst werden, führen beispielsweise dazu, dass eine Datenquellenrecherche ausgelöst wird, und die Recherche kann dann unbestätigte Änderungen an bestehenden Zeilen beschädigen.) Wenn Ihr Unternehmen ein solches Szenario entdeckt, steht eine API zur Verfügung, mit der ein Entwickler ein einzelnes Raster von der asynchronen Zeilenvalidierung ausnehmen und zum veralteten Verhalten zurückkehren kann.

Wenn die asynchrone Zeilenvalidierung in einem Raster deaktiviert ist, können Benutzer keine neue Zeile erstellen oder zu einer anderen bestehenden Zeile im Raster wechseln, während in der aktuellen Zeile Validierungsprobleme bestehen. Ein Nebeneffekt dieser Aktion ist, dass Tabellen nicht aus Excel in Finanzen und Betrieb Raster eingefügt werden können.

Um ein einzelnes Raster von der asynchronen Zeilenvalidierung auszunehmen, fügen Sie in der Methode `run()` des Formulars den folgenden Aufruf nach `super()` ein.

```<gridControl>.allowPreemptiveClient(false);```

> [!NOTE]
> - Dieser Aufruf sollte nur in Ausnahmefällen aufgerufen werden und nicht für alle Raster die Norm sein.
> - Es wird nicht empfohlen, diese API zur Laufzeit nach dem Laden des Formulars umzuschalten.

### <a name="developer-size-to-available-width-columns"></a>[Entwickler] Spalten mit bis zur verfügbaren Breite angepasster Größe
Wenn ein Entwickler die **WidthMode**-Eigenschaft bei Spalten innerhalb des neuen Rasters auf **SizeToAvailable** festlegt, haben diese Spalten zunächst dieselbe Breite wie bei einer Einstellung der Eigenschaft **SizeToContent**. Sie dehnen sich jedoch, um jede zusätzliche verfügbare Breite innerhalb des Rasters zu nutzen. Wenn die Eigenschaft bei mehreren Spalten auf **SizeToAvailable** festgelegt ist, teilen sich alle diese Spalten die zusätzliche verfügbare Breite innerhalb des Rasters. Wenn ein Benutzer jedoch die Größe einer dieser Spalten manuell ändert, wird die Spalte statisch. Sie bleibt auf dieser Breite und wird nicht mehr gedehnt, um die zusätzliche verfügbare Rasterbreite einzunehmen.

### <a name="developer-specifying-the-column-that-receives-the-initial-focus-when-new-rows-are-created-by-using-the-down-arrow-key"></a>[Entwickler] Die Spalte festlegen, die den anfänglichen Fokus erhält, wenn neue Zeilen mithilfe der Nach-unten-Taste erstellt werden
Wie im Abschnitt [Unterschiede bei der Eingabe vor dem Verarbeitungspunkt des Systems](#differences-when-entering-data-ahead-of-the-system) besprochen, ist das Standardverhalten, den Fokus auf die erste Spalte in der neuen Zeile zu legen, wenn die Funktion „Type-ahead“ aktiviert ist und ein Benutzer eine neue Zeile erstellt, indem er die **Nach-unten**-Taste verwendet. Diese Erfahrung kann sich von der Erfahrung im Legacy-Raster oder wenn eine **Neu**-Schaltfläche ausgewählt ist unterscheiden.

Benutzer und Organisationen können gespeicherte Ansichten erstellen, die für die Dateneingabe optimiert sind. (Beispielsweise können Sie Spalten neu anordnen, sodass die erste Spalte diejenige ist, in der Sie mit der Dateneingabe beginnen möchten.) Darüber hinaus können Organisationen dieses Verhalten ab Version 10.0.29 mithilfe der **selectedControlOnCreate()**-Methode anpassen. Diese Methode erlaubt einem Entwickler, die Spalte festzulegen, die den anfänglichen Fokus erhalten soll, wenn eine neue Zeilen mithilfe der **Nach-unten**-Taste erstellt wird. Als Eingabe übernimmt diese API die Steuerelement-ID, die der Spalte entspricht, die den anfänglichen Fokus erhalten soll.

### <a name="developer-handling-grids-with-non-react-extensible-controls"></a>[Entwickler] Umgang mit Rastern mit erweiterbaren Nicht-React-Steuerelementen
Wenn ein Raster geladen wird und das System auf ein erweiterbares Steuerelement trifft, das nicht auf React basiert, erzwingt das System stattdessen das Rendern des Legacy-Grids. Tritt diese Situation zum ersten Mal auf, wird eine Meldung angezeigt, dass die Seite aktualisiert werden muss. Danach lädt diese Seite das alte Raster bis zum nächsten Systemupdate automatisch ohne weitere Benachrichtigungen an die Benutzer. 

Um diese Situation dauerhaft zu beheben, können Autoren erweiterbarer Steuerelemente eine React-Version des Steuerelements zur Verwendung im Raster erstellen.  Nach der Entwicklung kann die X++-Klasse für das Steuerelement mit dem Attribut **FormReactControlAttribute** ausgestattet werden, um den Speicherort des React-Bundles anzugeben, das für dieses Steuerelement geladen werden soll. Siehe die `SegmentedEntryControl`-Klasse als Beispiel.  

## <a name="known-issues"></a>Bekannte Probleme
In diesem Abschnitt wird eine Liste bekannter Probleme für die neue Rastersteuerung aufgeführt.

### <a name="open-issues"></a>Bekannte Probleme
- Nach dem Aktivieren der Funktion **Neue Rastersteuerung** werden einige Seiten weiterhin die vorhandene Rastersteuerung verwenden. Dies geschieht in den folgenden Situationen:
 
    - [Behoben] Auf der Seite gibt es eine Kartenliste, die in mehreren Spalten gerendert ist.
        - Diese Art von Kartenliste wird ab Version 10.0.30 von dem **Neuen Rastersteuerelement** unterstützt. Alle Verwendungen von forceLegacyGrid() für diesen Zweck können entfernt werden. 
    - [Behoben] Auf der Seite gibt es eine gruppierte Kartenliste.
        - Gruppierte Kartenlisten werden ab Version 10.0.30 von dem **Neuen Rastersteuerelement** unterstützt. Alle Verwendungen von forceLegacyGrid() für diesen Zweck können entfernt werden. 
    - [Behoben] Eine Rasterspalte mit einem nicht reagierenden erweiterbaren Steuerelement.
        - Erweiterbare Steuerelemente können eine React-Version ihres Steuerelements bereitstellen, die geladen wird, wenn sie im Raster platziert werden, und ihre Steuerelementdefinition so anpassen, dass dieses Steuerelement geladen wird, wenn es im Raster verwendet wird. Weitere Informationen finden Sie im entsprechenden Abschnitt für Entwickler. 

    Tritt diese Situation zum ersten Mal auf, wird eine Meldung zum Aktualisieren der Seite angezeigt. Nachdem diese Meldung angezeigt wird, verwendet die Seite das vorhandene Raster für alle Benutzer bis zur nächsten Aktualisierung der Produktversion weiter. Für ein zukünftiges Update wird an einem besseren Umgang mit diesen Szenarien gearbeitet, damit das neue Raster genutzt werden kann.

- [KB 4582758] Datensätze sind verschwommen, wenn Sie den Zoom von 100 auf einen anderen Prozentsatz ändern

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

