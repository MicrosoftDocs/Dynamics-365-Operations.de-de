---
title: Verwenden eines Gantt-Diagramms für die Feinterminierung
description: Produktionsplaner können Produktionspläne steuern und optimieren, indem Gantt-Diagramme verwendet werden.
author: johanhoffmann
manager: tfehr
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgShopSupervisorWorkspace, ProdTable, ProdTableListPage, GanttColorTable, GanttReqExplosionColor, GanttReqExplosionSetup, GanttTable, GanttTimescaleSetup, GanttWrkCtr, GanttWrkCtrColor, GanttWrkCtrJobInfo, GanttWrkCtrLoadResources, GanttWrkCtrMoveJob, GanttWrkCtrSetup, GanttWrkCtrView
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 99a7955178ae97e5b696fce04c665d9a251c4a0e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5215864"
---
# <a name="gantt-chart-for-job-scheduling"></a>Verwenden eines Gantt-Diagramms für die Feinterminierung

[!include [banner](../includes/banner.md)]

Das Gantt-Diagramm wurde so entworfen, dass bevollmächtige Produktionsplaner den Produktionsplan steuern und optimieren können. Im Gantt-Diagramm können einfach Fluss Arbeitsgängen angezeigt und der Produktionsplan bei gleichzeitiger Berücksichtigung der Material- oder Ressourcenmängeln angepasst werden. Dadurch wird der Terminplanern die verfügbaren Ressourcen optimal nutzen, die Arbeit minimieren und die Durchsatzzeiten für Produktionsaufträge optimieren.

Ein Gantt-Diagramm ist eine visuelle Darstellung von geplanten Aktivitäten innerhalb eines definierten Zeitintervalls. Die Aktivitäten werden für Ressourcen geplant, die die Kapazität haben, die von einem Kapazitätskalender definiert wird. Folgende Aktivitätstypen im Gantt-Diagramm können angezeigt werden.

-   Hiermit werden die geplanten Einzelvorgänge von Produktionsaufträgen angezeigt.
-   Umwandeln von geplanten Produktionsaufträgen.
-   Einzelvorgang geplanter Projektvorgänge vom Typ Stundenplanungen.

Das Gantt-Diagramm kann in zwei unterschiedlichen Ansichten geöffnet werden, **Auftragsansicht** und **Ressourcenansicht**. In **Auftragsansicht** werden unter Produktionsaufträgen Aktivitäten gruppiert. Dies kann hilfreich sein z.B um eine Übersicht über alle Einzelvorgänge zu erhalten, die verwaltet werden sollen, die dem gleichen Aufträge gehören. In **Ressourcenansicht** werden alle Einzelvorgänge unter einzelnen Ressourcen gruppiert. Diese Ansicht ist hilfreich, wenn Sie den Plan in einem Ressourcenniveau, beispielsweise einer Maschine oder einer Gruppe von Computern optimieren. Die angezeigten Gantt-Diagramme in der Abbildung zeigen **Auftragsansicht** und **Ressourcenansicht** mit diesen zentralen Elementen:

1.  Gantt-Diagramm-Aktivität
2.  Materialmangel-Symbol
3.  Materialverfügbarkeits-Symbol
4.  Auftragslieferdatum-Symbol
5.  Kapazitätsleiste

## <a name="order-view"></a>Auftragsansicht

[![Auftragsansicht](./media/orderview.png)](./media/orderview.png)

## <a name="resource-view"></a>Ressourcenansicht
[![Ressourcenansicht](./media/resview.png)](./media/resview.png)

