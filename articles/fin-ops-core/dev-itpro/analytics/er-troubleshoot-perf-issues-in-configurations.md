---
title: Beheben von Leistungsproblemen in ER-Konfigurationen
description: In diesem Artikel wird erläutert, wie Sie Leistungsprobleme in Konfigurationen für die elektronische Berichterstellung (EB) finden und beheben.
author: NickSelin
ms.date: 05/12/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner, ERFormatMappingRunJobTable, ERParameters, ERSolutionTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: maximbel
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 28ff68309bad7a6c1b6009ba03ef4b20aceb5194
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8847339"
---
# <a name="troubleshooting-performance-issues-in-er-configurations"></a>Beheben von Leistungsproblemen in ER-Konfigurationen

In diesem Artikel wird erläutert, wie Sie Leistungsprobleme in [Konfigurationen](general-electronic-reporting.md#Configuration) für die [elektronische Berichterstellung](general-electronic-reporting.md) (EB) finden und beheben.

In der Regel besteht die Leistungsuntersuchung aus mehreren Schritten.

1. [Daten](#collecting-data) sammeln.
2. Die gesammelten Daten analysieren.
3. Verwenden Sie basierend auf den Ergebnissen der Analyse ER-Konfigurationen, um [Änderungen vornehmen](#making-changes), oder beschließen, weitere Daten zu sammeln.

## <a name="troubleshooting"></a>Problembehandlung

### <a name="analyze-execution-time"></a>Ausführungszeit analysieren

Die Ausführungszeit kann von unvorhersehbaren Faktoren abhängen, z. B. von anderen Aufgaben, die in derselben Umgebung ausgeführt werden, und Zwischenspeichern, die beim ersten Aufruf Daten verwenden. Daher sollten Sie die Durchführung und Messung mehrmals wiederholen.

Manchmal werden Leistungsprobleme nicht durch eine ER-Formatkonfiguration verursacht, die für die Berichterstellung verwendet wird. Stattdessen werden sie durch den X++-Code verursacht, der zum Öffnen dieser ER-Formatkonfiguration verwendet wird.

1. Entweder im [Aktionszentrum](#infolog-time) oder im [Ereignisprotokoll](#event-log-time) sehen Sie sich die Ausführungszeit des Berichts an.
2. Vergleichen Sie die Ausführungszeit des Reports mit der Gesamtausführungszeit im Szenario.
3. Wenn die Ausführungszeit des Berichts viel kürzer ist als die Gesamtausführungszeit, berücksichtigen Sie die Datenmenge, die der Bericht verarbeitet:

    - Wenn der Bericht eine kleine Datenmenge verarbeitet, kann das Problem an der Ladezeit der Konfiguration liegen.
    - Wenn der Bericht eine große Datenmenge verarbeitet, kann das Problem die Vorverarbeitung von X++ beinhalten. [Trace-Parser](#analyze-trace-parser-trace) verwenden, um diesen Fall zu analysieren.

    Für andere Fälle siehe die nächsten Abschnitte.

4. Führen Sie mehrere Tests mit unterschiedlichen Datenmengen aus, um zu ermitteln, wie die Ausführungszeit von der Datenmenge abhängt.

### <a name="analyze-trace-parser-traces"></a><a name="analyze-trace-parser-trace"></a>Spuren von Trace Parsern analysieren

Bereiten Sie ein kleines Beispiel vor oder sammeln Sie mehrere Traces während zufälliger Teile der Berichtserstellung.

Dann in [Trace Parser](#trace-parser) führen Sie eine standardmäßige Bottom-Up-Analyse durch und beantworten Sie die folgenden Fragen:

- Was sind die Top-Methoden in Bezug auf den Zeitverbrauch?
- Welchen Teil der Gesamtzeit verwenden diese Methoden?

Beantworten Sie die gleichen Fragen für Anfragen.

Wenn Sie sehen, dass Methoden das Präfix „ER“ voranstellen, fahren Sie mit dem nächsten Abschnitt fort.

Wenn Sie feststellen, dass Methoden oder Abfragen aus der Anwendungssuite stammen, sollten Sie generische Optimierungen in Betracht ziehen (z. B. Indizes erstellen).

Analysieren Sie die Anzahl der Anrufe. Wenn die Zahl deutlich höher als erwartet ist, sollten Sie die entsprechenden Knoten der Konfiguration zwischenspeichern.

### <a name="analyze-database-calls"></a><a name="analyze-database-calls"></a>Datenbankaufrufe analysieren

Bereiten Sie ein Beispiel mit einer kleinen Datenmenge vor, damit Sie eine [ER-Spur](#electronic-reporting-traces) erfassen können.

Öffnen Sie dann die Ablaufverfolgung im ER-Modellzuordnungsdesigner und sehen Sie sich den unteren Teil der Seite an. Beantworten Sie folgende Fragen:

- Gibt es eine doppelte Abfrage? Wenn ja, ziehen Sie eine der folgenden Korrekturen in Betracht:

    - [Caching verwenden](#use-caching), wenn Sie der Meinung sind, dass mehrere Aufrufe in einem übergeordneten Datensatz vorhanden sind.
    - [Verwenden Sie ein zwischengespeichertes, parametrisiertes berechnetes Feld](#cached-parameterized), wenn Sie der Meinung sind, dass Aufrufe für denselben Datensatz in verschiedenen Datensätzen vorhanden sind.
    - [Verwenden eine **JOIN**-Datenquelle](#use-join-datasource), wenn Sie eine beträchtliche Anzahl verschiedener Datensätze aus einer Datenbank lesen müssen.

- Entspricht die Anzahl der Abfragen und geholten Datensätze der Gesamtdatenmenge? Wenn ein Dokument beispielsweise 10 Zeilen hat, zeigen die Statistiken, dass der Bericht 10 Zeilen oder 1.000 Zeilen extrahiert? Wenn Sie über eine beträchtliche Anzahl von abgerufenen Datensätzen verfügen, ziehen Sie eine der folgenden Korrekturen in Betracht:

    - [Verwenden Sie die **FILTER**-Funktion statt der **WHERE**-Funktion](#filter), um Daten auf der Microsoft SQL Server-Seite zu verarbeiten.
    - Verwenden Sie Caching, um zu vermeiden, dass dieselben Daten abgerufen werden.
    - [Verwenden Sie die Funktionen für erfasste Daten](#collected-data), um zu vermeiden, dass dieselben Daten für die Zusammenfassung abgerufen werden.

### <a name="analyze-perfview-traces"></a>Analysieren Sie PerfView-Traces

[PerfView](#perfview) ist ein Tool für erfahrene Entwickler. Ausführlichere Informationen zu den folgenden Schritten finden Sie unter [Grundlagen der Wanduhr-Zeitermittlung](https://channel9.msdn.com/Series/PerfView-Tutorial/Tutorial-12-Wall-Clock-Time-Investigation-Basics).

1. Sammeln Sie eine Ablaufverfolgung, indem Sie die Thread-Zeit verwenden.
2. Nur Stapel einschließen, die **runUnattended** verwenden, um nur den Thread zu filtern, der über die Konfigurationsausführung verfügt. (**runUnattended** zum Eingabefeld **IncPats** hinzufügen.)
3. Falten Sie alle CPU-, Netzwerk- und blockierten Zeiten.
4. [ER-Voreinstellungen für PerfView](https://download.microsoft.com/download/2/d/0/2d037b0f-ffd1-4d65-b64f-fcdf51f2c81f/ER_PerfViewPresets.xml) laden.
5. Wählen Sie **ER** \> **Andere Voreinstellung**.
6. Schau dir die Namen an:

    - Sie werden wahrscheinlich den Plattformcode sehen, der die meiste Zeit verbraucht.
    - Sie können doppeltippen (oder doppelklicken) und nach oben zu **Angerufene** gehen.

        Wenn Sie Klassen mit dem Präfix „ERExpression“ finden und es sich um Funktionen handelt, die sich auf Formeln beziehen, können Sie den Funktionsnamen anhand des Klassennamens erraten und im ER-Repository nach den Attributen suchen.

### <a name="fixes"></a>Korrekturen

- Wenn Sie feststellen, dass die meiste CPU-Zeit von Abfragen verbraucht wird, versuchen Sie, die Anzahl der Abfragen zu reduzieren:

    - [Überprüfen Sie die ER-Spur](#analyze-database-calls) auf doppelte Abfragen.
    - Sehen Sie, wie viele Datensätze abgerufen werden, und bewerten Sie, wie viele Daten theoretisch abgerufen werden sollten.

- Wenn Sie feststellen, dass die meiste CPU-Zeit von den verwendeten Funktionen verbraucht wird, versuchen Sie, die Stelle in der Konfiguration zu finden, die die meisten Ressourcen verbraucht.
- Wenn Sie feststellen, dass die meiste CPU-Zeit von Datenerfassungsfunktionen verbraucht wird, sollten Sie sie durch them ersetzen *SQL-Gruppe nach* auf der Modellzuordnungsseite.

### <a name="collecting-data"></a><a name="collecting-data"></a>Datenerfassung

Abhängig von Ihrer Umgebung gibt es mehrere Möglichkeiten, verfügbare Daten zu sammeln:

- Die Gesamtlaufzeit abrufen:

    - Aus dem Aktionszentrum
    - Aus dem Ereignisprotokoll

- Profil der Ausführung:

    - Durch die Verwendung von ER-Tools
    - Mit dem Trace Parser
    - Durch die Verwendung von PerfView

#### <a name="collecting-data-in-a-production-environment"></a>Sammeln von Daten in einer Produktionsumgebung

Manchmal können Probleme nur in einer Produktionsumgebung reproduziert werden. Sie können Daten auf folgende Arten sammeln:

- Mit [Trace Parser](../perf-test/trace-trace-tutorial.md)-Spuren
- Durch die Nutzung von [ER-Ausführung](trace-execution-er-troubleshoot-perf.md)-Spuren
- Durch Nutzung der gesamten Ausführungszeit

#### <a name="collecting-data-in-a-development-environment"></a>Sammeln von Daten in einer Entiwcklungsumgebung

Neben den Tools, die in einer Produktionsumgebung verwendet werden können, gibt es mehrere Tools, die Sie in einer Entwicklungsumgebung verwenden können:

- Ereignisprotokoll (Microsoft-Dynamics-ElectronicReporting). Dieses Protokoll kann Ihnen die Gesamtausführungszeit anzeigen.
- Gängige .NET-Tools wie PerfView.

Darüber hinaus bietet Ihnen eine Entwicklungsumgebung mehr Flexibilität beim Experimentieren. Sie können beispielsweise Teile von Berichten deaktivieren, um zu sehen, wie sich dies auf die Ausführungszeit auswirkt.

### <a name="tools"></a><a name="tools"></a>Extras

#### <a name="execution-time-in-the-action-center"></a><a name="infolog-time"></a>Ausführungszeit im Action Center

ER kann die Ausführungszeit der Konfiguration im Action Center anzeigen. Diese Option funktioniert nur für einen bestimmten Benutzer und ein bestimmtes Unternehmen und nur für interaktive Sitzungen. Gehen Sie folgendermaßen vor, um diese Funktion verfügbar zu machen.

1. Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.
2. Auf der Seite **Konfigurationen** im Aktivitätsbereich, auf der Registerkarte **Konfigurationen** in der Gruppe **Erweiterte Einstellungen** wählen Sie **Benutzerparameter** aus.
3. Im Dialogfeld **Benutzerparameter** setzen Sie die Option **Dateierstellungszeit anzeigen** auf **Ja**.

#### <a name="execution-time-in-the-event-log"></a><a name="event-log-time"></a>Ausführungszeit im Ereignisprotokoll

1. Öffnen Sie die Windows-Ereignisanzeige.
2. Öffnen Sie unter **Anwendungs- und Dienstprotokolle** die Option **Microsoft-Dynamics-ElectronicReporting/Operational**.
3. Suchen Sie nach **FormatMappingRun**-Ereignissen, bei denen **Ereignis-ID=2**, da diese Ereignisse die Informationen über die verstrichene Zeit enthalten.

#### <a name="trace-parser-traces"></a><a name="trace-parser"></a>Spuren von Trace Parsern 

Da ER in X++ implementiert ist, können Sie gängige X++-Tools verwenden, um die Leistung zu analysieren. Weitere Informationen finden Sie unter [Erfassen von Spuren mit dem Trace Parser](../perf-test/trace-trace-tutorial.md).

Dieser Ansatz unterliegt einigen Einschränkungen. Da ein Teil von ER in C# implementiert ist, sind nicht alle Details verfügbar. Sie können jedoch die Datennutzungsdetails anzeigen. Darüber hinaus können lange Berichtsausführungen die Speicherbeschränkungen für Traces überschreiten.

#### <a name="er-traces"></a><a name="electronic-reporting-traces"></a>ER-Spuren

ER kann seine eigenen Spuren sammeln und verfügt über Visualisierungs- und Analysetools für diese Spuren. Weitere Informationen finden Sie unter [Überwachen der Ausführung von EB-Formaten zur Behebung von Leistungsproblemen](trace-execution-er-troubleshoot-perf.md).

#### <a name="perfview"></a><a name="perfview"></a>PerfView

Da sowohl X++ als auch ER auf der .NET-Plattform implementiert sind, können Sie gängige .NET-Tools verwenden. Sie können zum Beispiel das kostenlose [PerfView](https://github.com/Microsoft/perfview)-Tool verwenden.

Sie können auch Daten über die Befehlszeile sammeln. Das folgende Windows PowerShell-Skript erfasst beispielsweise die Ausführungszeit, bis die Formatausführung auf dem Computer beendet wird.

```powershell
c:\programs\PerfView collect "e:\traces\$(date -format "ddMMyyyy_hhmm").etl" `
    -CircularMB:20000 -ThreadTime `
    -NoNGenRundown `
    -StopOnEtwEvent:Microsoft-Dynamics-ElectronicReporting/FormatMappingRun/Stop
```

Dieser Ansatz unterliegt einigen Einschränkungen. Sie müssen Administratorzugriff auf den Computer besitzen. Darüber hinaus müssen Sie ein erfahrener Entwickler sein, da die Lernkurve steil ist.

### <a name="making-changes"></a><a name="making-changes"></a>Änderungen vornehmen

#### <a name="use-caching"></a><a name="use-caching"></a>Caching verwenden

Das Caching verkürzt zwar die Zeit, die zum erneuten Abrufen von Daten erforderlich ist, kostet jedoch Speicher. Verwenden Sie Caching in Fällen, in denen die Menge der abgerufenen Daten nicht sehr groß ist. Weitere Informationen und ein Beispiel zur Verwendung von Caching finden Sie unter [Verbessern der Modellzuordnung basierend auf Informationen aus dem Ausführungsspur](trace-execution-er-troubleshoot-perf.md#improve-the-model-mapping-based-on-information-from-the-execution-trace).

#### <a name="reduce-volume-of-data-fetched"></a><a name="reduce-fetched-data"></a>Die Menge der abgerufenen Daten reduzieren

Sie können den Speicherverbrauch für das Zwischenspeichern reduzieren, indem Sie die Anzahl der Felder in den Datensätzen einer Anwendungstabelle begrenzen, die Sie zur Laufzeit abrufen. In diesem Fall rufen Sie nur die Feldwerte einer Anwendungstabelle ab, die Sie in Ihrer ER-Modellzuordnung benötigen. Andere Felder in dieser Tabelle werden nicht abgerufen. Daher wird das Speichervolumen, das zum Zwischenspeichern abgerufener Datensätze erforderlich ist, reduziert. Weitere Informationen finden Sie unter [Verbessern der Leistung von ER-Lösungen, indem die Anzahl der Tabellenfelder reduziert wird, die zur Laufzeit abgerufen werden](er-reduce-fetched-fields-number.md)

#### <a name="use-a-cached-parameterized-calculated-field"></a><a name="cached-parameterized"></a>Verwenden Sie ein zwischengespeichertes, parametrisiertes berechnetes Feld

Manchmal müssen Werte wiederholt nachgeschlagen werden. Beispiele sind Kontonamen und Kontonummern. Um Zeit zu sparen, können Sie ein berechnetes Feld mit Parametern auf der obersten Ebene erstellen und das Feld dann zum Cache hinzufügen.

Es wird empfohlen, diesen Ansatz nur zu verwenden, wenn die Größe der zwischengespeicherten Daten gering ist. Weitere Informationen finden Sie unter [Verbessern der Leistung von ER-Lösungen durch Hinzufügen parametrisierter CALCULATED FIELD-Datenquellen](er-calculated-field-ds-performance.md).

#### <a name="use-a-join-data-source"></a><a name="use-join-datasource"></a>JOIN-Datenquelle verwenden

Eine **JOIN**-Datenquelle ermöglicht das Abrufen mehrerer verbundener Datensätze mit einer Abfrage. Es muss nicht eine separate Abfrage verwendet werden, um jeden verbundenen Datensatz abzurufen. Wenn Sie beispielsweise 1.000 Zeilen haben und Artikeldaten für jede Zeile nach Relation abrufen, haben Sie 1.001 Abfragen (= 1.000 + 1). Wenn Sie eine **JOIN**-Datenquelle verwenden, verwenden Sie nur eine Abfrage, um dieselben Daten abzurufen. Weitere Informationen finden Sie unter [JOIN-Datenquellenzuordnungen verwenden, um Daten aus mehreren Anwendungstabellen abzurufen](er-join-data-sources.md).

#### <a name="use-the-filter-function-instead-of-the-where-function"></a><a name="filter"></a>Verwenden Sie die FILTER-Funktion anstelle der WHERE-Funktion

Die **[FILTER](er-functions-list-filter.md)**-Funktion führt Bedingungen auf SQL Server aus, während die **WHERE**-Funktion alle Daten aus der Liste abruft, einen Datensatz nach dem anderen, und die Bedingung für jeden Datensatz anwendet. Sie möchten beispielsweise einen Datensatz aus 1.000 Datensätzen auswählen. Wenn Sie **WHERE** verwenden, werden alle 1.000 Datensätze abgerufen. Wenn Sie jedoch **FILTER** verwenden, wird genau ein Datensatz geholt. **FILTER** kann auch datenbankseitig Indizes verwenden.

#### <a name="using-collected-data-functions-or-an-accumulated-data-data-source"></a><a name="collected-data"></a>Verwenden von Funktionen für gesammelte Daten oder einer Datenquelle für gesammelte Daten

Wenn Ihre Konfiguration ein *gruppiere nach*-Komponente hat, die zuvor abgerufene Daten nach Bericht zusammenfasst, ruft die Komponente alle Daten erneut ab. Durch die Verwendung von Funktionen für gesammelte Daten ermöglichen Sie ER, Daten während des ersten Abrufs zu sammeln. Weitere Informationen finden Sie unter [Konfigurieren des ER-Formats für Inventuren und Summierungen](tasks/er-format-counting-summing-2.md).

#### <a name="rewrite-parts-of-the-configuration-in-x"></a>Teile der Konfiguration in X++ umschreiben

ER unterstützt Aufrufmethoden von Tabellen und Klassen, einschließlich Erweiterungen. Ziehen Sie in Betracht, Teile der Modellzuordnung in X++ umzuschreiben, um die Leistung zu verbessern.

ER kann Daten aus den folgenden Quellen verbrauchen:

- Klassen (Datenquellen **Objekt** und **Klasse**)
- Tabellen (Datenquellen **Tabelle** und **Tabellendatensätze** Datenquellen)

Das [ER-Schnittstelle für die Anwendungsprogrammierung API](er-apis-app73.md#how-to-access-internal-x-objects-by-using-erobjectsfactory) bietet auch eine Möglichkeit, vorberechnete Daten aus dem aufrufenden Code zu senden. Die Anwendungssuite enthält zahlreiche Beispiele für diesen Ansatz.
