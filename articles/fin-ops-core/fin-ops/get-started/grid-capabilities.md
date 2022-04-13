---
title: Rasterfunktionen
description: In diesem Thema werden mehrere leistungsstarke Funktionen der Rastersteuerung beschrieben. Sie müssen die neue Rasterfunktion aktivieren, damit auf diese Fähigkeiten zugegriffen werden kann.
author: jasongre
ms.date: 03/21/2022
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
ms.openlocfilehash: 81577f54bd7fdc7d683c760dd4410f27da8ee1f0
ms.sourcegitcommit: c0f7ee7f8837fec881e97b2a3f12e7f63cf96882
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2022
ms.locfileid: "8462791"
---
# <a name="grid-capabilities"></a>Rasterfunktionen

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Die neue Rastersteuerung bietet eine Reihe nützlicher und leistungsfähiger Funktionen, mit denen Sie die Benutzerproduktivität steigern, interessantere Ansichten Ihrer Daten erstellen und aussagekräftige Einblicke in Ihre Daten gewinnen können. Dieser Artikel deckt die folgenden Funktionen ab: 

- Summen berechnen
- Type-ahead
- Auswerten von mathematischen Ausdrücken 
- Gruppierung von Tabellendaten (separat aktiviert durch Verwendung der Funktion **Gruppierung in Rastern**)
- Spalten einfrieren (separat aktiviert über die Funktion **Spalten in Rastern einfrieren**)
- Spaltenbreite automatisch anpassen
- Dehnbare Spalten

## <a name="calculating-totals"></a>Summen berechnen
In Apps für Finanzen und Betrieb haben Benutzer die Möglichkeit, Summen am unteren Rand numerischer Spalten in Rastern anzuzeigen. Diese Summen werden in einem Fußzeilenbereich am unteren Rand des Rasters angezeigt. 

### <a name="showing-the-grid-footer"></a>Anzeigen der Rasterfußzeile
In den Apps für Finanzen und Betrieb gibt es am unteren Rand jedes Tabellenrasters einen Fußbereich. In der Fußzeile können wertvolle Informationen angezeigt werden, die sich auf die im Gitter angezeigten Daten beziehen. Hier sind einige Beispiele für diese Informationen:

- Die Anzahl der ausgewählten Zeilen in der Tabelle (wenn Sie mehr als einen Datensatz auswählen)
- Gesamtsummen am unteren Ende konfigurierter, numerischer Spalten
- Die Anzahl von Reihen in einem Dataset 

Diese Fußzeile ist standardmäßig ausgeblendet, aber Sie können sie einschalten. Um die Fußzeile für ein Raster anzuzeigen, wählen Sie die Schaltfläche **Rasteroptionen** in der Rasterübeschrift aus und wählen Sie dann die Option **Fußzeile anzeigen** aus. Nachdem Sie die Fußzeile für ein bestimmtes Raster aktiviert haben, wird diese Einstellung gespeichert, bis der Benutzer die Fußzeile ausblendet. Um die Fußzeile auszublenden, wählen Sie **Fußzeile ausblenden** im Menü **Rasteroptionen** aus.

### <a name="specifying-columns-with-totals"></a>Angeben von Spalten mit Summen
Derzeit werden in keiner Spalte standardmäßig Summen angezeigt. Stattdessen wird dies als einmalige Einrichtungsaktivität betrachtet, ähnlich wie das Anpassen der Spaltenbreiten in Rastern. Wenn Sie festlegen, dass für eine Spalte Summen angezeigt werden sollen, wird diese Einstellung für den nächsten Besuch der Seite gespeichert.

Es gibt zwei Möglichkeiten, eine Spalte so zu konfigurieren, dass eine Summe angezeigt wird: 

- Klicken Sie mit der rechten Maustaste in die Spalte, für die Sie eine Gesamtsumme sehen möchten, und wählen Sie dann **Summe dieser Spalte**. Diese Aktion führt zu drei Ereignissen:

    1. Die Fußzeile wird sichtbar. 
    2. Ihre Präferenz für die Anzeige einer Gesamtsumme für diese Spalte wird gespeichert. 
    3. Eine Berechnung der Summen für diese Spalte und alle anderen Spalten, für die Sie zuvor die Summen angezeigt haben, wird gestartet. Die Zeit, die benötigt wird, um eine Gesamtsumme anzuzeigen, hängt von der Größe des Datensatzes ab, den Sie summieren möchten.