## <a name="activities"></a>Aktivitäten
Die Aktivitäten werden als Striche angezeigt und sind in einem Zeitskalaraster mit einer geplanten Start- und Endzeit organisiert und treffen die Länge für die Abwicklung, die sich auf die Zeit bezieht, die erforderlich ist, um die Aktivität zu beenden. Die Aktivitäten werden entsprechend einer Zeitskala angezeigt. Sie können die Zeitskala im Menü, wo Sie ein Start- und ein Enddatum und eine Zeiteinheit, beispielsweise, Stunden oder Tagen auswählen. Durch das Anpassen der Zeitskala können Sie das Ziel in einem Zeitintervall festlegen, in dem Sie Aktivitäten verwalten möchten. 

Um einen besseren Überblick abzurufen, gibt es verschiedene Optionen zum Steuern der Farbe der Aktivitäten. Sie können eine einzelne Farbe für Aktivitäten konfigurieren, die Themenfarbe verwenden, die das allgemeine Farbenthema für die Anwendung ist oder die Farbe so einrichten, dass sie durch Farbcodes für Produktionsaufträge gesteuert wird. 

Das Zeitintervall für Aktivitäten hat einen Hintergrundschatten. Perioden mit einem weißen Schatten geben ein Zeitintervall mit der definierten Kapazität der Ressource für die Aktivität an, wohingegen in Perioden mit einem grauen Schatten Zeitintervallen ohne die festgelegte Kapazität angeben werden. 

Link des Diagramms sind noch einige zusätzliche Informationen zur Aktivität, beispielsweise die Ressource, in der die Aktivität geplant ist und die Produktionsauftragsnummer aufgeführt.und geplant wird. Die Verknüpfung zwischen Einzelvorgängen, die demselben Auftrag gehören, wird mit einem Pfeil angezeigt. 

Sie können weitere Informationen über eine Aktivität im Dialogfeld "Aktivitäten" abrufen. Um das Dialogfeld zu öffnen, doppelklicken Sie auf die Aktivität oder aktivieren Sie das Menü **Informationen** aus. Sie können im Dialogfeld "Aktivitäten" das geplante Start- und Enddatum und die Zeitinformation sehen, und sehen, welche geplanten Aktivitäten Materialien brauchen. 

Die Aktivitäten können in den Gruppierungsebenen gruppiert werden. Die Gruppierungsebenen sind hierarchisch und können verwendet werden, um eine logische Gruppierung von Aktivitäten zu aktivieren. Wenn Sie beispielsweise ein Layout haben, in dem Unternehmensaktivitäten, Produktionseinheiten, Ressourcengruppen und Ressourcen gruppiert dargestellt werden, können Sie die Gruppierungsebenen verwenden, um die Aktivitäten entsprechend diesem Layout zu gruppieren. Die Gruppierungsebenen können entweder für einzelne oder für alle Gruppierungsebenen in der Grafik erweitert oder reduziert werden, indem Sie im Menü **Alle erweitern** und **Alle reduzieren** anklicken. Sie können auch die Gruppierungsebenen erweitern oder reduzieren, wenn das Diagramm geöffnet ist.

### <a name="material-availability"></a>Materialverfügbarkeit

Das Gantt-Diagramm kann eingerichtet werden, um den Planer mit detaillierten Informationen zu Status für die einzelnen Aktivitäten zu ermöglichen. Diese Option kann beispielsweise hilfreich sein, wenn Material verzögert wird und den Produktionsplan betroffen. In diesem Fall werden Abgänge im Gantt-Diagramm hervorgehoben, damit der Planer die Konsequenzen besser versteht und Anpassen vornehmen kann. 

Ein Einzelvorgang erscheint mit einem Symbol Mangel, wenn das Zeitplanstartdatum des Einzelvorgangs spätere ist, als der Verfügbarkeitstermin für die Materialien, die für den Einzelvorgang verbraucht werden. Das Materialverfügbarkeitsdatum wird basierend auf der Bedarfsverursacherinformation im dynamischen Produktprogrammplan berechnet. Das Symbol Mangel wird beispielsweise für einen Einzelvorgang angezeigt, der Material verbraucht, das vom Bedarfsverurscher als Bestellung erfolgt, dessen Empfang später ist als das geplante Datum des Einzelvorgangs.

