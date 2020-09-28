---
title: Rasterfunktionen
description: In diesem Thema werden mehrere leistungsstarke Funktionen der Rastersteuerung beschrieben. Die neue Rasterfunktion muss aktiviert sein, damit auf diese Fähigkeiten zugegriffen werden kann.
author: jasongre
manager: AnnBe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DefaultDashboard
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: b4efad8423ab42bf6f7f6e2d1054307c11d31d2c
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760398"
---
# <a name="grid-capabilities"></a>Rasterfunktionen

[!include [banner](../includes/banner.md)]

Die neue Rastersteuerung bietet eine Reihe nützlicher und leistungsfähiger Funktionen, mit denen die Benutzerproduktivität gesteigert, interessantere Ansichten Ihrer Daten erstellt und Sie aussagekräftige Einblicke in Ihre Daten gewinnen können. Dieser Artikel deckt die folgenden Funktionen ab: 

-  Summen berechnen
-  Type-ahead
-  Auswerten von mathematischen Ausdrücken 
-  Gruppieren von Tabellendaten (separat mit der **(Vorschau) Gruppierung in Rastern**-Funktion aktiviert)

## <a name="calculating-totals"></a>Summen berechnen
In Finance and Operations-Apps haben Benutzer die Möglichkeit, Summen am unteren Rand numerischer Spalten in Rastern anzuzeigen. Diese Summen werden in einem Fußzeilenbereich am unteren Rand des Rasters angezeigt. 

### <a name="showing-the-grid-footer"></a>Anzeigen der Rasterfußzeile
In den Finance and Operations-Apps gibt es am unteren Rand jedes Tabellenrasters einen Fußbereich. In der Fußzeile können wertvolle Informationen angezeigt werden, die sich auf die im Gitter angezeigten Daten beziehen. Hier sind einige Beispiele für diese Informationen:

- Die Anzahl der ausgewählten Zeilen in der Tabelle (wenn mehr als ein Datensatz ausgewählt ist)
- Gesamtsummen am unteren Ende konfigurierter, numerischer Spalten
- Die Anzahl von Reihen in einem Dataset 

Diese Fußzeile ist standardmäßig ausgeblendet, kann jedoch problemlos aktiviert werden. Um die Fußzeile für ein Raster anzuzeigen, klicken Sie mit der rechten Maustaste auf eine Spaltenüberschrift im Raster und wählen **Fußzeile anzeigen** aus. Sobald die Fußzeile für ein bestimmtes Raster aktiviert wurde, wird diese Einstellung gespeichert, bis der Benutzer die Fußzeile ausblenden möchte. Dies geschieht über einen Klick mit der rechten Maustaste und der Auswahl von **Fußzeile ausblenden**.  Beachten Sie, dass sich die Position der **Fußzeile anzeigen/Fußzeile ausblenden**-Aktion in zukünftigen Versionen vermutlich ändert. 

### <a name="specifying-columns-with-totals"></a>Angeben von Spalten mit Summen
Derzeit werden keine Spalten konfiguriert, die standardmäßig Summen anzeigen. Stattdessen wird dies als einmalige Einrichtungsaktivität betrachtet, ähnlich wie das Anpassen der Spaltenbreiten in Rastern. Wenn Sie festlegen, dass für eine Spalte Summen angezeigt werden sollen, wird diese Einstellung für den nächsten Besuch der Seite gespeichert.  

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

Wenn die Berechnung zu lange dauert, können Sie den Vorgang abbrechen, indem Sie **Abbrechen** auswählen. Manchmal ist das Dataset jedoch zu groß, um Summen zu berechnen (eine von Ihrer Organisation aufgelegte Beschränkung). In diesem Fall werden Sie aufgefordert, die Daten stärker zu filtern.

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
Benutzer konnten immer Daten aus Rastern in Finance and Operations-Apps mit dem **Nach Excel exportieren**-Mechanismus nach Excel exportieren. Die Möglichkeit, Daten vor dem System einzugeben, ermöglicht es dem neuen Raster jedoch, das Kopieren von Tabellen aus Excel und das direkte Einfügen in Tabellen in Raster in Finance and Operations-Apps zu unterstützen. Die Rasterzelle, von der aus der Einfügevorgang initiiert wird, bestimmt, wo die kopierte Tabelle eingefügt wird. Der Inhalt des Rasters wird durch den Inhalt der kopierten Tabelle überschrieben, außer in zwei Fällen:

