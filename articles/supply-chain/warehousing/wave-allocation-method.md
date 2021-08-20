---
title: Wellenzuteilung
description: In diesem Thema wird beschrieben, wie Sie den Wellenzuweisungsschritt einrichten und unter anderem die parallele Verarbeitung dafür aktivieren.
author: Mirzaab
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 9c534f5e10f5797543d56ff4a5a7ada937edcb017228ebe395ae8a45efa10886
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6781320"
---
# <a name="wave-allocation"></a>Wellenzuteilung

[!include [banner](../includes/banner.md)]

Die Wellenverarbeitung kann zeitaufwändig sein, und der größte Teil der Verarbeitungszeit wird bei der Zuteilung und der Arbeitserstellung verbracht.

Diese Schritte können jetzt parallel ausgeführt werden, wodurch die Leistung der Wellenverarbeitung verbessert und ein größerer Wellendurchsatz im selben Lagerort ermöglicht wird. In diesem Thema wird erklärt, wie Sie die Wellenzuteilungsmethode für eine parallele Ausführung einrichten. Weitere Informationen zum Einrichten der parallelen Ausführung der Arbeitserstellung finden Sie unter [Planen der Arbeitserstellung während der Welle](configure-wave-schedule-work-creation.md).

Bisher war es immer nur möglich, jeweils eine Welle in einem Lagerort zuzuteilen. Diese Einschränkung wurde entfernt und durch eine neue Einschränkung ersetzt, die nur den Artikel und die Dimensionen sperrt, die sich in der Reservierungshierarchie über dem Lagerplatz befindet. Dimensionen über dem Lagerplatz enthalten immer Produktdimensionen. Zum Beispiel, wenn ein Artikel mit *Farbe* konfiguriert ist, können Varianten für *Rot*, *Blau* und *Gelb* jeweils parallel verarbeitet werden.

Dies bedeutet, dass, wenn derselbe Artikel mit denselben Dimensionen über dem Lagerplatz einer Welle zugewiesen wird, andere Wellen warten müssen, um eine Sperre für denselben Artikel und dieselben Dimensionen zu erhalten. Wenn die Sperre nicht rechtzeitig eingesetzt werden kann, tritt ein Fehler auf und die Wellenverarbeitung schlägt fehl.

Um die Parallelverarbeitung nutzen zu können, muss die Welle als Stapel verarbeitet werden.

## <a name="performance-improvements"></a>Leistungsverbesserungen

Die Leistungsvorteile der Parallelverarbeitung lassen sich in zwei Kategorien einteilen:

- **Verbesserter Durchsatz** – Der Durchsatz von Wellen verbessert sich normalerweise auch dann, wenn die Parallelverarbeitung nicht konfiguriert ist, insbesondere in Szenarien, in denen innerhalb der Wellen keine Artikel überlappen.
- **Verbesserung der Zuteilung für eine einzelne Welle** – Tests mit Kundendaten haben nach der Umstellung auf die parallele Zuteilung eine Leistungsverbesserung von fast 50 % ergeben. Die parallele Verarbeitung erfolgt nach Artikeln und Dimensionen über dem Lagerplatz. Die Verbesserungen hängen also davon ab, wie viele verschiedene Artikel eine Welle enthält, welche Infrastruktur verfügbar ist und wie lange die Zuteilung im Vergleich zur Dauer der Arbeitserstellung dauert.

## <a name="configure-parallel-allocation"></a>Eine parallele Zuteilung konfigurieren

### <a name="warehouse-management-parameters"></a>Parameter für Lagerortverwaltung

Um die parallele Zuteilungsverarbeitung zu verwenden, gehen Sie zu **Lagerortverwaltung > Einstellungen > Lagerortverwaltungsparameter**, öffnen Sie die Registerkarte **Wellenverarbeitung** und nehmen Sie die folgenden Einstellungen vor:

- **Wellenverarbeitungs-Stapelverarbeitungsgruppe** – Wählen Sie die Stapelverarbeitungsgruppe aus, die für die erste Verarbeitung der Wellen verwendet werden soll. Die nachfolgende Verarbeitung der Zuteilung kann mit verschiedenen Stapelverarbeitungsgruppen erfolgen.
- **Wellen in einem Stapel verarbeiten** – Setzen Sie diese Option auf *Ja*, um die parallele Verarbeitung zu verwenden.
- **Auf Sperre (ms) warten** – Geben Sie die Uhrzeit ein, in Millisekunden, die ein Zuteilungsschritt auf eine Systemressource wartet, die von einem anderen Zuteilungsschritt gesperrt ist. Bei Überschreitung dieser Zeit wird, wird die Welle nicht verarbeitet und eine Fehlermeldung wird angezeigt. Wir empfehlen, dass Sie mindestens einige Sekunden einplanen, damit die Zuteilung einer logischen Einheit abgeschlossen werden kann.

Informationen zu diesen und anderen Wellenverarbeitungsoptionen auf der Seite **Lagerortverwaltungsparameter** finden Sie unter [Lagerortparameter für Wellenverarbeitung](wave-warehouse-parameters.md).

## <a name="wave-process-methods"></a>Wellenverarbeitungsmethoden

So richten Sie die parallele Verarbeitung ein:

1. Gehen Sie zu **Lagerortverwaltung > Einstellungen > Wellen > Wellenverarbeitungsmethoden**.
1. Wählen Sie die Methode `allocateWave` im Raster aus.
1. Wählen Sie im Aktivitätsbereich **Aufgabenkonfiguration** aus.
1. Die Seite **Konfiguration der Wellenbuchungsmethodenaufgabe** wird geöffnet. Dieses Raster listet alle Lagerorte auf, in denen Sie die `allocateWave`-Methode konfiguriert haben. Die parallele Verarbeitung wird nur für aufgeführte Lagerorte verwendet. Verwenden Sie die Schaltflächen im Aktivitätsbereich, um Lagerorte nach Bedarf zum Raster hinzuzufügen oder daraus zu entfernen. 
1. Nehmen Sie für jeden Lagerort die folgenden Einstellungen vor:
    - **Maximale Anzahl an Stapelverarbeitungsaufgaben** – Geben Sie die Anzahl der Stapelverarbeitungsaufgaben an, die für die Zuteilung für den ausgewählten Lagerort verwendet werden sollen. Die optimale Anzahl an Stapelverarbeitungsaufgaben hängt von der verfügbaren Infrastruktur und den anderen Stapelverarbeitungen ab, die auf dem Server verarbeitet werden. Tests, die in einer Umgebung mit vier Kernen für die Wellenverarbeitung durchgeführt wurden, zeigten, dass die Verwendung von acht Aufgaben zu guten Ergebnissen führte.
    - **Wellenverarbeitungs-Stapelverarbeitungsgruppe** – Bestimmte Stapelverarbeitungsgruppen können für verschiedene Lagerorte verwendet werden, damit die Zuteilungsverarbeitung pro Lagerort erweitert werden kann.

## <a name="enable-or-disable-parallelization-across-all-legal-entities"></a>Die Parallelisierung für alle juristischen Personen aktivieren oder deaktivieren

Wir empfehlen Ihnen, die `allocateWave`-Methode so einzustellen, dass sie parallel über alle juristischen Personen hinweg ausgeführt wird, da dies zur Verbesserung der Leistung der Wellenverarbeitung beiträgt. Ab Version 10.0.17 von Supply Chain Management ist die Funktion *Wellenparallelisierung für Wellenzuweisungsmethode* standardmäßig für alle neuen und aktualisierten Installationen aktiviert und kann nicht wieder deaktiviert werden. Nach dem Aktivieren dieser Funktion geschieht Folgendes:

- Die `allocateWave`-Methode wurde aktualisiert und enthält nun eine Aufgabenkonfigurationseinstellung, mit der Sie die Seite **Wellenverarbeitungsmethoden** verwenden können, um die Anzahl der Aufgaben festzulegen, die, entsprechend der Anzahl der parallelen Prozesse, gleichzeitig ausgeführt werden. Infolgedessen wird die für die Wellenzuteilung gebrauchte Zeit (typischerweise 30 bis 60 % der gesamten Verarbeitungszeit) um einen Faktor reduziert, der in etwa der Anzahl der Aufgaben entspricht. Sie können auch auswählen, welchem Stapel die Verarbeitung dieser Aufgaben zugewiesen werden soll. Es ist wichtig zu beachten, dass alle Ihre juristischen Personen so konfiguriert werden, dass Wellen im Stapel verarbeitet werden. Für die Lagerorte, die bereits für die Stapelverarbeitung von Wellen oder der parallelen Verwendung der `allocateWave`-Methode konfiguriert sind, wird die vorhandene Konfiguration beibehalten.
- Standardmäßig sind alle neuen juristischen Personen so konfiguriert, dass Wellen im Stapel verarbeitet werden. Bei allen neuen Lagerorte, bei denen die Option **Lagerortverwaltungsprozesse** aktiviert ist, ist die `allocateWave`-Methode so konfiguriert, dass sie standardmäßig parallel läuft.
- Auf der Seite **Lagerortverwaltungsparameter** ist **Prozess speichert im Stapel** auf *Ja* und **Auf Sperre (ms) warten** auf einen Standardwert von 15 Sekunden eingestellt. Dies bedeutet, dass alle Wellen im Stapel ausgeführt werden. Wenn eine Welle läuft, erhält sie während des Zuteilungsschritts eine Sperre für das Element und die Dimension über der Position. Wenn eine andere Wellenverarbeitungsaufgabe versucht, dieselbe Sperre für den identischen Datensatz abzurufen, wird sie blockiert, bis der aktuelle Prozess abgeschlossen ist. Die Einstellung **Auf Sperre (ms) warten** legt die maximale Wartezeit des Systems fest, bevor die Sperre aufgehoben wird.

Für die parallele Verarbeitung von Zuweisungen muss die Welle als Stapelverarbeitung laufen. Daher verringern Sie die Wellenverarbeitungsleistung, wenn Sie die Einstellung **Prozess speichert im Stapel** deaktivieren, insbesondere, wenn die Wellenverarbeitung einen parallelen Prozess verwendet, wie in der Aufgabenkonfiguration für die entsprechenden Wellenmethoden definiert.

Bei Bedarf können Sie jede der standardmäßig vorgenommenen Einstellungen rückgängig machen, wenn die Funktion *Wellenparallelisierung für Wellenzuweisungsmethode* automatisch für Ihre Instanz aktiviert ist. Aktion:

- Gehen Sie zu **Lagerortverwaltung\>Einstellungen \> Lagerortverwaltungsparameter**. Wenden Sie auf der Registerkarte **Wellenverarbeitung** Ihre bevorzugten Werte für **Wellen in einem Stapel verarbeiten** und **Auf Sperre (ms) warten**.
- Wechseln Sie zu **Lagerortverwaltung \> Setup \> Wellen \> Wellenverarbeitungsmethoden**. Wählen Sie die `allocateWave`-Methode aus. Wählen Sie im Aktivitätsbereich die Option **Aufgabenkonfiguration** aus, um eine Seite zu öffnen, auf der jeder Lagerort aufgelistet ist, für den die Methode parallel ausgeführt werden soll. Ändern oder löschen Sie nach Bedarf die Anzahl der Stapelverarbeitungsaufgaben und die zugewiesene Wellengruppe für die einzelnen aufgeführten Lagerorte.

## <a name="troubleshooting"></a>Problembehandlung

### <a name="troubleshoot-using-the-infolog"></a>Problembehandlung mit dem Infolog