### <a name="indicator-of-material-availability-date"></a>Indikator für das Materialverfügbarkeitsdatum

Wenn Sie das gewünschte Diagramm einrichten, um Einzelvorgänge mit dem Symbol Mängel für das Anzeigen von Verfügbarkeitstermin anzuzeigen, kann der Einzelvorgang angezeigt werden. Das Symbol wird nur angezeigt, wenn der Verfügbarkeitstermin innerhalb des definierten Zeitintervalls des Diagramms ist. Wenn das Verfügbarkeitsdatum außerhalb des definierten Zeitintervalls liegt, dann kann die ausführlichere Materialverfügbarkeits-Informationen aus der Liste im Dialogfeld Einzelvorgang abgerufen werden. In der Liste wird zudem ein Symbol angezeigt, das verspätetes Material für den Einzelvorgang anzeigt. Sie können einen Einzelvorgang mithilfe des Verfügbarkeitstermins als Startdatum neu planen.

### <a name="indicator-of-order-delivery-date"></a>Anzeige des Auftragslieferdatums

Dieses Symbol gibt das Lieferdatum für einen Produktionsauftrag an. Das Symbol ist in der Auftragsansicht sichtbar.

### <a name="capacity-bar"></a>Kapazitätsleiste

Sie können das Diagramm konfigurieren, um eine Ressourcenkapazitätsleiste anzuzeigen. Die Informationsleiste enthält einen Überblick der Ressourcenkapazität für eine Aktivität im angegebenen Zeitintervall des Diagramms bereit. Die Kapazitätsleiste wird nicht für Perioden angezeigt, in der die Ressource nicht gebucht wurde. In Perioden, in denen Ressourcen für die Kapazität gebucht werden, wird die Kapazitätsleiste als ausgefüllte Leiste angezeigt. In Perioden, in denen Ressource überbucht werden, erscheint die Leiste stärker und in roter Farbe. Wenn beispielsweise zwei Stellen überlappen, gibt die Kapazitätsleiste in einem überbuchten Zeitintervall an, wo es eine Überlappung gibt. Die Kapazitätsleiste wird dynamisch aktualisiert, wenn ein Einzelvorgang geplant ist. Sie aktivieren die Kapazitätsleiste im Menü **Kapazitätsleiste anzeigen**. Sie kann nur in der **Ressourcenansicht** angezeigt werden. Wenn Sie eine detailliertere Ansicht der Kapazitätsauslastung für eine Ressource abrufen möchten, verwenden Sie das Diagramm **Kapazitätsauslastung** im Menü oder im Kontextmenü für eine bestimmte Aktivität.

## <a name="job-scheduling-in-the-gantt-chart"></a>Wählen Sie im Gantt-Diagramm einen Einzelvorgang aus.
Das Gantt-Diagramm bietet verschiedene Optionen zum Vornehmen von Regulierungen im Produktionsplan an. Im Gantt-Diagramm können Aktivitäten als Drag & Drop-Interaktion oder über ein Zeitplanmenü geplant werden. Im Planungsprozess können Sie die Ressourcen, die Ressourcenkapazität und die Materialeinschränkungen berücksichtigen.

### <a name="schedule-a-job-as-a-drag-and-drop-interaction"></a>Planen eines Einzelvorgangs als Drag & Drop-Interaktion

Sie können einen Einzelvorgang innerhalb des definierten Zeitintervalls als Drag & Drop-Interaktion neu planen. Sie können den Einzelvorgang in der gleichen Ressource nur neu planen, und Sie können nur einen Einzelvorgang gleichzeitig planen.

### <a name="schedule-a-job-from-the-menu"></a>Einen Einzelvorgang vom Menü planen

Wählen Sie im Menü **Einzelvorgänge planen** einen oder mehrere Einzelvorgänge im Diagramm Planung auf einer Planungsrichtung und für ein Planungsdatums-/uhrzeit aus. Dazu stehen drei unterschiedliche Methoden zur Verfügung.

