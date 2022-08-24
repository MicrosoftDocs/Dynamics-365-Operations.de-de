---
title: Verbessern der Leistung des Planungsmoduls
description: Dieser Artikel enthält Informationen zum Planungsmodul und zur Verbesserung der Leistung.
author: t-benebo
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: ''
ms.author: benebotg
ms.search.validFrom: 2020-09-03
ms.dyn365.ops.version: ''
ms.openlocfilehash: ddc22bdd223eff513ff571501c599712ac78a7da
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/02/2022
ms.locfileid: "9219906"
---
# <a name="improve-scheduling-engine-performance"></a>Verbessern der Leistung des Planungsmoduls

[!include [banner](../includes/banner.md)]

Das Ressourcenplanungsmodul wird verwendet, um Arbeitspläne für geplante und freigegebene Produktionsaufträge zu planen. Das Modul wurde ursprünglich als Teil von Dynamics AX 2012 veröffentlicht und hat seit seiner Veröffentlichung mehrere Verbesserungen durchlaufen.

Das [Feinterminierungsproblem](https://en.wikipedia.org/wiki/Job_shop_scheduling) ist ein äußerst komplexes kombinatorisches Problem, bei dem die Lösungszeit exponential mit der Anzahl der Entscheidungsvariablen wächst. Oft richten Kunden Produktionsarbeitspläne und zugehörige Daten so ein, dass ein Planungsarbeitsplan entsteht, das selbst auf modernster Hardware nicht in angemessener Zeit gelöst werden kann. Dieser Artikel hilft Ihnen dabei, das Planungsmodul zu verstehen und zu verstehen, wie ein bestimmtes Setup die Leistung beeinflussen kann.

Wenn es darum geht, die Leistung der Planung zu verbessern, empfehlen allgemeine Richtlinien, die Komplexität des Problems zu reduzieren, das das Modul lösen muss. Einige der Hauptfaktoren, die die Leistung beeinflussen können, sind:

- Arbeitspläne mit vielen Arbeitsgängen
- Arbeitspläne mit parallelen Arbeitsgängen
- Arbeitsgänge mit einer Ressourcenmenge von mehr als eins
- Arbeitsgänge mit vielen anwendbaren Ressourcen
- Verwendung von festen Links
- Nutzung begrenzter Kapazität
- Die Anzahl der verschiedenen verwendeten Kalender
- Die Anzahl der Arbeitszeitfenster pro Tag im Kalender
- Gesamtdauer des Arbeitsplans
- Paralleles Ausführen mehrerer Planungsmodule

## <a name="overview-of-basic-scheduling-flow"></a>Übersicht über den grundlegenden Planungsflow

Um zu verstehen, wie sich ein bestimmtes Setup auf die Leistung auswirken kann, ist es wichtig, etwas über den Ablauf des Prozesses zu verstehen, sowohl innerhalb des Moduls als auch im umgebenden X++–Code.

Der grundlegende Prozess zum Planen eines Auftrags besteht aus drei Hauptschritten:

- **Daten laden** – Hier werden die X++–Datenmodelle in Form von Einzelvorgängen und Einschränkungen in das interne Datenmodell des Moduls integriert.
- **Planung** – Dies ist die Hauptquelle für die Planung, die das angegebene Modell und die Einschränkungen verarbeitet und ein Ergebnis generiert. Während dieses Vorgangs fordert das Modul bei Bedarf Arbeitszeitinformationen und vorhandene Kapazitätsreservierungen von X++ an.
- **Daten speichern** – Das Modulergebnis in Form von Slots für Einzelvorgangs-Kapazitätsreservierungen wird von X++ Code verarbeitet, um Kapazitätsreservierungen zu speichern und die Start- und Endzeiten der Einzelvorgänge/des Arbeitsgangs/des Auftrags zu aktualisieren.

## <a name="load-data-into-the-engine"></a>Laden der Daten in das Modul

Das Planungsmodul verfügt über ein abstrakteres Datenmodell als die Supply Chain Management-Datenbank, da es als generisches Modul erstellt wurde, das verschiedene Datenquellen verarbeiten kann. Die Konzepte des Arbeitsplans, der sekundären Arbeitsgänge und der Laufzeit müssen in das generische Einzelvorgangs- und Einschränkungsmodell „übersetzt“ werden, das das Modul verfügbar macht. Die Logik zum Erstellen des Modells enthält eine erhebliche Menge an Geschäftslogik und ist je nach Quelldaten unterschiedlich. Die verantwortliche X++– Klasse ist `WrkCtrScheduler`. Zudem gibt es abgeleitete Klassen für geplante Produktionsaufträge, freigegebene Produktionsaufträge und Projektplanungen.

Betrachten Sie als Beispiel einen Arbeitsplan, der in der folgenden Tabelle und im folgenden Bild dargestellt ist und relativ einfach zu sein scheint.

| Arbeitsgang- Nr. | Priorität | Rüstzeit | Bearbeitungszeit | Wartezeit danach | Ressourcenmenge | Nächster |
| --- | --- | --- | --- | --- | --- | --- |
| 10 | Primär | 1.00 | 2.00 | | 1 | 20 |
| 10 | Sekundär&nbsp;1 | | | | 1 | 20 |
| 20 | Primär | | 3.00 | 1.00 | 3 | 0 |

![Beispiel eines Arbeitsplandiagramms.](media/scheduling-engine-route.png "Beispiel eines Arbeitsplandiagramms")

Wenn Sie dies an das Modul senden, wird es in acht Einzelvorgänge aufgeteilt, wie in der folgenden Abbildung gezeigt (wählen Sie das Bild aus, um es zu vergrößern).

[![Planen von Moduleinzelvorgängen](media/scheduling-engine-jobs.png "Planen von Moduleinzelvorgängen")](media/scheduling-engine-jobs-large.png)

Die Standardverbindung zwischen zwei Einzelvorgängen ist `FinishStart`. Dies bedeutet, dass die Endzeit eines Einzelvorgangs vor der Startzeit eines anderen Einzelvorgangs liegen muss. Da das Setup von derselben Ressource ausgeführt werden muss, die später den Prozess ausführt, gibt es `OnSameResource`-Einschränkungen zwischen ihnen. Zwischen den Einzelvorgängen für den primären und den sekundären Betrieb für 10 gibt es `StartStart`- und `FinishFinish`-Links, was bedeutet, dass die Einzelvorgänge gleichzeitig beginnen und enden müssen, und es gibt `NotOnSameResource`-Einschränkungen, die verhindern, dass die gleiche Ressource für primäre und sekundäre Arbeitsvorgänge verwendet wird.

Für Arbeitsgang 20, bei dem die Ressourcenmenge auf 3 festgelegt wurde, wurde der Prozesseinzelvorgang in drei verschiedene Einzelvorgänge aufgeteilt, bei denen alle Einzelvorgänge genau zur gleichen Zeit ausgeführt werden müssen.
In diesem Fall wurde die Arbeitsplangruppe so eingerichtet, dass keine Kapazität für die Warteschlange nach Zeiten reserviert wird. Daher gibt es nur einen einzigen Einzelvorgang für die Warteschlange danach.

Das Planungsmodul versteht nur die Konzepte von Einzelvorgängen und hat keine Vorstellung von Arbeitsgängen. Dies bedeutet, dass bei der Arbeitsgangplanung die Arbeitsgänge auch in Einzelvorgänge aufgeteilt werden, obwohl diese nicht in der Datenbank gespeichert werden.

Für jeden Einzelvorgang definieren wir auch die zugehörige Kapazitätsanforderung (die Anzahl der erforderlichen Sekunden). Abhängig davon, wie die Ressourcenanforderungen definiert wurden, können wir für jeden Einzelvorgang auch eine Liste aller potenziell anwendbaren Ressourcen senden, mit denen der Einzelvorgang ausgeführt werden könnte, und die Kapazitätsanforderungen für diese bestimmte Ressource angeben. Obwohl die Liste der anwendbaren Ressourcen beim Erstellen des Modells gesendet wird, muss das Modul dennoch sicherstellen, dass die Ressourcenzuweisung tatsächlich für die gesamte Einzelvorgangsdauer gültig ist.

## <a name="scheduling-engine-internals"></a>Interne Komponenten des Planungsmoduls

### <a name="scheduling-engine-interface"></a>Schnittstelle des Planungsmoduls

Um eine Vorstellung davon zu bekommen, wie das Modul intern funktioniert, sollten Sie sich die Funktionen ansehen, die es extern bereitstellt. In X++ ist die Hauptschnittstelle `WrkCtrSchedulerEngineInterface`. Sie verfügt über die in den folgenden Unterabschnitten beschriebenen Methoden.

#### <a name="general-engine"></a>Allgemeines Modul

| **Methode** | **Kostenträger** |
| --- | --- |
| `run` | Plant alle geladenen Einzelvorgänge und gibt den Fehlercode zurück. |
| `getJobSchedulingSequenceResult` | Ruft das Planungsergebnis und den ersten Einzelvorgang mit Fehler für die von einem bestimmten Einzelvorgang identifizierte Sequenz ab. |
| `validateJobCapacityReservations` | Überprüft die Kapazitätsreservierungen für alle vom Modul gespeicherten Einzelvorgänge. |
| `setReservationsTimeStamp` | Sendet einen Zeitstempel an das Modul, der für alle neuen Kapazitätsreservierungen für die geplanten Einzelvorgänge im Cache des Moduls festgelegt wurde. |
| `addPropertyToGroupAggregation` | Fügt dem Satz von Eigenschaften, die beim Aggregieren der Kapazität verwendet werden, ein Eigenschaftspräfix hinzu. |
| `addResource` | Fügt dem Ressourcenpool des Planungsmoduls eine Ressource hinzu. |
| `addResourceGroup` | Fügt dem Ressourcengruppenpool des Planungsmoduls eine Ressourcengruppe hinzu. |
| `addResourceGroupMembership` | Fügt einer Ressourcengruppe eine Ressource als Mitglied hinzu. |
| `addOptimizationGoal` | Fügt ein Planungsoptimierungsziel hinzu (Dauer oder Priorität). |

#### <a name="individual-jobs"></a>Einzelne Einzelvorgänge

| **Methode** | **Kostenträger** |
| --- | --- |
| `addJobInfo` | Fügt einen Datensatz mit Einzelvorgangsinformationen hinzu, der das Modul über einen Einzelvorgang informiert, der geplant werden soll. |
| `addConstraintJobEndsAt` | Fügt eine Einschränkung hinzu, dass ein Einzelvorgang zu einem bestimmten Datum und einer bestimmten Uhrzeit enden soll. |
| `addConstraintJobStartsAt` | Fügt eine Einschränkung hinzu, dass ein Einzelvorgang zu einem bestimmten Datum und einer bestimmten Uhrzeit starten soll. |
| `addConstraintMaxJobDays` | Definiert die Einschränkung, dass sich ein Einzelvorgang über eine bestimmte maximale Anzahl von Tagen erstrecken kann. |
| `addConstraintResourceRequirement` | Fügt die Einschränkung hinzu, dass der Einzelvorgang für eine bestimmte Ressource geplant werden muss. |
| `addJobBindPriority` | Fügt eine Einzelvorgangs-Bindungspriorität für ein Paar (Einzelvorgang, Einschränkungsebene) hinzu. Ein höherer Prioritätswert bedeutet, dass die Einzelvorgangsvariablen früher gebunden werden. Der Einzelvorgang wird vor Einzelvorgängen mit niedrigerer Priorität in derselben Sequenz verarbeitet. |
| `addJobCapacity` | Fügt Kapazitätsauslastungsinformationen für einen Einzelvorgang hinzu (z. B. die erforderliche Einzelvorgangs-Laufzeit), unabhängig davon, mit welcher Ressource der Einzelvorgang ausgeführt wird. |
| `addJobResourceCapacity` | Fügt der Gruppe von Ressourcen, die zum Ausführen eines Einzelvorgangs verwendet werden können, eine Ressource hinzu und gibt die Kapazität an, die für die Ausführung mit dieser Ressource erforderlich ist. |
| `addJobGoal` | Fügt Einzelvorgangsziel-Informationen für eine bestimmte Einschränkungsebene hinzu (früheste Endzeit oder späteste Startzeit). |
| `addJobResourcePriority` | Fügt die Priorität hinzu, die verwendet werden soll, wenn ein Einzelvorgang für eine Ressource geplant ist. |
| `addJobResourceRuntime` | Gibt eine Einzelvorgangszeit an, die von der Ressource abhängt, für die der Einzelvorgang geplant wird. |
| `addJobRuntime` | Gibt eine Einzelvorgangszeit an, die von der Ressource unabhängig ist, für die der Einzelvorgang geplant wird. |
| `scheduleJobOnResourceGroup` | Markiert einen Einzelvorgang für die Planung auf Ressourcengruppenebene. |
| `setJobResourcePreemptionAllowed` | Legt fest, ob für einen Einzelvorgang einer Ressource eine Vorwegnahme zulässig ist (wenn das Modul den Einzelvorgang nicht in zusammenhängenden Kapazitätsslots planen darf). |
| `setRequiredNumberOfResources` | Legt die Anzahl der Ressourcen fest, die zum Planen eines Einzelvorgangs erforderlich sind (nur für die Planung von Arbeitsgängen). |

#### <a name="constraints-between-jobs"></a>Einschränkungen zwischen Einzelvorgängen

| **Methode** | **Kostenträger** |
| --- | --- |
| `addJobLink` | Fügt einen Link (z. B. Ende\>Start) zwischen zwei Einzelvorgängen hinzu. |
| `addConstraintEndsDelayed` | Definiert die Einschränkung, dass ein Einzelvorgang nicht vor dem Ende eines anderen Einzelvorgangs beendet werden kann, zuzüglich einer gewissen Verzögerungszeit. |
| `addConstraintJobListWorkingTimeIntersect` | Fügt eine Einschränkung hinzu, dass sich die für die Einzelvorgänge reservierten Kapazitätsslots in den sich überschneidenden Arbeitszeiten für die beiden von den Einzelvorgängen verwendeten Ressourcen befinden müssen. |
| `addConstraintJobOverlap` | Fügt eine Einschränkung hinzu, die definiert, wie Einzelvorgänge sequenziert werden, wenn eine bestimmte Menge eines Artikels zwischen zwei Ressourcen verschoben werden kann, während die erste Ressource die Verarbeitung noch nicht beendet hat, sodass die zweite Ressource mit der Verarbeitung beginnen kann. |
| `addConstraintNotOnSameResource` | Fügt eine Einschränkung hinzu, dass zwei Einzelvorgänge nicht für dieselbe Ressource geplant werden sollen. |
| `addConstraintOnSameResource` | Fügt eine Einschränkung hinzu, dass zwei Einzelvorgänge dieselbe Ressource verwenden müssen. |
| `addJobSameReservations` | Fügt eine Einschränkung hinzu, dass ein Einzelvorgang am Ende Kapazitätsreservierungen für dieselben Zeitfenster wie der primäre Einzelvorgang haben muss. |
| `setPrimaryParallelJob` | Fügt Informationen darüber hinzu, welcher Einzelvorgang der primäre Einzelvorgang in einer Reihe von parallelen Einzelvorgängen ist. |

### <a name="solver"></a>Solver

Das Modul selbst ist im Wesentlichen ein spezialisierter Einschränkungssolver mit benutzerdefinierten Heuristiken. Der Solver basiert auf zwei Hauptelementen: Variablen und Einschränkungen.

#### <a name="variable"></a>Variabel

Eine Variable repräsentiert eine Domäne möglicher Werte. Das Planungsmodul verfügt über zwei Arten von Variablen:

- **DateTime-Variable** – Hat eine Domäne mit allen Daten und Zeiten, und die Domäne kann eingeschränkt werden, indem die Unter- und Obergrenze für die Zeit der Variablen näher aneinander verschoben werden.
- **Ressourcenvariable** – Verfügt über eine Domäne mit anwendbaren Ressourcen, und die Domäne kann eingeschränkt werden, indem Ressourcen aus der Liste entfernt werden.

#### <a name="constraint"></a>Einschränkung

Eine Einschränkung wirkt sich auf Variablen aus, indem sie ihre Domänen einschränkt. Sie hängt jedoch auch von Variablen ab, sodass sie aktiviert wird, wenn sich Variablen ändern. Der Prozess der „Einschränkungsweitergabe“ ist, wenn eine Einschränkung ihre Hauptfunktion ausführt und bei Erfolg an die Hauptlogik zurückmeldet.

Eine Variable gilt als gebunden, wenn sie nicht weiter eingeschränkt werden kann. Dies bedeutet für die DateTime-Variable, dass obere und untere Grenze identisch sind, und für die Ressourcenvariable, dass sie nur eine einzige anwendbare Ressource hat. Wenn alle Variablen gebunden sind, wird eine Lösung gefunden.

### <a name="constraint-levels"></a>Einschränkungsebenen

Wenn die Planung im Rahmen der Phase der Materialbedarfsplanung (MRP) ausgeführt wird, werden die Aufträge ab dem Anforderungsdatum rückwärts geplant. Wenn es jedoch nicht möglich ist, einen Zeitplan zu finden, der heute oder später beginnt und vor dem Anforderungsdatum endet, ändert sich die Planungsrichtung ab heute in die Zukunft.

Diese Hauptgeschäftsregel wird durch Organisieren der Einschränkungen in Ebenen abgewickelt. Wenn bei Verwendung der Einschränkungen auf der höchsten Ebene keine Lösung gefunden wird, werden alle Einschränkungen auf dieser Ebene verworfen, und die niedrigere Ebene wird ausprobiert. In der Praxis bedeutet dies, dass das Modell für die Rückwärtsterminierung eine Ebene 1 mit Einzelvorgangszielen der spätesten Startzeit bei einer maximalen Endzeitbeschränkung (dem Anforderungsdatum) und eine Ebene 0 mit Einzelvorgangszielen der frühesten Endzeit und einer minimalen Startzeitbeschränkung von heute enthält.

### <a name="algorithm"></a>Algorithmus

Die Hauptschritte des Modulalgorithmus sind:

1. Finden Sie Sequenzen (Einzelvorgangsketten), die separat gelöst werden können.
1. Versuchen Sie, eine erste Lösung für die Sequenz für die höchste Einschränkungsebene zu finden.
    1. Sortieren Sie die Einzelvorgänge in der Reihenfolge nach Einzelvorgangsziel und Prioritäten, sodass ein Starteinzelvorgang gefunden werden kann.
    1. Ordnen Sie die Einzelvorgänge in der folgenden Reihenfolge in einer Schleife an:
        1. Finden Sie alle Einschränkungen, die weitergegeben werden müssen, und die Weitergabe ausführen.
        1. Wenn alle Variablen für den Einzelvorgang gebunden wurden, wurde eine Lösung für diesen Einzelvorgang gefunden.
        1. Wenn eine der Variablen nicht gebunden werden konnte, ohne die Einschränkungen zu verletzen, führen Sie ein Rollback der Variablenbindung aus, versuchen Sie einen anderen Wert in der Domäne (für Ressourcenvariable), und führen Sie die Weitergabe der Einschränkungen erneut aus.
1. Wenn keine Lösung gefunden wurde, werden alle Einschränkungen auf der aktuellen Einschränkungsebene entfernt, eine niedrigere Einschränkungsebene wird verwendet (sofern niedrigere Ebenen verfügbar sind) und die Lösungssuche mit dem neuen Satz von Einschränkungen wiederholt.
1. Wenn eine praktikable Lösung gefunden wurde, wird die Optimierungsphase gestartet, in der versucht wird, eine bessere Lösung zu finden, bis das Optimierungszeitlimit erreicht ist oder alle Ressourcenkombinationen erschöpft sind.

Dem Einschränkungssolver sind die Besonderheiten des Planungsalgorithmus nicht bekannt. In der Definition und Kombination der verschiedenen Einschränkungen geschieht die „Magie“.

### <a name="determining-working-times"></a>Arbeitszeiten bestimmen

Ein großer Teil der (internen) Einschränkungen im Modul steuert die Arbeitszeit und Kapazität einer Ressource. Im Wesentlichen besteht die Aufgabe darin, die Arbeitszeitfenster für eine Ressource von einem bestimmten Punkt in eine bestimmte Richtung zu durchlaufen und ein ausreichend langes Intervall zu finden, in das die für die Einzelvorgänge erforderliche Kapazität (Zeit) passen kann.

Dazu muss da Modul die Arbeitszeiten einer Ressource kennen. Im Gegensatz zu den Hauptmodelldaten sind die Arbeitszeiten *faul geladen*. Dies bedeutet, dass sie nach Bedarf in das Modul geladen werden. Der Grund für diesen Ansatz ist, dass es in Supply Chain Management häufig Arbeitszeiten für einen Kalender über einen sehr langen Zeitraum gibt und in der Regel viele Kalender vorhanden sind, sodass die Daten zum Vorabladen ziemlich groß sind.

Kalenderinformationen werden vom Modul in Blöcken angefordert, indem die X++–Klassenmethode aufgerufen wird `WrkCtrSchedulingInteropDataProvider.getWorkingTimes`. Die Anforderung betrifft eine bestimmte Kalender-ID in einem bestimmten Zeitintervall. Abhängig vom Status des Servercaches in Supply Chain Management kann jede dieser Anforderungen zu mehreren Datenbankaufrufen führen, was lange dauert (relativ zur reinen Rechenzeit). Wenn der Kalender sehr ausgefeilte Arbeitszeitdefinitionen mit vielen Arbeitszeitintervallen pro Tag enthält, verlängert sich die Ladezeit ebenfalls.

Wenn die Arbeitszeitdaten in das Planungsmodul geladen werden, werden diese im internen Cache für den jeweiligen Kalender gespeichert. Wenn also andere Jobs oder Ressourcen denselben Kalender verwenden, können die nächsten Suchvorgänge schnell aus dem Speicher ausgeführt werden. Eine häufige Ursache für schlechte Leistung ist die Verwendung einer separaten Kalender-ID für jede Ressource, da dann für jeden Kalender Daten angefordert werden müssen, obwohl der Inhalt der Kalender möglicherweise identisch ist.

### <a name="finite-capacity"></a>Begrenzte Kapazität

Bei Verwendung einer begrenzten Kapazität werden die Arbeitszeitfenster aus dem Kalender basierend auf den vorhandenen Kapazitätsreservierungen aufgeteilt und reduziert. Diese Reservierungen werden auch über dieselbe `WrkCtrSchedulingInteropDataProvider`-Klasse wie die Kalender abgerufen, aber verwenden stattdessen die Methode `getCapacityReservations`. Bei der Planung während der Produktprogrammplanung werden die Reservierungen für den jeweiligen Produktprogrammplan berücksichtigt und, falls auf der Seite **Produktprogrammplanungsparameter** aktiviert, sind auch die Reservierungen aus festen Produktionsaufträgen enthalten. Ebenso ist es bei der Planung eines Produktionsauftrags möglich, Reservierungen aus vorhandenen geplanten Aufträgen einzubeziehen, obwohl dies nicht so häufig ist wie umgekehrt.

Bei Verwendung einer begrenzten Kapazität dauert die Planung aus mehreren Gründen länger:

- Das Abrufen der Kapazitätsinformationen aus der Datenbank ist ein langsamer Vorgang, und das serverseitige Zwischenspeichern von Kapazitätsinformationen ist normalerweise nicht so gut wie bei Arbeitszeiten, da sie normalerweise nicht wie Kalender von Ressourcen gemeinsam genutzt werden.
- Die Anzahl der zu durchlaufenden Arbeitszeitfenster nimmt aufgrund der Teilungen zu, und Zeitfenster für einen längeren Zeitraum müssen typischerweise untersucht werden, bevor eine Lösung gefunden werden kann.
- Nach Abschluss der Planung muss eine Überprüfung auf widersprüchliche Reservierungen durchgeführt werden (Einzelheiten finden Sie im Abschnitt „Paralleles Ausführen von Planungsmodulen“).

### <a name="examining-the-resource-combinations"></a>Untersuchen der Ressourcenkombinationen

Wenn die Abfolge der Einzelvorgänge nur die standardmäßigen `FinishStart`-Links enthält – sie also eine einfache Kette ohne Verzweigungen darstellt –, kann ein optimales Ergebnis (aus der Perspektive einzelner Aufträge, nicht über Aufträge hinweg) erzielt werden, indem die beste Lösung für den ersten Einzelvorgang gefunden und dann die beste Lösung für den nächsten Einzelvorgang gefunden wird. Die beste Lösung für einen Einzelvorgang besteht darin, die Ressource zu finden, mit der das Startdatum und das Enddatum geplant werden können, die am nächsten am Einzelvorgangsziel liegen (bei der Vorausplanung bedeutet dies, dass das Enddatum des Einzelvorgangs so früh wie möglich liegt), wobei die Einschränkungen weiterhin beachtet werden.

Bei parallelen Einzelvorgängen kann das Finden einer Lösung das Untersuchen verschiedener Ressourcenkombinationen umfassen. Die Anzahl der möglichen Ressourcenkombinationen ergibt sich aus der Anzahl der anwendbaren Ressourcen für die verbundenen parallelen Einzelvorgänge. Insbesondere wenn ein Auftrag ab einem Anforderungsdatum rückwärts geplant wird, kann es eine Weile dauern, bis die Logik erkennt, dass es keine Lösung für das Problem gibt, bei dem die parallelen Einzelvorgänge vor das heutige Datum passen, da alle Kombinationen überprüft werden müssen, weil es einige Ressourcen geben könnte, die eine höhere Effizienz hatten oder einen anderen Kalender, der ein Ergebnis liefern könnte. Dies bedeutet, dass, wenn kein Zeitlimit festgelegt wurde, die Ausführung lange Zeit andauert, bevor die Richtung in vorwärts geändert wird.

Diese kombinatorische Logik bedeutet auch, dass das Modul möglicherweise langsamer ausgeführt wird, wenn mehr anwendbare Ressourcen hinzugefügt werden. Wenn Leistungsprobleme bei parallelen Arbeitsgängen und bei der Planung mit unbegrenzter Kapazität auftreten, kann dies teilweise behoben werden, indem der Arbeitsplan-Designer entscheidet, welche Ressource verwendet werden soll, und die Ressource dann direkt dem Arbeitsgang zuweist (das Modul wird in den meisten Fällen am Ende immer die gleiche Ressource auswählen, sodass das Endergebnis das gleiche sein wird).

### <a name="hard-links"></a>Feste Links

Wenn Sie den Linktyp zwischen zwei Einzelvorgänge auf „Fest“ setzen, wird sichergestellt, dass zwischen dem Ende eines Einzelvorgangs und dem Beginn des nächsten Einzelvorgangs keine Zeitlücke besteht. Dies kann in Szenarien sehr nützlich sein, in denen Metall in einem Einzelvorgang erhitzt und dann im nächsten Einzelvorgang verarbeitet wird und in denen es nicht wünschenswert ist, das Metall dazwischen abkühlen zu lassen.

Wenn der Arbeitsplan bei standardmäßigen weichen Links und Vorwärtsplanung eine einfache Kette ohne Verzweigungen bildet, kann ein Ergebnis erzielt werden, indem eine Lösung für den ersten Einzelvorgang gefunden wird, der seine eigenen Einschränkungen erfüllt, und dann in der Kette weitergegangen wird und die Endzeit vom vorherigen Einzelvorgang zum nächsten Einzelvorgang weitergegeben wird. Wenn für den aktuellen Einzelvorgang keine Kapazität zu finden ist, wird seine Startzeit weiter verschoben, ohne dass dies Auswirkungen auf die vorherigen Einzelvorgänge hat, wodurch möglicherweise Lücken zwischen den Einzelvorgängen entstehen. Bei festen Links (insbesondere im Zusammenhang mit begrenzter Kapazität) für dasselbe Szenario bedeutet die Tatsache, dass ein Einzelvorgang später in der Kette keine Kapazität finden kann, dass alle vorher geplanten Einzelvorgänge einzeln nachgezogen und damit mehrmals umgeplant werden müssen. Insbesondere in Szenarien mit hoher Auslastung für mehrere Ressourcen können die harten Links eine Kettenreaktion verursachen, bei der sich die Einzelvorgänge gegenseitig beeinflussen und eine Reihe von Iterationen durchgeführt werden müssen, bevor sich das Ergebnis in einem realisierbaren Zeitplan stabilisiert.

## <a name="running-scheduling-engines-in-parallel"></a>Paralleles Ausführen von Planungsmodulen

Wenn Sie die Planung als Teil eines Produktprogrammplanungslaufs durchführen, in dem Hilfsprogramme verwendet werden, kann jeder der Produktprogrammplanung-Hilfsprogrammthreads auch Planungsaufgaben für Produktionsaufträge übernehmen. Dies bedeutet, dass mehrere Planungsmodule gleichzeitig ausgeführt werden können. Während Multithreading im Allgemeinen einen sehr bedeutenden Leistungsvorteil darstellt, gibt es auch einige funktionale Nachteile, wenn es um die Planung geht.

In der MRP werden alle Produktionsaufträge für eine bestimmte Stücklistenebene in der Reihenfolge des Anforderungsdatums geplant. Dies bedeutet, dass die Aufträge mit dem frühesten Anforderungsdatum zuerst geplant werden sollten und daher die höchste Chance haben, die verfügbare Ressourcenkapazität zu erhalten. Wenn jedoch mehrere Module aus der Liste der nicht geplanten Aufträge auswählen, ist die Reihenfolge nicht mehr gewährleistet, da eins möglicherweise schneller als das andere ausgeführt wird.

Wenn Sie mit begrenzter Kapazität planen und mehrere Modulinstanzen versuchen, Aufträge zu planen, die möglicherweise dieselben Ressourcen im selben Zeitintervall verwenden, kann eine Racebedingung auftreten. Die Anzahl solcher Racebedingungen wird im Feld **Planungskonflikte** auf der Verlaufsseite der Produktprogrammpläne erfasst. Die Konfliktlösungslogik lautet wie folgt:

- Planen Sie einen Auftrag (sperrenfrei) und erhalten Sie Kapazitätsreservierungen.
- Setzen Sie die Sperre.
- Überprüfen Sie, ob in der Zeitspanne neuere Kapazitätsreservierungen für die geplanten Ressourcen vorhanden sind.
  - Wenn nein, schreiben Sie die Kapazität und heben Sie die Sperre auf.
  - Wenn ja, heben Sie die Sperre auf und planen Sie den Auftrag ganz neu.

Wenn Sie also mit mehreren Modulinstanzen planen, ist das Ergebnis nicht vollständig deterministisch, da es vom genauen Timing jedes Threads abhängt.

## <a name="operation-scheduling-performance"></a>Leistung der Grobterminierung

Obwohl die Grobterminierung auch als grobe Kapazitätsplanung bezeichnet wird, kann es vom Standpunkt des Moduls aus schwieriger sein, das Problem zu lösen, wenn eine begrenzte Kapazität verwendet wird, da mehr Daten benötigt werden, um die Durchführbarkeit zu bestimmen.

Die Kapazität einer Ressourcengruppe hängt davon ab, welche und wie viele Ressourcen Mitglieder der Ressourcengruppe sind. Eine Ressourcengruppe an sich hat keine Kapazität – nur wenn Ressourcen Mitglied der Gruppe sind, verfügen sie über Kapazität. Da die Mitgliedschaft in Ressourcengruppen im Laufe der Zeit variieren kann, muss die Kapazität pro Tag bewertet werden.

Bei der Grobterminierung wird der Kalender der Ressourcengruppe verwendet, um die Start- und Endzeiten für jeden Arbeitsgang zu bestimmen. Dies bedeutet, dass der Kalender der Ressourcengruppe begrenzt, wie viel Zeit für einen Arbeitsgang an einem Tag in einer Ressourcengruppe grobterminiert werden kann. Im Gegensatz zum Kalender für die spezifischen Ressourcen werden die Effizienzdaten des Kalenders für die Ressourcengruppe ignoriert, da sie lediglich die Öffnungszeiten und nicht die tatsächliche Kapazität angeben.

Wenn beispielsweise die Arbeitszeit für eine Ressourcengruppe an einem bestimmten Datum zwischen 8:00 und 16:00 Uhr liegt, kann ein Arbeitsgang die Ressourcengruppe nicht mehr belasten, als in 8 Stunden passt, egal über wie viel Kapazität diese Ressourcengruppe an diesem Tag insgesamt verfügt. Die verfügbare Kapazität kann die Last jedoch weiter begrenzen.

Die Auslastung der Einzelvorgangsplanung für alle Ressourcen in der Ressourcengruppe an einem bestimmten Tag wird berücksichtigt, wenn die verfügbare Kapazität für die Ressourcengruppe am selben Tag berechnet wird. Für jedes Datum lautet die Berechnung:

*Verfügbare Ressourcengruppenkapazität = Kapazität für Ressourcen in der Gruppe basierend auf ihrem Kalender &ndash; Job geplante Auslastung der Ressourcen in der Gruppe &ndash; Geplante Operationen laden die Ressourcen in der Gruppe &ndash; Geplante Operationen laden die Ressourcengruppe*

Auf der Registerkarte **Ressourcenanforderungen** des Arbeitsplan-Arbeitsgangs können die Ressourcenanforderungen entweder mithilfe einer bestimmten Ressource (in diesem Fall wird der Arbeitsgang mit dieser Ressource geplant), für eine Ressourcengruppe, für einen Ressourcentyp oder für eine oder mehrere Funktionen, Qualifikationen, Kurse oder Zertifikate angegeben werden. Die Verwendung all dieser Optionen bietet zwar eine große Flexibilität beim Arbeitsplandesign, erschwert jedoch auch die Planung für das Modul, da die Kapazität pro „Eigenschaft“ berücksichtigt werden muss (der abstrakte Name, der im Modul für Funktionen, Qualifikationen usw. verwendet wird).

Die Kapazität der Ressourcengruppe für eine Funktion ist die Summe der Kapazität für alle Ressourcen in der Ressourcengruppe, die über die betreffende Funktionen verfügen. Wenn eine Ressource in der Gruppe über eine Funktion verfügt, wird diese unabhängig von der erforderlichen Kapazität berücksichtigt.

Bei der Grobterminierung wird die verfügbare Kapazität für eine bestimmte Funktion für eine Ressourcengruppe reduziert, wenn sie mit einem Arbeitsgang geladen wird, für den die betreffende Funktion erforderlich ist. Wenn für den Vorgang mehr als eine Funktion erforderlich ist, wird die Kapazität für alle erforderlichen Funktionen reduziert.

Für jedes Datum lautet die erforderliche Berechnung:

*Verfügbare Kapazität für eine Fähigkeit = Kapazität für die Fähigkeit &ndash; Job geplante Auslastung der Ressourcen mit der spezifischen Funktion, die in der Ressourcengruppe enthalten ist &ndash; Geplante Operationen laden die Ressourcen mit der spezifischen Funktion, die in der Ressourcengruppe enthalten ist &ndash; Geplante Operationen laden die Ressourcengruppe selbst, für die die jeweilige Funktion erforderlich ist*

Dies bedeutet, dass bei einer Auslastung einer bestimmten Ressource die Auslastung bei der Berechnung der verfügbaren Kapazität der Ressourcengruppe pro Funktion berücksichtigt wird, da die Auslastung einer bestimmten Ressource ihren Beitrag zur Kapazität der Ressourcengruppe für eine Funktion reduziert, unabhängig davon, ob die Auslastung der spezifischen Ressource sich auf diese spezifische Funktion bezieht. Wenn auf Ressourcengruppenebene eine Auslastung vorhanden ist, wird diese bei der Berechnung der verfügbaren Kapazität der Ressourcengruppe pro Funktion nur berücksichtigt, wenn die Auslastung von einem Arbeitsgang stammt, für den die spezifische Funktion erforderlich ist.

Die obige Logik ist kompliziert, weil diese für jeden Typ von „Eigenschaft“ gleich ist. Daher erfordert die Verwendung der Grobterminierung mit begrenzter Kapazität das Laden einer erheblichen Datenmenge.

## <a name="viewing-scheduling-engine-input-and-output"></a>Anzeigen der Ein- und Ausgabe des Planungsmoduls

Aktivieren Sie die Protokollierung, um bestimmte Details zur Eingabe und Ausgabe des Planungsprozesses abzurufen, indem Sie zu **Organisationsverwaltung \> Einrichten \> Planung \> Planungsverfolgungs-Cockpit** wechseln.

Wählen Sie auf dieser Seite zuerst **Protokollierung aktivieren** im Aktivitätsbereich aus. Führen Sie dann die Planung für den Produktionsauftrag aus. Wenn Sie fertig sind, kehren Sie zur Seite **Planungsverfolgungs-Cockpit** zurück und wählen **Protokollierung deaktivieren** im Aktivitätsbereich aus. Aktualisieren Sie die Seite und eine neue Zeile wird im Raster angezeigt. Wählen Sie die neue Zeile aus und wählen Sie im Aktivitätsbereich **Herunterladen** aus. Dadurch erhalten Sie einen komprimierten ZIP-Ordner mit den folgenden Dateien:

- **Log.txt** – Dies ist die Protokolldatei, die die Schritte beschreibt, die das Modul durchläuft. Es ist sehr präzise und kann etwas überwältigend sein, aber wenn es als Teil des Experimentierens mit den Arbeitsplaneinstellungen verwendet wird, um Leistungsprobleme zu lösen, ist das erste, wonach gesucht werden muss, der Zeitunterschied zwischen der ersten und der letzten Zeile, da dies die genaue Zeit ist, die der Scheduler benötigt hat.
- **XmlModel.xml** – Dies enthält das Modell, das in X++ erstellt wurde und mit dem das Modul arbeitet. Die in der Datei verwendete `JobId` korreliert mit der `RecId` aus der Quelltabelle mit den Einzelvorgängen (`ReqRouteJob` oder `ProdRouteJob`). Die typische Sache, nach der in dieser Datei gesucht werden muss, ist, dass die in `ConstraintJobStartsAt` und `ConstraintJobEndsAt` angegebenen Daten wie erwartet sind und dass die `JobGoal`-Eigenschaft korrekt festgelegt ist und die Einzelvorgänge über die `JobLink`-Einschränkungen miteinander verknüpft sind.
- **XmlSlots.xml** – Dies enthält alle Arbeitszeiten und Kapazitätsreservierungen, die das Modul angefordert hat. Die Arbeitszeiten und Reservierungen des Kalenders werden von dem Modul nur für die Zeiträume angefordert, in denen versucht wird, die Einzelvorgänge (und einen zusätzlichen Puffer) zu platzieren. Wenn die Datei also Zeiten enthält, die sehr weit in der Zukunft liegen, kann dies ein Hinweis auf ein Problem mit dem Setup sein. Die `ResourceProperty`-Knoten zeigen für jede Ressource an, welcher Ressourcengruppe und welchen Funktionen sie für welche Zeiträume zugeordnet ist.
- **Result.xml** – Dies enthält das Ergebnis des Planungslaufs.

Beachten Sie, dass die Ablaufverfolgungsfunktion einen erheblichen Leistungsaufwand verursachen kann. Verwenden Sie sie daher nur, um die Planung bestimmter Aufträge auf kontrollierte Weise zu untersuchen. Wenn sie während eines Produktprogrammplanungslaufs eingeschaltet wird, erreicht sie schnell ihre Größenbeschränkung und stoppt.

## <a name="troubleshooting-performance"></a>Problembehandlung bei der Leistung

Wie aus allen vorherigen Abschnitten hervorgeht, gibt es einige Fallstricke bei der Einrichtung und Verwendung des Planungsmoduls, was zu Leistungsproblemen führen kann. Die folgende Prüfliste kann zur Problembehandlung verwendet werden. Es ist wichtig, alle Punkte zu betrachten, da es meistens eine Kombination mehrerer Faktoren ist, die zu Problemen führt.

### <a name="performing-scheduling-as-part-of-mrp-when-it-is-not-needed"></a>Durchführen der Planung als Teil der Materialbedarfsplanung, wenn diese nicht benötigt wird

Obwohl Arbeitspläne für Produktionskontrollzwecke wie Kostenrechnung und Berichterstellung verwendet werden, ist es möglicherweise nicht erforderlich, sie während der Materialbedarfsplanung zu berücksichtigen. In einigen Fällen reicht es für die Planung aus, eine für den Artikel festgelegte standardmäßige Produktionsdurchlaufzeit zu haben. Um die Arbeitsplanplanung zu deaktivieren, setzen Sie den Kapazitätszeitrahmen auf Null. Wenn eine Planung durchgeführt werden soll, muss der Kapazitätszeitraum sorgfältig festgelegt werden, da möglicherweise nicht die Arbeitspläne für den ganzen Planungszeitraum der MRP berücksichtigt werden müssen.

Beachten Sie, dass der Auftrag, wenn er während der Materialbedarfsplanung nicht geplant ist, stattdessen geplant werden muss, wenn der geplante Auftrag umgewandelt wird. Dies bedeutet, dass der Umwandlungsvorgang länger dauert. Je nachdem, wie viele der vorgeschlagenen geplanten Aufträge umgewandelt werden, kann der Leistungsgewinn aus der Materialbedarfsplanung beim Umwandeln verloren gehen.

### <a name="route-with-unnecessary-operations"></a>Arbeitsplan mit unnötigen Arbeitsgängen

Bei der Gestaltung des Arbeitsplans ist es verlockend zu versuchen, die reale Welt mit allen Schritten, die die Produktion durchläuft, genau zu modellieren. Dies kann in einigen Fällen nützlich sein, ist jedoch nicht gut für die Leistung, da das Modell, mit dem das Modul arbeiten muss, größer wird (sowohl in Bezug auf Einzelvorgänge als auch in Bezug auf Einschränkungen) und mehr SQL-Anweisungen zum Einfügen und Aktualisieren der Einzelvorgänge und Kapazitätsreservierungen ausgeführt werden. Es gibt auch den nachgelagerten Effekt, dass eventuell Fortschritte bei den Einzelvorgängen gemeldet werden müssen, was durch automatische Buchungen gemindert werden kann. Wenn die Daten für nichts verwendet werden, entsteht eine unnötige Auslastung.

Wir empfehlen, dass Sie nur Arbeitsgänge erstellen, die für die Planung (in der Regel die Engpassressourcen) und/oder für Kalkulationszwecke unbedingt erforderlich sind. Alternativ sollten Sie viele kleinere unterschiedliche Arbeitsgänge zu einem größeren Arbeitsgang zusammenfassen, der einen größeren Teil des Prozesses darstellt.

### <a name="many-applicable-resources-for-an-operation"></a>Viele anwendbare Ressourcen für einen Arbeitsgang

Die Anzahl der anwendbaren Ressourcen für einen Arbeitsgang wird durch die Ressourcenanforderungen bestimmt, die für die Arbeitsgangbeziehung festgelegt wurden. Die Anforderung kann entweder für eine bestimmte (einzelne) Ressource gelten oder auf der Mitgliedschaft der Ressource in einer Ressourcengruppe oder Funktion basieren.

Wenn die Planung nicht mit begrenzter Kapazität durchgeführt wird und alle anwendbaren Ressourcen den gleichen Kalender und die gleiche Effizienz haben, wählt das Planungsmodul letztendlich immer dieselbe Ressource für einen Arbeitsgang aus, jedoch erst, nachdem alle anwendbaren Ressourcen ausprobiert wurden, um zu überprüfen, ob es eine Ressource gibt, die sich besser eignet als die anderen. In diesem Fall kann die Auslastung der Planung erheblich reduziert werden, indem dem Arbeitsgang zum Zeitpunkt des Arbeitsplandesigns immer eine bestimmte Ressource zugewiesen wird.

### <a name="route-with-parallel-operations"></a>Arbeitsplan mit parallelen Arbeitsgängen

Parallele Arbeitsgänge (primär/sekundär) sind ein leistungsstarkes Tool zur Modellierung von Szenarien, z. B. wenn eine Maschine und ein Bediener zur Ausführung einer bestimmten Aufgabe benötigt werden. Sie sind jedoch auch die Ursache für viele Leistungsprobleme. Wenn eine Anforderung für eine bestimmte einzelne Ressource sowohl der primäre als auch der sekundäre Arbeitsgang zugewiesen wird, ist dies normalerweise kein Problem. Wenn jedoch für jeden der Arbeitsgänge viele mögliche Ressourcen vorhanden sind, erhöht dies die Planungskomplexität erheblich.

Eine Alternative zur Verwendung paralleler Arbeitsgänge besteht darin, die Paare entweder als „virtuelle“ Ressourcen zu modellieren (die dann das Team darstellen, das für den Arbeitsgang immer zusammenarbeitet) oder einfach keinen der Arbeitsgänge zu modellieren, wenn sie keinen Engpass darstellen.

### <a name="route-with-quantity-of-resources-higher-than-1"></a>Arbeitsgang mit einer Ressourcenmenge von mehr als 1

Wenn Sie die für einen Arbeitsgang erforderliche Ressourcenmenge höher als eins ist, entspricht das Ergebnis effektiv der Verwendung von primären/sekundären Arbeitsgängen, da mehrere parallele Einzelvorgänge an das Modul gesendet werden. In diesem Fall besteht jedoch keine Möglichkeit, bestimmte Ressourcenzuweisungen zu verwenden, da für eine höhere Menge als eins mehr als eine Ressource für den Einzelvorgang anwendbar sein muss.

Ein sekundärer Arbeitsgang mit einer Ressourcenbelastungsmenge größer als eins bedeutet, dass die angegebene Menge an sekundären Ressourcen für jede Ressource des primären Arbeitsgangs benötigt wird. Wenn beispielsweise die Ressourcenmenge eines primären Arbeitsgangs auf zwei und die Ressourcenmenge seines sekundären Arbeitsgangs auf drei gesetzt ist, werden für den sekundären Arbeitsgang insgesamt sechs Ressourcen benötigt.

### <a name="excessive-use-of-finite-capacity"></a>Übermäßige Nutzung begrenzter Kapazität

Die Nutzung begrenzter Kapazität erfordert, dass das Modul die Kapazitätsinformationen aus einer Datenbank lädt, und kann einen Rechenaufwand verursachen, da es schwieriger ist, eine Lösung zu finden, insbesondere in Umgebungen, in denen die Ressourcen nahe ihrer maximalen Kapazität gebucht sind. Daher ist es wichtig, sorgfältig zu prüfen, ob eine Ressource wirklich eine begrenzte Kapazität benötigt oder überbucht werden kann. Da es bei begrenzten Kapazitätsressourcen möglicherweise unterschiedlich wichtig ist, dass sie nicht überbucht werden, empfehlen wir, die Engpassoption für eine Ressource in Kombination mit einem separaten Wert im Plan unter „Kapazitätsplanungszeitraum für Engpassressourcen“ zu verwenden. Durch die Nutzung des Engpasskonzepts kann der allgemeine Zeitrahmen für begrenzte Kapazitäten verringert werden.

### <a name="setting-hard-links"></a>Feste Links setzen

Der Standardlinktyp des Arbeitsplans ist *weich*. Dies bedeutet, dass zwischen der Endzeit eines Arbeitsgangs und dem Beginn des nächsten Arbeitsgangs eine Zeitlücke zulässig ist. Dies zuzulassen kann den unglücklichen Effekt haben, dass die Produktion für eine Weile stillstehen kann, wenn Materialien oder Kapazitäten für einen der Arbeitsgänge für eine sehr lange Zeit nicht verfügbar sind, was eine mögliche Erhöhung der laufenden Arbeit bedeutet. Dies ist bei harten Links nicht der Fall, da Ende und Start perfekt ausgerichtet sein müssen. Das Festlegen fester Links erschwert jedoch das Planungsproblem, da Arbeitszeit- und Kapazitätsschnittpunkte für die beiden Ressourcen der Arbeitsgänge berechnet werden müssen. Wenn auch parallele Arbeitsgänge beteiligt sind, erhöht dies die Rechenzeit erheblich. Wenn die Ressourcen der beiden Arbeitsgänge unterschiedliche Kalender haben, die sich überhaupt nicht überschneiden, ist das Problem nicht lösbar.

Wir empfehlen, harte Links nur dann zu verwenden, wenn dies unbedingt erforderlich ist, und sorgfältig zu prüfen, ob dies für jeden Arbeitsgang des Arbeitsplans erforderlich ist.

Um die laufende Arbeit zu reduzieren, ohne feste Links anzuwenden, kann ein Trick angewendet werden: Ein Auftrag wird zweimal geplant, und für den zweiten Durchgang wird die entgegengesetzte Richtung verwendet. Wenn der erste Zeitplan ab dem Liefertermin rückwärts erstellt wurde, sollte der zweite ab dem geplanten Startdatum vorwärts erstellt werden. Dies führt dazu, dass die Arbeitsgänge so weit wie möglich komprimiert werden, sodass die laufende Arbeiten minimiert wird.

### <a name="separate-calendar-for-each-resource"></a>Separater Kalender für jede Ressource

Eine der Hauptdatenquellen für das Planungsmodul sind Kalenderinformationen, deren Laden aus der Datenbank teuer sein kann. Da Kalender basierend auf Vorlagen generiert werden, wäre es verlockend, für jede Ressource einen Kalender zu generieren und dann die Informationen in diesem Kalender anzupassen, wenn die Ressource Ausfallzeiten und andere Probleme aufweist. Dies schränkt jedoch die Fähigkeit der Module, die Kalenderdaten zwischenzuspeichern, erheblich ein, da sie neue Daten für jede Ressource anfordern müssten, was eine große Quelle von Leistungsproblemen sein kann. Stattdessen empfehlen wir, dass Sie die Kalender so weit wie möglich zwischen den Ressourcen wiederverwenden und dann Änderungen der Ausfallzeit steuern, indem Sie für einen bestimmten Zeitraum eine andere Kalender-ID zuweisen.

### <a name="high-number-of-working-time-slots-per-calendar-day"></a>Hohe Anzahl der Arbeitszeitfenster pro Kalendertag

Da das Modul die Zeitfenster einzeln auf ihre Kapazität überprüft, ist es vorteilhaft, die Anzahl der Zeitfenster pro Kalendertag zu minimieren. Dies könnte zum Beispiel dadurch geschehen, dass überlegt wird, ob es wichtig ist, dass der resultierende Zeitplan widerspiegelt, dass die Arbeitskräfte jede Stunde eine Pause von 5 Minuten einlegen.

### <a name="large-or-none-scheduling-timeouts"></a>Große (oder keine) Planungszeitüberschreitungen

Die Leistung des Planungsmoduls kann mithilfe der Parameter auf der Seite **Planungsparameter** optimiert werden. Die Einstellungen **Zeitlimit für Zeitplanung aktiviert** und **Zeitlimit für Planungsoptimierung aktiviert** sollten immer auf **Ja** eingestellt sein. Sind sie auf **Nein** gesetzt, kann die Planung möglicherweise unbegrenzt ausgeführt werden, wenn ein nicht realisierbarer Arbeitsplan mit vielen Optionen erstellt wurde.

Der Wert für **Maximale Planungszeit pro Sequenz** steuert, wie viele Sekunden höchstens für die Suche nach einer Lösung für eine einzelne Sequenz aufgewendet werden können (in den meisten Fällen entspricht eine Sequenz einem einzelnen Auftrag). Der hier zu verwendende Wert hängt stark von der Komplexität des Arbeitsplans und den Einstellungen wie der begrenzten Kapazität ab, aber ein Maximum von etwa 30 Sekunden ist ein guter Ausgangspunkt.

Der Wert für **Zeitlimit für Optimierungsversuche** steuert, wie viele Sekunden höchstens verwendet werden können, um eine bessere Lösung als die ursprünglich gefundene zu finden. Dies wirkt sich nur auf Arbeitspläne aus, die parallele Arbeitsgänge verwenden, da diese das Testen verschiedener Kombinationen erforderlich machen.

> [!NOTE]
> Die für die Zeitüberschreitungen festgelegten Werte werden sowohl für die Planung von freigegebenen Produktionsaufträgen und von geplanten Aufträgen im Rahmen der Materialbedarfsplanung angewendet. Infolgedessen kann das Festlegen sehr hoher Werte die Laufzeit der Materialbedarfsplanung erheblich verlängern, wenn ein Plan mit vielen geplanten Produktionsaufträgen ausgeführt wird.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]