Da das Stapelverarbeitungs-Framework verwendet wird, werden Fehler, die während der Wellenverarbeitung auftreten, als Teil der Infologs für Stapelverarbeitungen erfasst. Um die Stapelverarbeitungsaufträge zu lesen, die sich auf eine Welle beziehen:

1. Wechseln Sie zu **Lagerortverwaltung \> Ausgehende Wellen \> Lieferungswellen \> Alle Wellen**.
1. Wählen Sie die Welle aus, die Sie sich ansehen möchten.
1. Öffnen Sie im Aktivitätsbereich die Registerkarte **Welle** und wählen Sie aus der Gruppe **Welle** **Stapelverarbeitungsaufträge** aus.

Die Wellenverarbeitung korrigiert sich selbst, daher sollte jeder während der Verarbeitung festgestellte Fehler mit dem Infolog gemeldet werden.

Ein typischer Fehler im Zusammenhang mit der parallelen Verarbeitung könnte sein, dass zwei Wellen versuchen, denselben Artikel gleichzeitig zuzuweisen, und eine Welle nicht abgeschlossen wird, sodass die andere nicht innerhalb der angegebenen Zeit eine Sperre erlangen kann. In diesem Fall enthält das Stapelaufgabenprotokoll Informationen, die besagen, dass die Sperre für den Artikel nicht erfasst werden konnte. In diesem Fall muss die fehlgeschlagene Welle erneut verarbeitet werden.

Da die Verarbeitung parallel erfolgt, müssen die Daten in verschiedenen Tabellen verwaltet werden, um den Status der Verarbeitung nachverfolgen zu können. Dies bedeutet, dass die Protokolle für die Stapelverarbeitungsaufträge möglicherweise Fehler enthalten, z. B. Doppelschlüssel.

Die Fehler aus den Stapelverarbeitungsaufgaben sind auch Teil des Protokolls der Stapelverarbeitungsaufträge. Die wichtigsten Informationen befinden sich normalerweise unten.

In seltenen Fällen, z. B. wenn die SQL-Verbindung beendet wurde, kann der Status der Wellenverarbeitung inkonsistent sein, in dem der Stapelverarbeitungsauftrag ausgeführt zu werden scheint, die Verarbeitung jedoch gestoppt wird. Die Welle kommt mit solchen Fehlern nicht zurecht, daher wird versucht, fehlgeschlagene Wellen zu bereinigen, wenn die nächste Welle ausgeführt wird. Wenn die aktuelle Welle einen inkonsistenten Status hat, führen Sie alternativ die folgenden Schritte aus:

1. Wechseln Sie zu **Lagerortverwaltung \> Ausgehende Wellen \> Lieferungswellen \> Alle Wellen**.
1. Wählen Sie die Welle aus, die Sie bereinigen möchten.
1. Öffnen Sie im Aktivitätsbereich die Registerkarte **Welle** und wählen Sie aus der Gruppe **Welle** **Wellendaten bereinigen** aus.

### <a name="troubleshoot-using-the-wave-progress-log"></a>Problembehandlung mithilfe des Wellenfortschrittsprotokolls

Wenn die Option **Wellenfortschrittsprotokoll erstellen** auf der Seite **Lagerortverwaltungsparameter** aktiviert ist, dann wird jedes Mal ein Protokolldatensatz erstellt, wenn die Zuteilung für einen Artikel und seine Dimensionen beginnt und endet. Sie sollten dieses Protokoll nur aktivieren, wenn Sie es benötigen, z. B. während des ersten Tests oder zur Problembehandlung. Wenn diese Option aktiviert ist, können Sie das Protokoll anzeigen, indem Sie die folgenden Schritte ausführen:

1. Wechseln Sie zu **Lagerortverwaltung \> Ausgehende Wellen \> Lieferungswellen \> Alle Wellen**.
1. Wählen Sie die Welle aus, die Sie sich ansehen möchten.
1. Öffnen Sie im Aktivitätsbereich die Registerkarte **Welle** und wählen Sie in der Gruppe **Welle** **Fortschritt** aus.