-   Vorwärts ab Planungsdatum
-   Rückwärts ab Planungsdatum
-   Ab Materialverfügbarkeitsdatum vortragen

Es ist nicht möglich, einen Einzelvorgang außerhalb des definierten Zeitintervalls des Gantt-Diagramms zu planen. Wenn Sie das tun, wird der Einzelvorgang ungeplant belassen und die Fehlermeldung "Einzelvorgang konnte in der geladenen Zeitperiode nicht geplant werde" wird angezeigt.

### <a name="schedule-previous-jobs"></a>Vorherige Einzelvorgänge planen

In einem Netzwerk von Aktivitäten, wie Einzelvorgänge, die demselben Produktionsauftrag angehören, können Sie die Funktion **Vorherige Einzelvorgänge planen** verwenden, um vorherige Einzelvorgänge eines ausgewählten Einzelvorgangs im Netzwerk zu planen. Im folgenden Beispiel ist die markierte Aktivität der ausgewählte Einzelvorgang. Das Diagramm wird angezeigt, bevor ein vorheriger Einzelvorgang geplant wird und nachdem der vorherige Einzelvorgang geplant wird. 

[![Vorherigen Einzelvorgang planen](./media/schprevjob3.png)](./media/schprevjob3.png)

### <a name="schedule-next-jobs"></a>Nächste Einzelvorgänge planen

Sie können die Funktion **Nächste Einzelvorgänge planen** verwenden, um die folgenden Stellen in einem ausgewählten Einzelvorgang in einem Netzwerk von Aktivitäten zu planen. Im folgenden Beispiel ist die markierte Aktivität der ausgewählte Einzelvorgang. Das Diagramm wird angezeigt, bevor der nächste Einzelvorgang geplant wird und nachdem der nächste Einzelvorgang geplant wird. 

[![Nächsten Einzelvorgang planen](./media/schnxtjob.png)](./media/schnxtjob.png)

### <a name="schedule-around-job"></a>Um Einzelvorgang herum planen

Sie können die Funktion **Nächste Einzelvorgänge planen** verwenden, um die folgenden Stellen in einem ausgewählten Einzelvorgang in einem Netzwerk von Aktivitäten zu planen. Im folgenden Beispiel ist die markierte Aktivität der ausgewählte Einzelvorgang. Das Diagramm wird angezeigt, bevor ein Einzelvorgang geplant wird und nachdem der Einzelvorgang geplant wird. 

[![Um Einzelvorgang herum planen](./media/scharoundjob1.png)](./media/scharoundjob1.png)

### <a name="arrange-jobs"></a>Einzelvorgänge anordnen

Sie können die Funktion **Anordnen** verwenden, um die ausgewählten Aktivitäten auf der gleichen Ressource anzuordnen. Diese Aktivitäten werden im gleichen Netzwerk von Aktivitäten sein, können aber auch verschiedenen Netzwerken angehören. Wenn Sie die Anordnensfunktion verwenden, werden die Zeitlücken zwischen den ausgewählten Aktivitäten gelöscht. Sie können diese Funktion verwenden, um die Kapazitätsauslastung der Ressourcen zu optimieren. Das Diagramm wird angezeigt, bevor ein Einzelvorgang geplant wird und nachdem der Einzelvorgang geplant wird. 

[![Einzelvorgang anordnen](./media/arrangejobs1.png)](./media/arrangejobs1.png)

### <a name="reassign-activities-from-one-resource-to-another"></a>Einzelvorgänge zwischen Ressourcen neu zuweisen

Einzelvorgänge zwischen Ressourcen neu zuweisen. Dies kann in den folgenden Situationen hilfreich, in denen eine Maschine gestört oder geüberbucht ist, und Sie müssen ein andere verfügbare Durchschnitt finden, das der Arbeit erledigen kann.

