---
title: Rasterfunktionen
description: In diesem Thema werden mehrere leistungsstarke Funktionen der Rastersteuerung beschrieben. Die neue Rasterfunktion muss aktiviert sein, damit auf diese Fähigkeiten zugegriffen werden kann.
author: jasongre
manager: AnnBe
ms.date: 01/20/2020
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
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: b49d7823f48bcc9cdbb56b87d5fa72d46ddfa15c
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019791"
---
# <a name="grid-capabilites"></a>Rasterfunktionen

[!include [banner](../includes/banner.md)]

Die neue Rastersteuerung bietet eine Reihe nützlicher und leistungsfähiger Funktionen, mit denen die Benutzerproduktivität gesteigert, interessantere Ansichten Ihrer Daten erstellt und Sie aussagekräftige Einblicke in Ihre Daten gewinnen können. Dieser Artikel deckt die folgenden Funktionen ab: 

-  Summen berechnen
-  Daten gruppieren
-  Type-ahead
-  Auswerten von mathematischen Ausdrücken 

## <a name="calculating-totals"></a>Summen berechnen
In Finance and Operations-Apps haben Benutzer die Möglichkeit, Summen am unteren Rand numerischer Spalten in Rastern anzuzeigen. Diese Summen werden in einem Fußzeilenbereich am unteren Rand des Rasters angezeigt. 

### <a name="showing-the-grid-footer"></a>Anzeigen der Rasterfußzeile
Jedes Tabellenraster in den Finance and Operations-Apps hat einen Fußzeilenbereich am unteren Rand des Rasters, in dem wertvolle Informationen zu den angezeigten Daten angezeigt werden können. Diese Informationen umfassen Folgendes: 
-  Die Anzahl der ausgewählten Zeilen in der Tabelle (wenn mehr als ein Datensatz ausgewählt ist)
-  Die Gesamtsummen am unteren Rand der konfigurierten numerischen Spalten
-  Die Anzahl von Reihen in einem Dataset 

Diese Fußzeile ist standardmäßig ausgeblendet, kann jedoch problemlos aktiviert werden. Um die Fußzeile für ein Raster anzuzeigen, klicken Sie mit der rechten Maustaste auf eine Spaltenüberschrift im Raster und wählen **Fußzeile anzeigen** aus. Sobald die Fußzeile für ein bestimmtes Raster aktiviert wurde, wird diese Einstellung gespeichert, bis der Benutzer die Fußzeile ausblenden möchte. Dies geschieht über einen Klick mit der rechten Maustaste und der Auswahl von **Fußzeile ausblenden**.  Beachten Sie, dass sich die Position der **Fußzeile anzeigen/Fußzeile ausblenden**-Aktion in zukünftigen Versionen vermutlich ändert. 

### <a name="specifying-columns-with-totals"></a>Angeben von Spalten mit Summen
Derzeit werden keine Spalten konfiguriert, die standardmäßig Summen anzeigen. Stattdessen wird dies als einmalige Einrichtungsaktivität betrachtet, ähnlich wie das Anpassen der Spaltenbreiten in Rastern. Wenn Sie festlegen, dass für eine Spalte Summen angezeigt werden sollen, wird diese Einstellung für den nächsten Besuch der Seite gespeichert.  

Es gibt zwei Möglichkeiten, eine Spalte so zu konfigurieren, dass eine Summe angezeigt wird: 
1.  Klicken Sie mit der rechten Maustaste auf die Spalte, für die Sie eine Summe anzeigen möchten, und wählen Sie die Option für **Summe für diese Spalte** aus. Diese Aktion bewirkt drei Dinge. Zunächst wird die Fußzeile sichtbar. Zweitens wird Ihre Präferenz für die Anzeige einer Summe in dieser Spalte gespeichert. Drittens wird durch diese Aktion eine Summenberechnung für diese und alle anderen Spalten initiiert, die Sie zuvor für die Anzeige von Summen konfiguriert haben. Die Zeit, die für die Anzeige einer Gesamtsumme benötigt wird, hängt direkt von der Größe des zu summierenden Datasets ab.  

2.  Sobald die Fußzeile angezeigt wurde, können Sie alternativ im Fußzeilenbereich am unteren Rand der Spalte, für die Sie eine Summe anzeigen möchten, auf **Summe anzeigen** klicken. Wenn keine Spalten konfiguriert sind, wird die Schaltfläche **Summe anzeigen** für alle numerischen Spalten angezeigt. Sobald mindestens eine Spalte für Summen konfiguriert ist, wird die Schaltfläche **Summe anzeigen** nur beim Fokussieren oder beim Bewegen der Maus über diese angezeigt. Diese Aktion speichert einfach Ihre Voreinstellung für die Anzeige einer Summe in dieser Spalte für zukünftige Besuche auf dieser Seite. Dieser Status wird durch den Bindestrich in dieser Spalte in der Fußzeile angezeigt (oder es wird sofort eine Summe angezeigt, wenn das Dataset entsprechend klein ist).