- Nachdem die Fußzeile sichtbar ist, wählen Sie **Summe anzeigen** im Fußbereich am unteren Ende der Spalte, für die Sie eine Summe sehen möchten. Wenn es keine konfigurierten Spalten gibt, ist die Schaltfläche **Summe anzeigen** für alle numerischen Spalten verfügbar. 

    Nachdem mindestens eine Spalte für Summen konfiguriert wurde, sind die Schaltflächen **Summe anzeigen** nur noch beim Hovern oder Fokussieren verfügbar. Die Auswahl von **Summe anzeigen** speichert nur Ihre Präferenz für die Anzeige einer Summe in dieser Spalte, sodass diese Präferenz bei zukünftigen Besuchen der Seite angewendet wird. In der Fußzeile wird dieser Zustand durch einen Bindestrich in der Spalte angezeigt. (Alternativ wird, wenn der Datensatz klein genug ist, sofort eine Gesamtsumme angezeigt).

Wenn Sie einen Fehler gemacht haben und keine Summe mehr in einer bestimmten Spalte anzeigen möchten, klicken Sie mit der rechten Maustaste auf die Spalte und wählen Sie **Summe ausblenden** aus oder wählen Sie **Summe ausblenden** in der Fußzeile der Spalte aus. Diese Einstellung wird ebenfalls für zukünftige Besuche der Seite gespeichert. 

### <a name="calculating-totals"></a>Summen berechnen
Wenn Sie zu einer Seite mit sichtbarer Fußzeile und Spalten kommen, die bereits für Summen konfiguriert sind, werden Summen möglicherweise in der Fußzeile angezeigt oder nicht. Das Verhalten ist abhängig von der Größe des Datasets auf der Seite. Wenn das Dataset ausreichend klein ist, werden automatisch die Gesamtsummen sowie die Anzahl der Zeilen im Dataset angezeigt. Befinden sich in der Fußzeile unter den Spalten, die Sie für Gesamtsummen konfiguriert haben, Bindestriche, ist das Dataset zu groß für das System, um Gesamtsummen sofort anzuzeigen. Eine explizite Aktion ist erforderlich, um die Gesamtsummen zu berechnen. Klicken Sie dazu auf die Schaltfläche **Berechnung** in der Fußzeile oder klicken Sie mit der rechten Maustaste auf eine Spalte, für die Sie eine Gesamtsumme wünschen, und wählen Sie **Summe für diese Spalte** aus.

Wenn die Berechnung sehr lange dauert, können Sie den Vorgang durch Auswahl der Schaltfläche **Abbrechen** abbrechen. Manchmal ist das Dataset zu groß, um Summen zu berechnen (eine von Ihrem Unternehmen auferlegte Grenze), und Sie werden stattdessen benachrichtigt, Ihre Daten stärker zu filtern. 

> [!NOTE]
> Systemadministratoren können das Limit für die Anzahl der Datensätze, die für die Berechnung von Summen zur Verfügung stehen, ändern, indem sie den Parameter **Maximale Anzahl lokaler Datensätze für jedes Raster** auf der Seite **Client-Leistungsoptionen** anpassen. Der Standardwert ist 25.000 Datensätze. Administratoren sollten bei der Anpassung dieses Wertes vorsichtig sein, da ein zu großer Wert den verfügbaren Speicher auf dem Rechner des Benutzers erschöpfen kann. Es wird empfohlen, 50.000 Datensätze nicht zu überschreiten.   

Die Summen werden automatisch aktualisiert, wenn Sie Zeilen im Dataset aktualisieren, löschen oder erstellen.

## <a name="typing-ahead-of-the-system"></a>Type-ahead
In vielen Geschäftsszenarien ist die Möglichkeit, Daten schnell in das System einzugeben, sehr wichtig. Vor Einführung der neuen Rastersteuerung konnten Benutzer Daten nur in der aktuellen Zeile ändern. Bevor sie eine neue Zeile erstellen oder zu einer anderen Zeile wechseln konnten, mussten sie warten, bis das System alle Änderungen erfolgreich überprüft hatte. Um die Wartezeit der Benutzer auf den Abschluss dieser Überprüfungen zu verringern und die Benutzerproduktivität zu verbessern, passt das neue Raster diese Überprüfungen so an, dass sie asynchron sind. Daher kann der Benutzer zu anderen Zeilen wechseln, um Änderungen vorzunehmen, während die vorherigen Zeilenüberprüfungen ausstehen. 

