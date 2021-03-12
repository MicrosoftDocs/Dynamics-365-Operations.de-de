---
title: Einen Produktprogrammplanungslauf überwachen
description: In diesem Abschnitt wird erläutert, wie der Produktionsplaner sehen kann, ob ein Masterplanungslauf läuft.
author: josaw1
manager: tfehr
ms.date: 11/04/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, InventItemIdLookupSimple, ReqLog, ReqProcessTaskTrace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1cbe2c55ef9e3ed35db30ca927f3472c750c1db5
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4999805"
---
# <a name="monitor-a-master-planning-run"></a>Einen Produktprogrammplanungslauf überwachen

[!include [banner](../../includes/banner.md)]

## <a name="use-a-gantt-chart-to-visualize-master-planning-progress"></a>Verwenden Sie ein Gantt-Diagramm, um den Fortschritt der Masterplanung zu visualisieren.

Auf der Seite **Masterplanungsfortschritt anzeigen** können Sie Details zu historischen Masterplanungsläufen als Gantt-Diagramm anzeigen. Diese Funktionalität kann Ihnen helfen, die Zeit zu verstehen, die für die verschiedenen Phasen der Masterplanung aufgewendet wird. Für einen aktuellen aktiven Planungsauftrag kann die Seite **Masterplanungsfortschritt anzeigen** verwendet werden, um den Fortschritt zu verfolgen und die geschätzte Restzeit anzuzeigen.

### <a name="turn-on-and-use-the-master-plan-progress-visualization-feature"></a>Einschalten und Verwenden der Visualisierungsfunktion für den Fortschritt des Masterplans

Um diese Funktionalität zu nutzen, führen Sie die folgenden Schritte aus.

1. Wählen Sie im Arbeitsbereich **Feature-Management** auf der Registerkarte **Neu** **Masterplanung Fortschrittsvisualisierung** in der Liste. Wenn die Funktion nicht auf der Registerkarte **Neu** erscheint, schauen Sie auf die Registerkarten **Nicht aktiviert** und **Alle**.
1. Wählen Sie **Jetzt aktivieren**. Alternativ können Sie auch **Terminplanung** wählen und dann die Zeit auswählen, zu der die Funktion eingeschaltet werden soll.

Auf der Seite **Masterplanungsfortschritt anzeigen** können sowohl historische Planungsaufträge als auch aktive Planungsaufträge angezeigt werden. 

Um Aufträge zur historischen Planung anzuzeigen, gibt es zwei Möglichkeiten. 

1. Gehen Sie zu **Masterplanung \> Einrichtung \> Pläne \> Masterpläne**, und wählen Sie dann im Aktionsbereich **Verlauf**. Wenn der gewünschte Auftrag ausgewählt ist, wählen Sie **Anfragen**, und wählen Sie dann **Fortschritt anzeigen**.
1. Gehen Sie zu **Masterplanung \> Arbeitsbereiche \> Masterplanung**, klicken Sie auf der Masterplantafel auf **Historie**. Wenn der gewünschte Auftrag ausgewählt ist, wählen Sie **Anfragen**, und wählen Sie dann **Fortschritt anzeigen**.

Um aktive Planungsjobs anzuzeigen, gibt es zwei Möglichkeiten. 
1. Gehen Sie zu **Masterplanung \> Arbeitsbereiche \> Masterplanung**, wählen Sie im Aktionsbereich **Unfertiger Planungsprozess**. Wenn der gewünschte Auftrag ausgewählt ist, wählen Sie **Anfragen**, und wählen Sie dann **Fortschritt anzeigen**.
1. Gehen Sie zu **Masterplanung \> Arbeitsbereiche \> Masterplanung**, klicken Sie auf der Masterplantafel auf **Fortschritt anzeigen**. Wenn der gewünschte Auftrag ausgewählt ist, wählen Sie **Anfragen**, und wählen Sie dann **Fortschritt anzeigen**.

Beachten Sie, dass Sie aktive Aufträge nur dann anzeigen können, wenn ein Planungsauftrag bearbeitet wird.

### <a name="analyze-a-master-planning-job"></a>Analysieren eines Masterplanungsauftrags

Im Gantt-Diagramm können Sie jeden der folgenden Planungsprozesse erweitern, um zusätzliche Details über die aufgewendete Zeit anzuzeigen:

- Initialisierung wird ausgeführt
- Daten werden gelöscht und eingefügt.
- Dispositionsplanung
- Verzögerungen
- Aktivitätsmeldungen
- Abschluss
- Automatische Umwandlung

Das Gantt-Diagramm ist ein nützliches Werkzeug, wenn Sie die Auswirkungen der Verwendung von Aktionsnachrichten sehen möchten.

#### <a name="navigation-in-the-gantt-chart"></a>Navigation im Gantt-Diagramm