Wenn Sie einen Fehler gemacht haben und keine Summe mehr in einer bestimmten Spalte anzeigen möchten, klicken Sie mit der rechten Maustaste auf die Spalte und wählen Sie **Summe ausblenden** aus oder wählen Sie **Summe ausblenden** in der Fußzeile der Spalte aus. Diese Einstellung wird ebenfalls für zukünftige Besuche der Seite gespeichert. 

### <a name="calculating-totals"></a>Summen berechnen
Wenn Sie zu einer Seite mit sichtbarer Fußzeile und Spalten kommen, die bereits für Summen konfiguriert sind, werden Summen möglicherweise in der Fußzeile angezeigt oder nicht. Das Verhalten ist abhängig von der Größe des Datasets auf der Seite. Wenn das Dataset ausreichend klein ist, werden automatisch die Gesamtsummen sowie die Anzahl der Zeilen im Dataset angezeigt. Befinden sich in der Fußzeile unter den Spalten, die Sie für Gesamtsummen konfiguriert haben, Bindestriche, ist das Dataset zu groß für das System, um Gesamtsummen sofort anzuzeigen. Eine explizite Aktion ist erforderlich, um die Gesamtsummen zu berechnen. Klicken Sie dazu auf die Schaltfläche **Berechnung** in der Fußzeile oder klicken Sie mit der rechten Maustaste auf eine Spalte, für die Sie eine Gesamtsumme wünschen, und wählen Sie **Summe für diese Spalte** aus.  

Wenn die Berechnung zu lange dauert, können Sie den Vorgang abbrechen, indem Sie **Abbrechen** auswählen. Manchmal ist das Dataset jedoch zu groß, um Summen zu berechnen (eine von Ihrer Organisation aufgelegte Beschränkung). In diesem Fall werden Sie aufgefordert, die Daten stärker zu filtern.

Die Summen werden automatisch aktualisiert, wenn Sie Zeilen im Dataset aktualisieren, löschen oder erstellen.  

## <a name="grouping-data"></a>Daten gruppieren
Geschäftsanwender müssen häufig Ad-hoc-Datenanalysen durchführen. Während dies durch das Exportieren von Daten nach Microsoft Excel und der Nutzung von Pivot-Tabellen geschehen kann, ermöglicht die Funktion **Gruppieren** in Tabellenrastern Benutzern, ihre Daten auf effektive Weise in Finance and Operations-Apps zu organisieren. Diese Funktion erweitert die **Summen**-Funktion. Die Funktion **Gruppieren** ermöglicht zudem, wichtige Einblicke in die Daten zu gewinnen, indem Zwischensummen auf Gruppenebene bereitgestellt werden.

Um diese Funktion zu verwenden, klicken Sie mit der rechten Maustaste auf die Spalte, nach der Sie gruppieren möchten, und wählen die Option für **Nach dieser Spalte gruppieren** aus. Diese Aktion sortiert die Daten nach der ausgewählten Spalte, fügt eine neue Gruppieren nach Spalte am Anfang des Rasters hinzu und fügt Kopfzeilen am Anfang jeder Gruppe ein. Diese Kopfzeilen enthalten die folgenden Informationen zu jeder Gruppe: 
-  Datenwert für die Gruppe 
-  Spaltenbezeichnung. Dies ist besonders nützlich, wenn mehrere Gruppierungsebenen unterstützt werden.  
-  Anzahl der Datenzeilen in dieser Gruppe
-  Zwischensummen für jede Spalte, die zur Anzeige von Gesamtsummen konfiguriert ist

Wenn [Gespeicherte Ansichten](saved-views.md) aktiviert ist, kann diese Gruppierung im Rahmen der Personalisierung als Teil einer Ansicht gespeichert werden, damit Sie beim nächsten Besuch der Seite schnell darauf zugreifen können.  

Wenn Sie die Option für **Nach dieser Spalte gruppieren** in einer anderen Spalte auswählen, wird die ursprüngliche Gruppierung ersetzt, da in 10.0.9/Plattform-Update 33 nur die Gruppierungsebene unterstützt wird.

Um die Gruppierung in einem Raster rückgängig zu machen, klicken Sie mit der rechten Maustaste auf die Gruppierungsspalte und wählen Sie **Gruppierung aufheben** aus.  


## <a name="evaluating-math-expressions"></a>Auswerten von mathematischen Ausdrücken
Zur Produktivitätssteigerung kann der Benutzer mathematische Formeln in numerische Zellen in einem Raster eingeben, anstatt die Berechnung in einer App außerhalb des Systems durchführen zu lassen. Zum Beispiel können Sie **= 15\*4** eingeben und über die Tabulatortaste das Feld verlassen. Das System wertet den Ausdruck aus und speichert einen Wert von „60“ für das Feld.

Damit das System einen Wert als Ausdruck erkennt, müssen Sie vor dem Wert ein Gleichheitszeichen (**=**) angeben. Weitere Informationen zu den unterstützten Operatoren und zur Syntax finden Sie unter [Unterstützte mathematische Symbole](http://redhivesoftware.github.io/math-expression-evaluator/#supported-maths-symbols).  