- Wenn die Anzahl der Spalten in der kopierten Tabelle die Anzahl der im Raster verbleibenden Spalten überschreitet, wird der Benutzer benachrichtigt, dass die zusätzlichen Spalten ignoriert wurden. 
- Wenn die Anzahl der Zeilen in der kopierten Tabelle die Anzahl der Zeilen im Raster überschreitet, beginnend mit der Einfügeposition, werden die vorhandenen Zellen durch den eingefügten Inhalt überschrieben, und alle zusätzlichen Zeilen aus der kopierten Tabelle werden unten im raster als neue Zeilen eingefügt. 

## <a name="evaluating-math-expressions"></a>Auswerten von mathematischen Ausdrücken
Als Produktivitätssteigerung können Benutzer mathematische Formeln in numerische Zellen in einem Gitter eingeben. Sie müssen die Berechnung nicht in einer Anwendung außerhalb des Systems durchführen. Wenn Sie z.B. **=15\*4** eingeben und dann die Taste **Tab** drücken, um das Feld zu verlassen, wertet das System den Ausdruck aus und speichert einen Wert von **60** für das Feld.

Damit das System einen Wert als Ausdruck erkennt, müssen Sie vor dem Wert ein Gleichheitszeichen (**=**) angeben. Mehr Informationen zu den unterstützten Operatoren und zur Syntax finden Sie unter [Unterstützte mathematische Symbole](http://bugwheels94.github.io/math-expression-evaluator/#supported-maths-symbols).

## <a name="grouping-tabular-data"></a>Gruppieren von Tabellendaten
[!include [preview banner](../includes/preview-banner.md)]

Geschäftsanwender müssen häufig Ad-hoc-Datenanalysen durchführen. Während dies durch das Exportieren von Daten nach Microsoft Excel und der Nutzung von Pivot-Tabellen geschehen kann, ermöglicht die Funktion **(Vorschau) Gruppierung in Rastern**, die von der neuen Rastersteuerungsfunktion abhängt, Benutzern, ihre Tabellendaten auf effektive Weise in Finance and Operations-Apps zu organisieren. Da diese Funktion die **Summen**-Funktion erweitert, ermöglicht die Funktion **Gruppieren** wichtige Einblicke in die Daten zu gewinnen, indem Zwischensummen auf Gruppenebene bereitgestellt werden.

Um diese Funktion zu verwenden, klicken Sie mit der rechten Maustaste auf die Spalte, nach der Sie gruppieren möchten, und wählen die Option für **Nach dieser Spalte gruppieren** aus. Diese Aktion sortiert die Daten nach der ausgewählten Spalte, fügt eine neue **Gruppe nach Spalte** am Anfang des Rasters hinzu und fügt „Kopfzeilen“ am Anfang jeder Gruppe ein. Diese Kopfzeilen enthalten die folgenden Informationen zu jeder Gruppe: 
-  Datenwert für die Gruppe 
-  Spaltenname (Diese Information ist besonders nützlich, wenn mehrere Gruppierungsebenen unterstützt werden).  
-  Anzahl der Datenzeilen in dieser Gruppe
-  Zwischensummen für jede Spalte, die zur Anzeige von Gesamtsummen konfiguriert ist

Wenn [Gespeicherte Ansichten](saved-views.md) aktiviert ist, kann diese Gruppierung im Rahmen der Personalisierung als Teil einer Ansicht gespeichert werden, damit Sie beim nächsten Besuch der Seite schnell darauf zugreifen können.  

Wenn Sie **Gruppe nach dieser Spalte** für eine andere Spalte wählen, wird die ursprüngliche Gruppierung ersetzt, da seit Version 10.0.9/Plattform-Update 33 nur eine Gruppierungsebene unterstützt wird.

Um die Gruppierung in einem Raster rückgängig zu machen, klicken Sie mit der rechten Maustaste auf die Gruppierungsspalte und wählen Sie **Gruppierung aufheben** aus.  

### <a name="expanding-and-collapsing-groups"></a>Gruppen erweitern und reduzieren
Bei der anfänglichen Gruppierung von Daten werden alle Gruppen erweitert. Sie können zusammengefasste Ansichten der Daten erstellen, indem Sie einzelne Gruppen reduzieren, oder Sie können das Erweitern und Reduzieren von Gruppen verwenden, um die Navigation durch die Daten zu erleichtern. Um eine Gruppe zu erweitern oder zu reduzieren, wählen Sie die Schaltfläche Chevron (>) in der entsprechenden Gruppenkopfzeile. Beachten Sie: Der Status zum Erweitern/Reduzieren einzelner Gruppen lautet: **nicht** in der Personalisierung gespeichert.

### <a name="selecting-and-unselecting-rows-at-the-group-level"></a>Auswählen und Aufheben der Auswahl von Zeilen auf Gruppenebene
Auf die gleiche Weise, wie Sie alle Zeilen im Raster auswählen (oder die Auswahl aufheben) können, indem Sie das Kontrollkästchen oben in der ersten Spalte des Rasters aktivieren, können Sie auch alle Zeilen in einer Gruppe schnell auswählen (oder die Auswahl aufheben), indem Sie das Kontrollkästchen in der entsprechenden Gruppenkopfzeile auswählen. Das Kontrollkästchen in der Gruppenkopfzeile gibt immer den aktuellen Auswahlstatus der Zeilen in dieser Gruppe wieder, unabhängig davon, ob alle Zeilen ausgewählt sind, keine Zeilen ausgewählt sind oder nur einige Zeilen ausgewählt sind.

### <a name="hiding-column-names"></a>Spaltennamen ausblenden
Beim Gruppieren von Daten wird standardmäßig der Spaltenname in der Gruppenkopfzeile angezeigt. Ab Version 10.0.14/Plattform-Update 38 können Sie den Spaltennamen in Gruppenkopfzeilen unterdrücken, indem Sie **Rasteroptionen** > **Gruppenspaltennamen ausblenden** auswählen.

## <a name="frequently-asked-questions"></a>Häufig gestellte Fragen
### <a name="how-do-i-enable-the-new-grid-control-in-my-environment"></a>Wie aktiviere ich die neue Rastersteuerung in meiner Umgebung? 

**10.0.9/Plattform-Update 33 und höher** Die Funktion **Neue Rastersteuerung** ist in jeder Umgebung direkt in der Funktionsverwaltung verfügbar. Wie andere öffentliche Vorschaufunktionen unterliegt auch die Aktivierung dieser Funktion in der Produktion den [Zusätzlichen Nutzungsbedingungen](https://go.microsoft.com/fwlink/?linkid=2105274).  

**10.0.8/Plattform-Update 32 und 10.0.7 / Plattform-Update 31** Die Funktion **Neue Rastersteuerung** kann in Stufe 1-Umgebungen (Entwicklung/Test) und Stufe 2-Umgebungen (Sandbox) aktiviert werden, um zusätzliche Test- und Entwurfsänderungen bereitzustellen, indem die folgenden Schritte ausgeführt werden.

1.  **Flight aktivieren**: Führen Sie die folgende SQL-Anweisung aus: 

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, enabled, FLIGHTSERVICEID, PARTITION) VALUES('CLIReactGridEnableFeature', 1, 0, 5637144576);`

2. **Reset IIS** zum Leeren des statischen Flighting-Cache. 

3.  **Finden Sie die Funktion**: Gehen Sie zum Arbeitsbereich **Feature-Management**. Wenn **Neue Rastersteuerung** nicht in der Liste aller Funktionen erscheint, wählen Sie **Auf Updates prüfen**.   

4.  **Aktivieren Sie die Funktion**: Suchen Sie die Funktion **Neue Rastersteuerung** in der Liste der Funktionen und wählen Sie **Jetzt aktivieren** im Detailbereich. Beachten Sie, dass eine Browseraktualisierung erforderlich ist. 

Alle folgenden Benutzersitzungen beginnen mit der aktivierten neuen Rastersteuerung.

## <a name="developer-opting-out-individual-pages-from-using-the-new-grid"></a>[Entwickler] Deaktivierung einzelner Seiten für die Verwendung des neuen Rasters 
Wenn Ihre Organisation eine Seite entdeckt, bei der Probleme bei der Verwendung des neuen Rasters auftreten, steht eine API zur Verfügung, mit der ein einzelnes Formular die Vorgängerrastersteuerung und der Rest des Systems weiterhin die neue Rastersteuerung verwenden kann. Fügen Sie den folgenden Aufruf `super()` in die `run()` Methode des Formulars ein, um das Raster für eine einzelne Seite zu deaktivieren.

 ```this.forceLegacyGrid();```

Diese API wird bis zur Veröffentlichung im Oktober 2021 durchgeführt, danach wird die neue Rastersteuerung obligatorisch. Bitte melden Sie alle Probleme, für die diese API verwendet werden muss, an Microsoft. 

## <a name="known-issues"></a>Bekannte Probleme
In diesem Abschnitt wird eine Liste bekannter Probleme für das neue Rastersteuerelement verwaltet, während sich die Funktion in einem Vorschaustatus befindet.  

### <a name="open-issues"></a>Bekannte Probleme
-  Nach dem Aktivieren der Funktion **Neue Rastersteuerung** werden einige Seiten weiterhin die vorhandene Rastersteuerung verwenden. Dies geschieht in den folgenden Situationen:  
    -  Auf der Seite gibt es eine Kartenliste, die in mehreren Spalten gerendert ist.
    -  Auf der Seite gibt es eine gruppierte Kartenliste.
    -  Eine Rasterspalte mit einem nicht reagierenden erweiterbaren Steuerelement.

    Tritt diese Situation zum ersten Mal auf, wird eine Meldung zum Aktualisieren der Seite angezeigt. Nachdem diese Meldung angezeigt wird, verwendet die Seite das vorhandene Raster für alle Benutzer bis zur nächsten Aktualisierung der Produktversion weiter. Für ein zukünftiges Update wird an einem besseren Umgang mit diesen Szenarien gearbeitet, damit das neue Raster genutzt werden kann.     

### <a name="fixed-as-part-of-10013"></a>Als Teil von 10.0.13 behoben

-  [Bug 470173] Kontrollkästchen in inaktiven Zeilen werden umgeschaltet, wenn auf das Leerzeichen in der Zelle geklickt wird
-  [Bug 474848] Erweiterte Vorschauen mit Rastern werden nicht angezeigt
-  [Bug 474851] Hyperlinks in Referenzgruppensteuerelementen funktionieren nicht 
-  [Bug 471777] Felder in einem Raster können nicht zum Bearbeiten oder Erstellen einer mobilen App ausgewählt werden
-  [KB 4569441] Probleme beim Rendern mehrspaltiger Kartenlisten, QuickInfos für Bilder und Anzeigeoptionen für einige Felder
-  [KB 4575279] Nicht alle markierten Zeilen werden aus der allgemeinen Erfassung gelöscht
-  [KB 4575233] Anzeigeoptionen werden nach dem Verschieben in eine andere Zeile nicht wiederhergestellt
-  [KB 4571095] Die Buchung des Produktzugangs erfolgt, wenn versehentlich die Eingabetaste gedrückt wird (korrekte Behandlung der Standardaktivität einer Seite)
-  [KB 4575437] Suchvorgänge mit bearbeitbaren Steuerelementen werden unerwartet geschlossen
-  [KB 4569418] Doppelte Zeile im Lieferzeitplan erstellt
-  [KB 4575435] Die verbesserte Vorschau bleibt manchmal bestehen, auch wenn sich der Mauszeiger nicht in der Nähe des Felds befindet
-  [KB 4575434] Die Suche filtert nicht, wenn das Feld geändert wurde
-  [KB 4575430] Werte in Kennwortfeldern werden im Raster nicht maskiert
-  [KB 4569438] Nach dem Markieren von Zeilen beim Abwickeln von Lieferantentransaktionen wird „Die Verarbeitung wurde aufgrund eines Validierungsproblems gestoppt“ angezeigt
-  [KB 4569434] Das Aktualisieren des Formulars für juristische Personen führt zu weniger Datensätzen
-  [KB 4575297] Der Fokus bewegt sich beim Bearbeiten und Durchblättern eines Rasters immer wieder zur Aufgabenaufzeichnung
-  [KB 4566773] Korrekturtransaktionen werden bei der Belegbuchungsanfrage nicht als negativ angezeigt 
-  [KB 4575288] Der Fokus wird auf die aktive Zeile zurückgesetzt, wenn die Linie zwischen den Zeilen in einer einfachen Liste ausgewählt wird
-  [KB 4575287] Der Fokus kehrt nicht zur ersten Spalte zurück, wenn mit dem Abwärtspfeil eine neue Zeile in der Erfassung erstellt wird
-  [KB 4564819] Zeilen in einer Freitextrechnung können nicht gelöscht werden (da die Datenquelle ChangeGroupMode = ImplicitInnerOuter)
-  [KB 4563317] QuickInfos/verbesserte Vorschauen werden für Bilder nicht angezeigt

### <a name="fixed-as-part-of-10012"></a>Als Teil von 10.0.12 behoben

- [KB 4558545] Tabellensteuerelemente aktualisieren den Inhalt der angezeigten Elemente nicht.
- [KB 4558570] Elemente werden nach dem Löschen des Datensatzes weiterhin auf der Seite angezeigt.
- [KB 4558572] Stilelemente, die dem Listenfenster **ExtendedStyle** zugeordnet sind, werden nicht angewendet.
- [KB 4558573] Validierungsfehler können nicht behoben werden, wenn sich die erforderliche Änderung außerhalb des Rasters befindet.
- [KB 4558584] Negative Zahlen werden nicht korrekt gerendert.
- [KB 4560726] Ein unerwarteter Clientfehler tritt auf, nachdem der Austausch zwischen Listen mithilfe eines Listenansicht-Steuerelements erfolgt ist.
- [KB 4562141] Rasterindizes sind deaktiviert, nachdem ein neuer Datensatz hinzugefügt wurde.
- [KB 4562151] Die Aufgabenaufzeichnungsoptionen **Überprüfen** und **Kopieren** sind für Datums-/Nummernsteuerelemente nicht verfügbar. 
- [KB 4562153] Mehrfachauswahl-Kontrollkästchen sind in Listen-/Kartenraster nicht sichtbar.
- [KB 4562646] Sie können zeitweise nicht außerhalb des Rasters klicken, nachdem Sie einige Zeilen mehrfach ausgewählt haben.
- [KB 4562647] Fokus wird auf das erste Steuerelement im Dialogfeld **Veröffentlichen** zurückgesetzt, nachdem eine neue Zeile im Sicherheitsrollenraster hinzugefügt wurde.
- [KB 4563310] Die erweiterte Vorschau wird nach dem Ändern einer Zeile nicht geschlossen.
- [KB 4563313] Ein unerwarteter Clientfehler tritt im Internet Explorer auf, wenn ein Wert in einer Suche ausgewählt wird.
- [KB 4564557] Suchvorgänge und Drop-down-Menüs werden nicht im Internet Explorer geöffnet
- [KB 4563324] Navigation funktioniert nachdem der **Personalmanagement** Arbeitsbereich geöffnet wurde.

### <a name="fixed-as-part-of-10011"></a>Als Teil von 10.0.11 behoben

- [Problem 432458] Leere oder doppelte Zeilen werden am Anfang einiger untergeordneter Sammlungen angezeigt.
- [KB 4549711] Zeilen in einem Zahlungsvorschlag können nicht korrekt entfernt werden, nachdem die neue Rastersteuerung aktiviert wurde.
- [KB 4558374] Datensätze, für die ein polymorphes Auswahldialogfeld erforderlich ist, können nicht erstellt werden.
- [KB 4558375] Hilfetext wird in den Spalten des neuen Rasters nicht angezeigt.
- [KB 4558376] Listenbedienfeldraster werden in Internet Explorer nicht in der richtigen Höhe gerendert.
- [KB 4558377] Kombinationsfeldspalten mit **SizeToAvailable**-Breite werden auf einigen Seiten nicht gerendert.
- [KB 4558378] Drillthrough öffnet manchmal den falschen Datensatz.
- [KB 4558379] Ein Fehler tritt auf, wenn Suchvorgänge geöffnet werden, wenn **ReplaceOnLookup**=**Nein** ist.
- [KB 4558380] Der verfügbare Platz im Raster wird nicht sofort nach dem Reduzieren eines Teils der Seite gefüllt.
- [KB 4558381] Negative Zahlen werden nicht korrekt gerendert/Benutzer bleiben manchmal hängen, nachdem Validierungsprobleme aufgetreten sind.
- [KB 4558382] Unerwartete Clientfehler treten auf.
- [KB 4558383] Steuerelemente außerhalb des Rasters werden nicht aktualisiert, nachdem der letzte Datensatz gelöscht wurde.
- [KB 4558587] Referenzgruppen mit Kombinationsfeldern für Ersatzfelder zeigen keine Werte an.
- [KB 4562143] Felder werden nach einem Zeilenwechsel nicht aktualisiert/die Rasterverarbeitung bleibt nach dem Löschen der Zeilen hängen.
- [KB 4562645] Eine Ausnahme tritt auf, wenn eine Suche geöffnet wird, während Remote Server Administration Tools ausgeführt werden.

### <a name="fixed-as-part-of-10010"></a>Als Teil von 10.0.10 behoben

- [Problem 414301] Einige Daten aus vorherigen Zeilen verschwinden, wenn neue Zeilen erstellt werden.
- [Bug 417044] Es gibt keine leere Rastermeldung für Raster im Listenstil.
- [KB 4539058] Einige Raster (normalerweise in Inforegistern) werden manchmal nicht gerendert (aber sie werden gerendert, wenn Sie herauszoomen).
- [KB 4549734] Aktive Zeilen werden nicht als markiert behandelt, wenn die Markierungsspalte ausgeblendet ist.
- [KB 4549796] Werte können im Ansichtsmodus nicht in einem Raster bearbeitet werden.
- [KB 4558367] Die Textauswahl ist inkonsistent, wenn Zeilen geändert werden.
- [KB 4558368] Mehrfachauswahl über die Tastatur ist in Single-Select-Szenarien zulässig.
- [KB 4558369] Statusbilder verschwinden im hierarchischen Raster.
- [KB 4558370] Eine neue Zeile wird nicht in die Ansicht gescrollt.
- [KB 4558372] Das neue Raster bleibt im Verarbeitungsmodus hängen, wenn die Anzahl der eingefügten Spalten im Inhalt die Anzahl der verbleibenden Spalten im Raster überschreitet.
- [KB 4562631] Zeitwerte sind nicht richtig formatiert.

### <a name="quality-update-for-1009platform-update-33"></a>Qualitätsupdate für 10.0.9/Platform update 33

- [KB 4550367] Zeitwerte sind nicht richtig formatiert.