Um dieses neue Verhalten zu unterstützen, wurde rechts von der Zeilenauswahlspalte eine neue Spalte für den Zeilenstatus hinzugefügt, wenn sich das Raster im Bearbeitungsmodus befindet. Diese Spalte gibt einen der folgenden Status an:

- **Leer** – Kein Statusbild zeigt an, dass die Zeile vom System erfolgreich gespeichert wurde.
- **Verarbeitung ausstehend** – Dieser Status zeigt an, dass die Änderungen in der Zeile noch nicht vom Server gespeichert wurden, sondern sich in einer Warteschlange mit Änderungen befinden, die verarbeitet werden müssen. Bevor Sie außerhalb des Rasters Maßnahmen ergreifen, müssen Sie warten, bis alle ausstehenden Änderungen verarbeitet wurden. Darüber hinaus ist der Text in diesen Zeilen kursiv gedruckt, um den nicht gespeicherten Status der Zeilen anzuzeigen. 
- **Ungültiger Status** – Dieser Status zeigt an, dass während der Verarbeitung der Zeile eine Warnung oder Meldung ausgelöst wurde, und das System möglicherweise daran gehindert hat, die Änderungen in dieser Zeile zu speichern. Im alten Raster wurden erzwungen, das Problem sofort zu beheben, wenn der Speichervorgang fehlgeschlagen hat. Im neuen Raster werden Sie jedoch benachrichtigt, dass ein Validierungsproblem aufgetreten ist. Sie können dann entscheiden, wann Sie Probleme in der Zeile beheben möchten. Wenn Sie bereit sind, das Problem zu beheben, können Sie den Fokus manuell zurück in die Zeile verschieben. Alternativ können Sie die Aktion **Dieses Problem beheben** auswählen. Durch diese Aktion wird der Fokus sofort wieder auf die Zeile verschoben, in der das Problem auftritt, und Sie können Änderungen innerhalb oder außerhalb des Rasters vornehmen. Beachten Sie, dass die Verarbeitung nachfolgender ausstehender Zeilen gestoppt wird, bis diese Validierungswarnung behoben ist. 
- **Pause** – Dieser Status zeigt an, dass die Verarbeitung durch den Server angehalten wurde, da die Überprüfung der Zeile ein Popup-Dialogfeld auslöste, für das Benutzereingaben erforderlich sind. Da der Benutzer möglicherweise Daten in einer anderen Zeile eingibt, wird das Popup-Dialogfeld diesem Benutzer nicht sofort angezeigt. Stattdessen wird es angezeigt, wenn der Benutzer die Verarbeitung fortsetzt. Dieser Status wird von einer Benachrichtigung begleitet, die den Benutzer über die Situation informiert. Die Benachrichtigung enthält eine Aktion **Verarbeitung fortsetzen**, die das Popup-Dialogfeld auslöst.

Wenn Benutzer Daten vor dem Serverstandort eingeben, können sie einige Beeinträchtigungen der Dateneingabe erwarten, z. B. fehlende Suchvorgänge, Validierung auf Steuerungsebene und Eingabe von Standardwerten. Benutzer, die eine Dropdown-Liste benötigen, um einen Wert zu finden, sollten warten, bis der Server die aktuelle Zeile erreicht hat. Die Validierung auf Kontrollebene und die Eingabe von Standardwerten erfolgt auch, wenn der Server diese Zeile verarbeitet.

### <a name="pasting-from-excel"></a>Einfügen aus Excel
Benutzer konnten immer Daten aus Rastern in Apps für Finanzen und Betrieb  mit dem **Nach Excel exportieren**-Mechanismus nach Microsoft Excel exportieren. Die Möglichkeit, Daten vor dem System einzugeben, ermöglicht es dem neuen Raster jedoch, das Kopieren von Tabellen aus Excel und das direkte Einfügen in Tabellen in Raster in Apps für Finanzen und Betrieb zu unterstützen. Die Rasterzelle, von der aus der Einfügevorgang initiiert wird, bestimmt, wo die kopierte Tabelle eingefügt wird. Der Inhalt des Rasters wird durch den Inhalt der kopierten Tabelle überschrieben, außer in zwei Fällen:

- Wenn die Anzahl der Spalten in der kopierten Tabelle die Anzahl der im Raster verbleibenden Spalten überschreitet, wird der Benutzer benachrichtigt, dass die zusätzlichen Spalten ignoriert wurden. 
- Wenn die Anzahl der Zeilen in der kopierten Tabelle die Anzahl der Zeilen im Raster überschreitet, beginnend mit der Einfügeposition, werden die vorhandenen Zellen durch den eingefügten Inhalt überschrieben, und alle zusätzlichen Zeilen aus der kopierten Tabelle werden unten im raster als neue Zeilen eingefügt. 

## <a name="evaluating-math-expressions"></a>Auswerten von mathematischen Ausdrücken
Als Produktivitätssteigerung können Benutzer mathematische Formeln in numerische Zellen in einem Gitter eingeben. Sie müssen die Berechnung nicht in einer Anwendung außerhalb des Systems durchführen. Wenn Sie z.B. **=15\*4** eingeben und dann die Taste **Tab** drücken, um das Feld zu verlassen, wertet das System den Ausdruck aus und speichert einen Wert von **60** für das Feld.

Damit das System einen Wert als Ausdruck erkennt, müssen Sie vor dem Wert ein Gleichheitszeichen (**=**) angeben. Mehr Informationen zu den unterstützten Operatoren und zur Syntax finden Sie unter [Unterstützte mathematische Symbole](http://bugwheels94.github.io/math-expression-evaluator/#supported-maths-symbols).

## <a name="grouping-tabular-data"></a>Gruppieren von Tabellendaten
Geschäftsanwender müssen häufig Ad-hoc-Datenanalysen durchführen. Während dies durch das Exportieren von Daten nach Microsoft Excel und der Nutzung von Pivot-Tabellen geschehen kann, ermöglicht die Funktion **Gruppierung in Rastern**, die von der neuen Rastersteuerungsfunktion abhängt, Benutzern, ihre Tabellendaten auf effektive Weise in Apps für Finanzen und Betrieb zu organisieren. Da diese Funktion die **Summen**-Funktion erweitert, ermöglicht die Funktion **Gruppieren** wichtige Einblicke in die Daten zu gewinnen, indem Zwischensummen auf Gruppenebene bereitgestellt werden.

Um diese Funktion zu verwenden, klicken Sie mit der rechten Maustaste auf die Spalte, nach der Sie gruppieren möchten, und wählen die Option für **Nach dieser Spalte gruppieren** aus. Diese Aktion sortiert die Daten nach der ausgewählten Spalte, fügt eine neue Spalte **Gruppieren nach** am Anfang des Rasters hinzu und fügt „Kopfzeilen“ am Anfang jeder Gruppe ein. Diese Kopfzeilen enthalten die folgenden Informationen zu jeder Gruppe:

- Datenwert für die Gruppe 
- Spaltenname (Diese Information ist besonders nützlich, wenn mehrere Gruppierungsebenen unterstützt werden.)
- Anzahl der Datenzeilen in dieser Gruppe
- Zwischensummen für jede Spalte, die zur Anzeige von Gesamtsummen konfiguriert ist

Wenn [Gespeicherte Ansichten](saved-views.md) aktiviert ist, kann diese Gruppierung im Rahmen der Personalisierung als Teil einer Ansicht gespeichert werden, damit Sie beim nächsten Besuch der Seite schnell darauf zugreifen können.

### <a name="multiple-levels-of-grouping"></a>Mehrere Gruppierungsebenen
Nachdem Sie Daten nach einer einzelnen Spalte gruppiert haben, können Sie die Daten durch Auswahl von **Nach dieser Spalte gruppieren** für die gewünschte Spalte nach einer anderen Spalte gruppieren. Dieser Prozess kann wiederholt werden, bis Sie 5 verschachtelte Gruppierungsebenen haben. Dies ist die maximal unterstützte Tiefe. Ab diesem Zeitpunkt können Sie nicht mehr nach zusätzlichen Spalten gruppieren.

Sie können die Gruppierung für jede Spalte jederzeit entfernen, indem Sie mit der rechten Maustaste auf diese Spalte klicken und **Gruppierung aufheben** auswählen. Sie können die Gruppierung auch für alle Spalten entfernen, indem Sie **Rasteroptionen** und dann **Gruppierung für alle aufheben** auswählen.

### <a name="sorting-grouped-data"></a>Sortieren von gruppierten Daten
Nachdem Sie Daten nach einer oder mehreren Spalten gruppiert haben, können Sie die Sortierrichtung für jede Gruppierungsspalte über die entsprechende Spaltenüberschrift ändern. 

Das Verhalten beim Sortieren nach nicht gruppierten Spalten hängt von Ihrer Produktversion ab:

- Wenn Sie in Version 10.0.24 und früher nach einer nicht gruppierten Spalte sortieren, wird die Gruppierung aus allen Spalten entfernt, und die Daten werden nach der ausgewählten Spalte sortiert. 
- Wenn Sie in Version 10.0.25 und später nach einer nicht gruppierten Spalte sortieren, bleibt die Gruppierung erhalten und die Daten werden innerhalb jeder Gruppe auf der Grundlage der ausgewählten Spalte sortiert.

### <a name="expanding-and-collapsing-groups"></a>Gruppen erweitern und reduzieren
Bei der anfänglichen Gruppierung von Daten werden alle Gruppen erweitert. Sie können zusammengefasste Ansichten der Daten erstellen, indem Sie einzelne Gruppen reduzieren, oder Sie können das Erweitern und Reduzieren von Gruppen verwenden, um die Navigation durch die Daten zu erleichtern. Um eine Gruppe zu erweitern oder zu reduzieren, wählen Sie die Schaltfläche Chevron (>) in der entsprechenden Gruppenkopfzeile. Beachten Sie: Der Status zum Erweitern/Reduzieren einzelner Gruppen lautet: **nicht** in der Personalisierung gespeichert.

### <a name="selecting-and-unselecting-rows-at-the-group-level"></a>Auswählen und Aufheben der Auswahl von Zeilen auf Gruppenebene
Auf die gleiche Weise, wie Sie alle Zeilen im Raster auswählen (oder die Auswahl aufheben) können, indem Sie das Kontrollkästchen oben in der ersten Spalte des Rasters aktivieren, können Sie auch alle Zeilen in einer Gruppe schnell auswählen (oder die Auswahl aufheben), indem Sie das Kontrollkästchen in der entsprechenden Gruppenkopfzeile auswählen. Das Kontrollkästchen in der Gruppenkopfzeile gibt immer den aktuellen Auswahlstatus der Zeilen in dieser Gruppe wieder, unabhängig davon, ob alle Zeilen ausgewählt sind, keine Zeilen ausgewählt sind oder nur einige Zeilen ausgewählt sind.

### <a name="hiding-column-names"></a>Spaltennamen ausblenden
Beim Gruppieren von Daten wird standardmäßig der Spaltenname in der Gruppenkopfzeile angezeigt. Sie können den Spaltennamen in Gruppenkopfzeilen unterdrücken, indem Sie **Rasteroptionen** > **Gruppenspaltennamen ausblenden** auswählen.

### <a name="grouping-on-date-and-time-columns"></a>Gruppierung nach Datums‑ und Uhrzeitspalten
Ab Version 10.0.24 gibt es für Date- oder DateTime-Felder die Möglichkeit, nach Jahr, Monat oder Tag zu gruppieren. Die Gruppe „Wert“ in der entsprechenden Kopfzeile entspricht dem Format aus diesem Feld. Außerdem können Sie bei DateTime- und Zeitfeldern nach Stunden, Minuten oder Sekunden gruppieren. 

## <a name="freezing-columns"></a>Spalten fixieren
Einige Spalten in einem Raster sind möglicherweise sehr wichtig für den Kontext, sodass sie nicht möchten, dass sie nicht mehr angezeigt werden. Stattdessen möchten Sie vielleicht, dass die Werte in diesen Spalten immer sichtbar sind. Die Funktion **Spalten im Raster einfrieren** bietet den Benutzern diese Flexibilität. 

Um eine Spalte zu fixieren, klicken Sie mit der rechten Maustaste in die Spaltenüberschrift und wählen Sie dann **Spalte fixieren**. Wenn Sie diesen Schritt zum ersten Mal ausführen, wird die ausgewählte Spalte zur ersten Spalte und wird nicht mehr aus der Ansicht gescrollt. Jede nachfolgende Spalte, die Sie fixieren, wird rechts von der letzten fixierten Spalte hinzugefügt. Sie können die Standardfunktion zum Verschieben verwenden, um fixierte Spalten nach Bedarf neu anzuordnen. Fixierte Spalten können jedoch nicht verschoben werden, sodass sie in der Gruppe der nicht fixierten Spalten angezeigt werden. Ebenso können nicht fixierte Spalten nicht verschoben werden, sodass sie in der Gruppe der fixierten Spalten angezeigt werden.

Um die Fixierung einer Spalte aufzuheben, klicken Sie mit der rechten Maustaste in die Überschrift der fixierten Spalte, und wählen Sie dann **Spaltenfixierung aufheben**. 

Beachten Sie, dass die Zeilenauswahl- und Zeilenstatusspalten im neuen Raster immer als die ersten beiden Spalten fixiert werden. Wenn diese Spalten in einem Raster enthalten sind, sind sie für Benutzer unabhängig von der horizontalen Bildlaufposition im Raster immer sichtbar. Diese beiden Spalten können nicht neu angeordnet werden.

## <a name="autofit-column-width"></a>Spaltenbreite automatisch anpassen
Ähnlich wie in Excel können Benutzer automatisch die Größenänderung einer Spalte basierend auf dem aktuell in dieser Spalte angezeigten Inhalt erzwingen. Doppelklicken Sie dazu auf die Ziehpunkte in der Spalte, oder setzen Sie den Fokus auf die Spaltenüberschrift und drücken Sie **A** (für automatische Anpassung). Diese Funktion ist ab Version 10.0.23 verfügbar.

## <a name="frequently-asked-questions"></a>Häufig gestellte Fragen
### <a name="how-do-i-enable-the-new-grid-control-in-my-environment"></a>Wie aktiviere ich die neue Rastersteuerung in meiner Umgebung? 

Die Funktion **Neue Rastersteuerung** ist in jeder Umgebung direkt in der Funktionsverwaltung verfügbar. Nachdem die Funktion in der Funktionsverwaltung aktiviert wurde, verwenden alle nachfolgenden Benutzersitzungen die neue Rastersteuerung. 

Diese Funktion ist ab Version 10.0.21 standardmäßig aktiviert und soll im Oktober 2022 obligatorisch werden.  

## <a name="developer-opting-out-individual-pages-from-using-the-new-grid"></a>[Entwickler] Deaktivierung einzelner Seiten für die Verwendung des neuen Rasters 
Wenn Ihre Organisation eine Seite entdeckt, bei der Probleme bei der Verwendung des neuen Rasters auftreten, steht eine API zur Verfügung, mit der ein einzelnes Formular die Vorgängerrastersteuerung und der Rest des Systems weiterhin die neue Rastersteuerung verwenden kann. Fügen Sie den folgenden Aufruf `super()` in die `run()` Methode für das Formular ein, um das Raster für eine einzelne Seite zu deaktivieren.

```this.forceLegacyGrid();```

Diese API wird beibehalten, bis das neue Rastersteuerelement obligatorisch wird. Diese Änderung ist derzeit für Oktober 2022 vorgesehen. Wenn Probleme die Verwendung dieser API erfordern, melden Sie diese an Microsoft.

### <a name="forcing-a-page-to-use-the-new-grid-after-previously-opting-out-the-grid"></a>Erzwingen, dass eine Seite das neue Raster verwendet, nachdem das Raster zuvor deaktiviert wurde
Wenn Sie eine einzelne Seite von der Verwendung des neuen Rasters abgemeldet haben, möchten Sie das neue Raster möglicherweise später wieder aktivieren, nachdem die zugrunde liegenden Probleme behoben wurden. Dazu müssen Sie lediglich den Aufruf von `forceLegacyGrid()` entfernen. Die Änderung wird erst wirksam, wenn eine der folgenden Bedingungen eintritt:

- **Erneute Bereitstellung der Umgebung**: Wenn eine Umgebung aktualisiert und erneut bereitgestellt wird, wird die Tabelle, die die Seiten speichert, die sich aus dem neuen Raster abgemeldet haben (FormControlReactGridState), automatisch gelöscht.
- **Manuelles Löschen der Tabelleninhalte**: Für Entwicklungsszenarien müssen Sie SQL verwenden, um die Inhalte der FormControlReactGridState-Tabelle zu löschen und dann den AOS neu zu starten. Diese Kombination von Aktivitäten setzt die Zwischenspeicherung von Seiten zurück, die sich vom neuen Raster abgemeldet haben.

## <a name="developer-opting-individual-grids-out-of-the-typing-ahead-of-the-system-capability"></a>[Entwickler] Einzelne Raster aus der Funktionalität Typing ahead of the system herausnehmen
Es gibt einige Szenarien, die sich nicht gut für die *Typisierung vor dem System* Funktionalität des Rasters eignen. (Einige Codes, die bei der Validierung einer Zeile ausgelöst werden, führen beispielsweise dazu, dass eine Datenquellenrecherche ausgelöst wird, und die Recherche kann dann unbestätigte Änderungen an bestehenden Zeilen beschädigen.) Wenn Ihr Unternehmen ein solches Szenario entdeckt, steht eine API zur Verfügung, mit der ein Entwickler ein einzelnes Raster von der asynchronen Zeilenvalidierung ausnehmen und zum veralteten Verhalten zurückkehren kann.

Wenn die asynchrone Zeilenvalidierung in einem Raster deaktiviert ist, können Benutzer keine neue Zeile erstellen oder zu einer anderen bestehenden Zeile im Raster wechseln, während in der aktuellen Zeile Validierungsprobleme bestehen. Ein Nebeneffekt dieser Aktion ist, dass Tabellen nicht aus Excel in Finance und Operations Raster eingefügt werden können.

Um ein einzelnes Raster von der asynchronen Zeilenvalidierung auszunehmen, fügen Sie in der Methode `run()` des Formulars den folgenden Aufruf nach `super()` ein.

```<gridControl>.allowPreemptiveClient(false);```

> [!NOTE]
> - Dieser Aufruf sollte nur in Ausnahmefällen aufgerufen werden und nicht für alle Raster die Norm sein.
> - Es wird nicht empfohlen, diese API zur Laufzeit nach dem Laden des Formulars umzuschalten.

## <a name="developer-size-to-available-width-columns"></a>[Entwickler] Spalten mit bis zur verfügbaren Breite angepasster Größe
Wenn ein Entwickler die **WidthMode**-Eigenschaft bei Spalten innerhalb des neuen Rasters auf **SizeToAvailable** festlegt, haben diese Spalten zunächst dieselbe Breite wie bei einer Einstellung der Eigenschaft **SizeToContent**. Sie dehnen sich jedoch, um jede zusätzliche verfügbare Breite innerhalb des Rasters zu nutzen. Wenn die Eigenschaft bei mehreren Spalten auf **SizeToAvailable** festgelegt ist, teilen sich alle diese Spalten die zusätzliche verfügbare Breite innerhalb des Rasters. Wenn ein Benutzer jedoch die Größe einer dieser Spalten manuell ändert, wird die Spalte statisch. Sie bleibt auf dieser Breite und wird nicht mehr gedehnt, um die zusätzliche verfügbare Rasterbreite einzunehmen.

## <a name="known-issues"></a>Bekannte Probleme
In diesem Abschnitt wird eine Liste bekannter Probleme für die neue Rastersteuerung aufgeführt.

### <a name="open-issues"></a>Bekannte Probleme
- Nach dem Aktivieren der Funktion **Neue Rastersteuerung** werden einige Seiten weiterhin die vorhandene Rastersteuerung verwenden. Dies geschieht in den folgenden Situationen:
 
    - Auf der Seite gibt es eine Kartenliste, die in mehreren Spalten gerendert ist.
    - Auf der Seite gibt es eine gruppierte Kartenliste.
    - Eine Rasterspalte mit einem nicht reagierenden erweiterbaren Steuerelement.

    Tritt diese Situation zum ersten Mal auf, wird eine Meldung zum Aktualisieren der Seite angezeigt. Nachdem diese Meldung angezeigt wird, verwendet die Seite das vorhandene Raster für alle Benutzer bis zur nächsten Aktualisierung der Produktversion weiter. Für ein zukünftiges Update wird an einem besseren Umgang mit diesen Szenarien gearbeitet, damit das neue Raster genutzt werden kann.

- [KB 4582758] Datensätze sind verschwommen, wenn Sie den Zoom von 100 auf einen anderen Prozentsatz ändern
- [KB 4592012] Unerwarteter Clientfehler in IE11 beim Einfügen mehrerer Zeilen aus Excel

    Microsoft verfolgt keine Lösung für dieses Problem


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