### <a name="reassigning-an-activity-as-a-drag-and-drop-interaction"></a>Eine Aktivität als Drag & Drop-Interaktion neu zuweisen

In der Ansicht **Ressource** können Sie eine Aktivität für eine andere Ressource im Gantt-Diagramm als Drag & Drop-Interaktion neu zuweisen. Sie gehen Sie folgendermaßen, indem Sie die entsprechende Zeile auswählen, in der die Aktivität geplant ist. Nachdem die Zeile ausgewählt ist, können Sie die Zeile der Ressource im Diagramm ziehen, das unter einer anderen Ressourcengruppierungsebene gruppiert wird.

### <a name="reassigning-an-activity-from-the-schedule-jobs-menu"></a>Eine Aktivität neu zuweisen Zeitplaneinzelvorgangsmenü

Sie können einen Einzelvorgang im **Zeitplaneinzelvorgang** aus dem Menü **Zeitplaneinzelvorgang** neu zuweisen. Von diesem Menü können Sie einen Einzelvorgang einer Ressource nur zuweisen, die bereits mit dem Gantt-Diagramm geladen ist. Wenn Sie nur einen Einzelvorgang auswählen, dann wird die Dropdownauswahl für die Ressource durch anwendbare Ressourcen sortiert. Wenn Sie mehrere Stellen auswählen, gibt es keine entsprechende Informationen zu Ressourcen der Ressourcenliste.

## <a name="load-additional-resources-to-the-gantt-chart"></a>Zusätzliche Ressourcen mit dem Gantt-Diagramm laden
In der **Ressourcenansicht** haben Sie eine Option, weitere Ressourcen für das Gantt-Diagramm zu laden. Dies kann hilfreich sein, wenn Sie eine andere Ressource für einen Einzelvorgang suchen möchten, der für eine Maschine geplant ist, die überbucht oder defekt ist. Auf der Seite **Auslastung zusätzlicher Ressourcen** wird eine Liste mit Ressourcen angezeigt, ab der das Datum gilt, das entsprechend dem in der Liste geöffneten Datum passt. Anwendbare Ressourcen, im Verhältnis zu einem bestimmten Einzelvorgang im Gantt-Diagramm, werden zuerst aufgeführt. Wenn Sie mehrere Einzelvorgänge vor dem Öffnen ausgewählt haben, wird kein Hinweis auf entsprechende Ressourcen angezeigt. Auf der Seite **Auslastung zusätzlicher Ressourcen** können Sie eine oder mehrere Ressourcen auswählen, die mit dem Gantt-Diagramm geladen werden, wenn Sie Ihre Auswahl bestätigen. Wenn keine Aufträge vorhanden sind, die in der ausgewählten Ressource im Zeitintervall des Gantt-Diagramms geplant werden, wird die Ressource in Ressourcengruppierungsebene unter eine am Fuß der Liste von Aktivitäten im Gantt-Diagramm erteilt.

### <a name="access-the-gantt-chart"></a>Auf Gantt-Diagramm zugreifen

Die Gantt-Diagramm können auf den folgenden Seiten geöffnet werden.