- Um die ausgewählte Gruppe zu erweitern und die Details anzuzeigen, wählen Sie das Pluszeichen (**+**) in der Baumansicht.
- Um die ausgewählte Gruppe zu komprimieren, wählen Sie das Minuszeichen (**-**) in der Baumansicht.
- Sie können Ihre Tastatur zur Navigation verwenden. Verwenden Sie die Tasten **Pfeil nach oben** und **Pfeil nach unten**, um zwischen den Zeilen zu wechseln. Verwenden Sie die Schaltflächen **Rechter Pfeil** und **Linker Pfeil**, um Gruppen auf- und zuklappen.
- Um alle Ebenen im Gantt-Diagramm zu öffnen oder zu schließen, wählen Sie **Alle erweitern** oder **Alle komprimieren**.
- Um die zugehörige Bearbeitungszeit anzuzeigen, fahren Sie mit der Maus über eine Aufgabe. (Aufgaben sind die unterste Ebene im Gantt-Diagramm.)

#### <a name="view-an-additional-master-planning-run-to-compare-jobs"></a>Anzeigen eines zusätzlichen Masterplanungslaufs zum Vergleich von Jobs

Durch die Auswahl eines Masterplanungsauftrags im Feld **Zeige zusätzlichen Masterplanungslauf** können Sie einen zusätzlichen Masterplanungslauf im Gantt-Diagramm anzeigen und die beiden Aufträge vergleichen.

#### <a name="bom-level-display"></a>Anzeige der Stücklistenstufen

Stücklistenstufen werden für die Disposition, Verzögerungen, Aktionen und Fixierungen unterschiedlich dargestellt.

- **Deckungsplanung** - Stücklistenstufen werden wie erwartet dargestellt. Sie werden von oben nach unten berechnet.

    **Beispiel:** Stücklistenstufe 0, 1, 2

- **Verzögerungen** - Stücklistenstufen werden angezeigt, wenn die Stücklistenstufen der Versorgungsplanung mit -1 multipliziert werden. (Mit anderen Worten, sie haben ein negatives Vorzeichen.)

    **Beispiel:** Stücklistenstufe -2, -1, 0

- **Aktionsmeldung** - Stücklistenstufen werden wie erwartet angezeigt. Sie werden von oben nach unten berechnet.

    **Beispiel:** Stücklistenstufe 0, 1, 2

- **Automatische Umwandlung** - Stücklistenstufen werden mit 999 abzüglich der Versorgungsplanungsstücklistenstufe dargestellt.

    **Beispiel:** Stücklistenstufe 999, 998, 997

Die folgende Tabelle fasst das Verhalten zusammen.

| Stücklistenstufe, die angezeigt wird | Endprodukt | Unterkomponente | Rohmaterial |
|---|---|---|---|
| Dispositionsplanung | 0 | 1 | 2 |
| Verzögerungen | 0 | –1 | –2 |
| Aktivitätsmeldung | 0 | 1 | 2 |
| Automatische Umwandlung | 999 | 998 | 997 |

#### <a name="visualize-progress"></a>Visualisieren des Fortschritts

Wenn Sie einen Masterplanungsauftrag anzeigen, der gerade ausgeführt wird, wird der Fortschritt durch Farben im Gantt-Diagramm angezeigt. Die folgenden Farben gelten für das blaue Thema. Bei anderen Farbthemen sind die Farben unterschiedlich.

- **Dunkelblau** - Erledigte Planungsaufgaben.
- **Orange** - Die Aufgabe, die gerade ausgeführt wird.
- **Hellblau** - Die Schätzung für die verbleibenden Aufgaben.

Die Farbe wird im Gantt-Diagramm nur auf der untersten Ebene angezeigt. Wählen Sie **Alle erweitern**, um alle Aufgaben im Masterplanungsauftrag anzuzeigen. Die Schätzung der verbleibenden Aufgaben basiert auf historischen Masterplanungsaufträgen.

## <a name="run-master-planning-and-track-processing-time"></a>Durchführung der Masterplanung und Verfolgung der Bearbeitungszeit

1. Wählen Sie im Standard-Dashboard **Masterplanung**.
1. Geben Sie im Feld **Plan** einen Wert ein oder wählen Sie ihn aus.
1. Wählen Sie **Ausführen** aus.
1. Stellen Sie die Option **Verarbeitungszeit der Tracks** auf **Ja**.
1. Geben Sie im Feld **Anzahl von Threads** eine Zahl ein.
1. Wählen Sie auf der Seite **Einschließende Datensätze** Inforegister die Option **Filter**.
1. Wählen Sie im Raster die Zeile aus, in der das Feld **Feld** auf **Artikelnummer** gesetzt ist.
1. Geben Sie im Feld **Kriterien** einen Wert ein.
1. Wählen Sie **OK**.