|                                                 <strong>Seite</strong>                                                  |                                                                                                                                                                                                                                                            <strong>Beschreibung</strong>                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|                                   <strong>Produktionsauftragsliste und -Detail</strong>                                    | Auf der Seite <strong>Produktionsauftragsliste und -Detail</strong> können Sie das Gantt-Diagramm aus mindestens einem ausgewählten Auftrag öffnen. Das Diagramm aus dem Menü <strong>Gantt-Diagramm</strong> wird alle Einzelvorgänge, die sich auf die ausgewählten Produktionsaufträge beziehen und mit den ausgewählten Produktionsaufträgen übereinstimmen laden, aber auch Aufträge von anderen Produktionsaufträgen, die auf den gleichen Ressourcen geplant werden. Das Diagramm aus der Menüansicht <strong>Inforegister – Gantt-Diagramm</strong> lädt nur die Einzelvorgänge, die auf die ausgewählten Produktionsaufträge beziehen. In dieser Ansicht ist es nicht möglich, um Einzelvorgänge zu planen. |
|                                               <strong>Ressource</strong>                                                |                                                                                                                                                        Auf der Seite <strong>Ressource</strong> können Sie das Gantt-Diagramm über die Menüoption <strong>Gantt-Diagramm</strong> öffnen. Wenn diese Option aktiviert ist, werden alle Einzelvorgänge, die für die Ressource in einem ausgewählten Zeitintervall eingeplant sind, z Diagramm geladen.                                                                                                                                                         |
|                                            <strong>Ressourcengruppe</strong>                                             |                                                                                                                                                 Auf der Seite <strong>Ressourcengruppe</strong> können Sie das Gantt-Diagramm über die Menüoption <strong>Gantt-Diagramm</strong> öffnen. Wenn diese Option aktiviert ist, werden alle Einzelvorgänge, die für die Ressource in einem ausgewählten Zeitintervall eingeplant sind, z Diagramm geladen.                                                                                                                                                 |
|                                             <strong>Gantt-Diagramme</strong>                                              |                                                                                 Auf der Seite <strong>Gantt-Diagramme</strong> können Sie Gantt-Diagramme nach Ressourcen und Ressourcengruppen konfigurieren. Wenn Sie z Produktionsaktivitäten für bestimmte Sätze Ressourcen oder Ressourcengruppen steuern möchten, dann können einzelnen Konfigurationen aus denen auf der Seite <strong>Gantt-Diagramme</strong> durchführen. Sie können das Gantt-Diagramm von den einzelnen Konfigurationen öffnen dann.                                                                                 |
|                                       <strong>Stundenplanungen</strong> (Projekt)                                        |                                                                                                                              Einzelvorgang geplanter Projektvorgänge vom Typ <strong>Stundenplanungen</strong>. Auf der Seite <strong>Stundenplanung</strong> im Menü <strong>Planung</strong> können Sie das Gantt-Diagramm in einem Auftrag öffnen, um geplante Projektvorgänge vom Typ Stundenplanung für einen Einzelvorgang anzuzeigen.                                                                                                                               |
|           <strong>Abschluss des Einzelvorgangs</strong> (Liste im Arbeitsbereich <strong>Produktionsbodenverwaltung</strong>)            |                                                                                               Der Arbeitsbereich <strong>Einzelvorgänge der vollständigen Liste in der Produktionsverwaltung</strong> zeigt Einzelvorgänge von der Produktion und Chargenaufträge, die für die ausgewählten Ressourcen für den Arbeitsbereich in Bearbeitung sind. Auf der Menüoption <strong>Gantt-Diagramm</strong> können Sie das Gantt-Diagramm öffnen, in dem alle Einzelvorgänge, die in der Liste ausgewählt werden, im Diagramm geladen werden.                                                                                               |
| <strong>Freigeben von Produktionsaufträgen</strong> (aus dem Arbeitsbereich <strong>Produktionsbodenverwaltung</strong> ) |                                                                                                                                         Freigeben von Produktionsaufträgen im Arbeitsbereich <strong>Produktionsverwaltung</strong>. Diese Seite enthält geplante Produktions- und Chargenaufträge der hängigen Freigabe. Auf dieser Seite können Sie für das ausgewählte Gantt-Diagramm Produktionsaufträge öffnen.                                                                                                                                          |

## <a name="additional-resources"></a>Zusätzliche Ressourcen  
[Visuelle Zeitplanung mit Gantt-Diagramm für Produktions- und Chargenaufträge (Video)](https://youtu.be/BtbuShkGj4I)

[Sichtplanung für Produktion (Vorführungsskript)](https://docs.microsoft.com/dynamics/s-e/)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]