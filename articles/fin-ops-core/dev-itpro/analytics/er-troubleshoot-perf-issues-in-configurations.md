---
title: Beheben von Leistungsproblemen in ER-Konfigurationen
description: In diesem Thema wird erläutert, wie Sie Leistungsprobleme in Konfigurationen für die elektronische Berichterstellung (ER) finden und beheben.
author: NickSelin
ms.date: 06/08/2021
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
ms.openlocfilehash: d77c2aad904ba911ac19009d6a981ea4153aaa48
ms.sourcegitcommit: 60afcd85b3b5b9e5e8981ebbb57c0161cf05e54b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216864"
---
# <a name="troubleshooting-performance-issues-in-er-configurations"></a><span data-ttu-id="7b8e8-103">Beheben von Leistungsproblemen in ER-Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="7b8e8-103">Troubleshooting performance issues in ER configurations</span></span>

<span data-ttu-id="7b8e8-104">In diesem Thema wird erläutert, wie Sie Leistungsprobleme in Konfigurationen für die [elektronische Berichterstellung](general-electronic-reporting.md) (ER) [finden und beheben](general-electronic-reporting.md#Configuration).</span><span class="sxs-lookup"><span data-stu-id="7b8e8-104">This topic explains how to find and solve performance issues in [Electronic reporting](general-electronic-reporting.md) (ER) [configurations](general-electronic-reporting.md#Configuration).</span></span>

<span data-ttu-id="7b8e8-105">In der Regel besteht die Leistungsuntersuchung aus mehreren Schritten.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-105">Typically, performance investigation consists of several steps.</span></span>

1. <span data-ttu-id="7b8e8-106">[Daten](#collecting-data) sammeln.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-106">[Collect](#collecting-data) data.</span></span>
2. <span data-ttu-id="7b8e8-107">Die gesammelten Daten analysieren.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-107">Analyze the collected data.</span></span>
3. <span data-ttu-id="7b8e8-108">Verwenden Sie basierend auf den Ergebnissen der Analyse ER-Konfigurationen, um [Änderungen vornehmen](#making-changes), oder beschließen, weitere Daten zu sammeln.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-108">Based on the results of the analysis, use ER configurations to [make changes](#making-changes), or decide to collect more data.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="7b8e8-109">Problembehandlung</span><span class="sxs-lookup"><span data-stu-id="7b8e8-109">Troubleshooting</span></span>

### <a name="analyze-execution-time"></a><span data-ttu-id="7b8e8-110">Ausführungszeit analysieren</span><span class="sxs-lookup"><span data-stu-id="7b8e8-110">Analyze execution time</span></span>

<span data-ttu-id="7b8e8-111">Die Ausführungszeit kann von unvorhersehbaren Faktoren abhängen, z. B. von anderen Aufgaben, die in derselben Umgebung ausgeführt werden, und Zwischenspeichern, die beim ersten Aufruf Daten verwenden.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-111">Execution time can depend on unpredictable factors, such as other tasks that are running in the same environment and caching that uses data when it's called for the first time.</span></span> <span data-ttu-id="7b8e8-112">Daher sollten Sie die Durchführung und Messung mehrmals wiederholen.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-112">Therefore, you should repeat the execution and measurement several times.</span></span>

<span data-ttu-id="7b8e8-113">Manchmal werden Leistungsprobleme nicht durch eine ER-Formatkonfiguration verursacht, die für die Berichterstellung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-113">Sometimes, performance issues aren't caused by an ER format configuration that is used for reporting.</span></span> <span data-ttu-id="7b8e8-114">Stattdessen werden sie durch den X++-Code verursacht, der zum Öffnen dieser ER-Formatkonfiguration verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-114">Instead, they are caused by the X++ code that is used to open that ER format configuration.</span></span>

1. <span data-ttu-id="7b8e8-115">Entweder im [Aktionszentrum](#infolog-time) oder im [Ereignisprotokoll](#event-log-time) sehen Sie sich die Ausführungszeit des Berichts an.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-115">In either the [Action center](#infolog-time) or the [event log](#event-log-time), look at the execution time of the report.</span></span>
2. <span data-ttu-id="7b8e8-116">Vergleichen Sie die Ausführungszeit des Reports mit der Gesamtausführungszeit im Szenario.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-116">Compare the execution time of the report with the total execution time in the scenario.</span></span>
3. <span data-ttu-id="7b8e8-117">Wenn die Ausführungszeit des Berichts viel kürzer ist als die Gesamtausführungszeit, berücksichtigen Sie die Datenmenge, die der Bericht verarbeitet:</span><span class="sxs-lookup"><span data-stu-id="7b8e8-117">If the execution time of the report is much less than the total execution time, consider the amount of data that the report processes:</span></span>

    - <span data-ttu-id="7b8e8-118">Wenn der Bericht eine kleine Datenmenge verarbeitet, kann das Problem an der Ladezeit der Konfiguration liegen.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-118">If the report processes a small amount of data, the issue might involve the loading time of the configuration.</span></span>
    - <span data-ttu-id="7b8e8-119">Wenn der Bericht eine große Datenmenge verarbeitet, kann das Problem die Vorverarbeitung von X++ beinhalten.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-119">If the report processes a large amount of data, the issue might involve preprocessing X++.</span></span> <span data-ttu-id="7b8e8-120">[Trace-Parser](#analyze-trace-parser-trace) verwenden, um diesen Fall zu analysieren.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-120">Use [Trace parser](#analyze-trace-parser-trace) to analyze this case.</span></span>

    <span data-ttu-id="7b8e8-121">Für andere Fälle siehe die nächsten Abschnitte.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-121">For other cases, see the next sections.</span></span>

4. <span data-ttu-id="7b8e8-122">Führen Sie mehrere Tests mit unterschiedlichen Datenmengen aus, um zu ermitteln, wie die Ausführungszeit von der Datenmenge abhängt.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-122">Run multiple tests that involve different amounts of data to determine how the execution time depends on the amount of data.</span></span>

### <a name="analyze-trace-parser-traces"></a><a name="analyze-trace-parser-trace"></a><span data-ttu-id="7b8e8-123">Spuren von Trace Parsern analysieren</span><span class="sxs-lookup"><span data-stu-id="7b8e8-123">Analyze Trace parser traces</span></span>

<span data-ttu-id="7b8e8-124">Bereiten Sie ein kleines Beispiel vor oder sammeln Sie mehrere Traces während zufälliger Teile der Berichtserstellung.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-124">Prepare a small example, or collect several traces during random parts of the report generation.</span></span>

<span data-ttu-id="7b8e8-125">Dann in [TraceParser](#trace-parser) führen Sie eine standardmäßige Bottom-to-Up-Analyse durch und beantworten Sie die folgenden Fragen:</span><span class="sxs-lookup"><span data-stu-id="7b8e8-125">Then, in [Trace parser](#trace-parser), do a standard bottom-to-up analysis, and answer the following questions:</span></span>

- <span data-ttu-id="7b8e8-126">Was sind die Top-Methoden in Bezug auf den Zeitverbrauch?</span><span class="sxs-lookup"><span data-stu-id="7b8e8-126">What are the top methods in terms of time consumption?</span></span>
- <span data-ttu-id="7b8e8-127">Welchen Teil der Gesamtzeit verwenden diese Methoden?</span><span class="sxs-lookup"><span data-stu-id="7b8e8-127">What part of the overall time do those methods use?</span></span>

<span data-ttu-id="7b8e8-128">Beantworten Sie die gleichen Fragen für Anfragen.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-128">Answer the same questions for queries.</span></span>

<span data-ttu-id="7b8e8-129">Wenn Sie sehen, dass Methoden das Präfix „ER“ voranstellen, fahren Sie mit dem nächsten Abschnitt fort.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-129">If you see that methods are prefixed with "ER," move on to the next section.</span></span>

<span data-ttu-id="7b8e8-130">Wenn Sie feststellen, dass Methoden oder Abfragen aus der Anwendungssuite stammen, sollten Sie generische Optimierungen in Betracht ziehen (z. B. Indizes erstellen).</span><span class="sxs-lookup"><span data-stu-id="7b8e8-130">If you see that methods or queries originated in the application suite, consider generic optimizations (for example, create indexes).</span></span>

<span data-ttu-id="7b8e8-131">Analysieren Sie die Anzahl der Anrufe.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-131">Analyze the number of calls.</span></span> <span data-ttu-id="7b8e8-132">Wenn die Zahl deutlich höher als erwartet ist, sollten Sie die entsprechenden Knoten der Konfiguration zwischenspeichern.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-132">If the number is significantly higher than expected, consider caching the corresponding nodes of the configuration.</span></span>

### <a name="analyze-database-calls"></a><a name="analyze-database-calls"></a><span data-ttu-id="7b8e8-133">Datenbankaufrufe analysieren</span><span class="sxs-lookup"><span data-stu-id="7b8e8-133">Analyze database calls</span></span>

<span data-ttu-id="7b8e8-134">Bereiten Sie ein Beispiel mit einer kleinen Datenmenge vor, damit Sie eine [ER-Spur](#electronic-reporting-traces) erfassen können.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-134">Prepare an example that has a small amount of data, so that you can collect an [ER trace](#electronic-reporting-traces).</span></span>

<span data-ttu-id="7b8e8-135">Öffnen Sie dann die Ablaufverfolgung im ER-Modellzuordnungsdesigner und sehen Sie sich den unteren Teil der Seite an.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-135">Then open the trace in the ER model mapping designer, and look at the bottom of the page.</span></span> <span data-ttu-id="7b8e8-136">Beantworten Sie folgende Fragen:</span><span class="sxs-lookup"><span data-stu-id="7b8e8-136">Answer the following questions:</span></span>

- <span data-ttu-id="7b8e8-137">Gibt es eine doppelte Abfrage?</span><span class="sxs-lookup"><span data-stu-id="7b8e8-137">Is there any query duplication?</span></span> <span data-ttu-id="7b8e8-138">Wenn ja, ziehen Sie eine der folgenden Korrekturen in Betracht:</span><span class="sxs-lookup"><span data-stu-id="7b8e8-138">If there is, consider one of the following fixes:</span></span>

    - <span data-ttu-id="7b8e8-139">[Caching verwenden](#use-caching), wenn Sie der Meinung sind, dass mehrere Aufrufe in einem übergeordneten Datensatz vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-139">[Use caching](#use-caching) if you think that there are several calls inside one parent record.</span></span>
    - <span data-ttu-id="7b8e8-140">[Verwenden Sie ein zwischengespeichertes, parametrisiertes berechnetes Feld](#cached-parameterized), wenn Sie der Meinung sind, dass Aufrufe für denselben Datensatz in verschiedenen Datensätzen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-140">[Use a cached, parameterized calculated field](#cached-parameterized) if you think that there are calls to the same record inside different records.</span></span>
    - <span data-ttu-id="7b8e8-141">[Verwenden eine **JOIN**-Datenquelle](#use-join-datasource), wenn Sie eine beträchtliche Anzahl verschiedener Datensätze aus einer Datenbank lesen müssen.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-141">[Use a **JOIN** data source](#use-join-datasource) if you have to read to a substantial number of different records from a database.</span></span>

- <span data-ttu-id="7b8e8-142">Entspricht die Anzahl der Abfragen und geholten Datensätze der Gesamtdatenmenge?</span><span class="sxs-lookup"><span data-stu-id="7b8e8-142">Does the number of queries and fetched records correspond to the overall amount of data?</span></span> <span data-ttu-id="7b8e8-143">Wenn ein Dokument beispielsweise 10 Zeilen hat, zeigen die Statistiken, dass der Bericht 10 Zeilen oder 1.000 Zeilen extrahiert?</span><span class="sxs-lookup"><span data-stu-id="7b8e8-143">For example, if a document has 10 lines, do the statistics show that the report extracts 10 lines or 1,000 lines?</span></span> <span data-ttu-id="7b8e8-144">Wenn Sie über eine beträchtliche Anzahl von abgerufenen Datensätzen verfügen, ziehen Sie eine der folgenden Korrekturen in Betracht:</span><span class="sxs-lookup"><span data-stu-id="7b8e8-144">If you have a substantial number of fetched records, consider one of the following fixes:</span></span>

    - <span data-ttu-id="7b8e8-145">[Verwenden Sie die **FILTER**-Funktion statt der **WHERE**-Funktion](#filter), um Daten auf der SQL Server-Seite zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-145">[Use the **FILTER** function instead of the **WHERE** function](#filter) to process data on the SQL Server side.</span></span>
    - <span data-ttu-id="7b8e8-146">Verwenden Sie Caching, um zu vermeiden, dass dieselben Daten abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-146">Use caching to avoid fetching the same data.</span></span>
    - <span data-ttu-id="7b8e8-147">[Verwenden Sie die Funktionen für erfasste Daten](#collected-data), um zu vermeiden, dass dieselben Daten für die Zusammenfassung abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-147">[Use collected data functions](#collected-data) to avoid fetching the same data for summarization.</span></span>

### <a name="analyze-perfview-traces"></a><span data-ttu-id="7b8e8-148">Analysieren Sie PerfView-Traces</span><span class="sxs-lookup"><span data-stu-id="7b8e8-148">Analyze PerfView traces</span></span>

<span data-ttu-id="7b8e8-149">[PerfView](#perfview) ist ein Tool für erfahrene Entwickler.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-149">[PerfView](#perfview) is a tool for experienced developers.</span></span> <span data-ttu-id="7b8e8-150">Ausführlichere Informationen zu den folgenden Schritten finden Sie unter [Grundlagen der Wanduhr-Zeitermittlung](https://channel9.msdn.com/Series/PerfView-Tutorial/Tutorial-12-Wall-Clock-Time-Investigation-Basics).</span><span class="sxs-lookup"><span data-stu-id="7b8e8-150">For more detailed information about the following steps, see [Wall Clock Time Investigation Basics](https://channel9.msdn.com/Series/PerfView-Tutorial/Tutorial-12-Wall-Clock-Time-Investigation-Basics).</span></span>

1. <span data-ttu-id="7b8e8-151">Sammeln Sie eine Ablaufverfolgung, indem Sie die Thread-Zeit verwenden.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-151">Collect a trace by using thread time.</span></span>
2. <span data-ttu-id="7b8e8-152">Nur Stapel einschließen, die **runUnattended** verwenden, um nur den Thread zu filtern, der über die Konfigurationsausführung verfügt.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-152">Include only stacks that use **runUnattended**, to filter only the thread that has configuration execution.</span></span> <span data-ttu-id="7b8e8-153">(**runUnattended** zum Eingabefeld **IncPats** hinzufügen.)</span><span class="sxs-lookup"><span data-stu-id="7b8e8-153">(Add **runUnattended** to the **IncPats** input box.)</span></span>
3. <span data-ttu-id="7b8e8-154">Falten Sie alle CPU-, Netzwerk- und blockierten Zeiten.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-154">Fold all CPU, network, and blocked time.</span></span>
4. <span data-ttu-id="7b8e8-155">[ER-Voreinstellungen für PerfView](https://download.microsoft.com/download/2/d/0/2d037b0f-ffd1-4d65-b64f-fcdf51f2c81f/ER_PerfViewPresets.xml) laden.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-155">Load [ER presets for PerfView](https://download.microsoft.com/download/2/d/0/2d037b0f-ffd1-4d65-b64f-fcdf51f2c81f/ER_PerfViewPresets.xml).</span></span>
5. <span data-ttu-id="7b8e8-156">Wählen Sie **ER** \> **Andere Voreinstellung**.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-156">Select **ER** \> **Other preset**.</span></span>
6. <span data-ttu-id="7b8e8-157">Schau dir die Namen an:</span><span class="sxs-lookup"><span data-stu-id="7b8e8-157">Look at the names:</span></span>

    - <span data-ttu-id="7b8e8-158">Sie werden wahrscheinlich den Plattformcode sehen, der die meiste Zeit verbraucht.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-158">You will probably see the platform code that consumes the most time.</span></span>
    - <span data-ttu-id="7b8e8-159">Sie können doppeltippen (oder doppelklicken) und nach oben zu **Angerufene** gehen.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-159">You can double-tap (or double-click) and go up through **callees**.</span></span>

        <span data-ttu-id="7b8e8-160">Wenn Sie Klassen mit dem Präfix „ERExpression“ finden und es sich um Funktionen handelt, die sich auf Formeln beziehen, können Sie den Funktionsnamen anhand des Klassennamens erraten und im ER-Repository nach den Attributen suchen.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-160">If you find classes that have the prefix "ERExpression," and if they are functions that are related to formulas, you can guess the function name based on the class name, and you can look at the ER repo to view the attributes.</span></span>

### <a name="fixes"></a><span data-ttu-id="7b8e8-161">Korrekturen</span><span class="sxs-lookup"><span data-stu-id="7b8e8-161">Fixes</span></span>

- <span data-ttu-id="7b8e8-162">Wenn Sie feststellen, dass die meiste CPU-Zeit von Abfragen verbraucht wird, versuchen Sie, die Anzahl der Abfragen zu reduzieren:</span><span class="sxs-lookup"><span data-stu-id="7b8e8-162">If you see that most of the CPU time is consumed by queries, try to reduce the number of queries:</span></span>

    - <span data-ttu-id="7b8e8-163">[Überprüfen Sie die ER-Spur](#analyze-database-calls) auf doppelte Abfragen.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-163">[Review the ER trace](#analyze-database-calls) for duplicated queries.</span></span>
    - <span data-ttu-id="7b8e8-164">Sehen Sie, wie viele Datensätze abgerufen werden, und bewerten Sie, wie viele Daten theoretisch abgerufen werden sollten.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-164">See how many records are fetched, and evaluate how much data should theoretically be fetched.</span></span>

- <span data-ttu-id="7b8e8-165">Wenn Sie feststellen, dass die meiste CPU-Zeit von den verwendeten Funktionen verbraucht wird, versuchen Sie, die Stelle in der Konfiguration zu finden, die die meisten Ressourcen verbraucht.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-165">If you see that most of the CPU time is consumed by the functions that are used, try to find the place in the configuration that consumes the most resources.</span></span>
- <span data-ttu-id="7b8e8-166">Wenn Sie feststellen, dass die meiste CPU-Zeit von Datenerfassungsfunktionen verbraucht wird, sollten Sie sie durch them ersetzen *SQL-Gruppe nach* auf der Modellzuordnungsseite.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-166">If you see that most of the CPU time is consumed by data collection functions, consider replacing them with *SQL group by* on the model mapping side.</span></span>

### <a name="collecting-data"></a><a name="collecting-data"></a><span data-ttu-id="7b8e8-167">Datenerfassung</span><span class="sxs-lookup"><span data-stu-id="7b8e8-167">Collecting data</span></span>

<span data-ttu-id="7b8e8-168">Abhängig von Ihrer Umgebung gibt es mehrere Möglichkeiten, verfügbare Daten zu sammeln:</span><span class="sxs-lookup"><span data-stu-id="7b8e8-168">Depending on your environment, there are several ways to collect available data:</span></span>

- <span data-ttu-id="7b8e8-169">Die Gesamtlaufzeit abrufen:</span><span class="sxs-lookup"><span data-stu-id="7b8e8-169">Get the total running time:</span></span>

    - <span data-ttu-id="7b8e8-170">Aus dem Aktionszentrum</span><span class="sxs-lookup"><span data-stu-id="7b8e8-170">From the Action center</span></span>
    - <span data-ttu-id="7b8e8-171">Aus dem Ereignisprotokoll</span><span class="sxs-lookup"><span data-stu-id="7b8e8-171">From the event log</span></span>

- <span data-ttu-id="7b8e8-172">Profil der Ausführung:</span><span class="sxs-lookup"><span data-stu-id="7b8e8-172">Profile the execution:</span></span>

    - <span data-ttu-id="7b8e8-173">Durch die Verwendung von ER-Tools</span><span class="sxs-lookup"><span data-stu-id="7b8e8-173">By using ER tools</span></span>
    - <span data-ttu-id="7b8e8-174">Mit dem Trace Parser</span><span class="sxs-lookup"><span data-stu-id="7b8e8-174">By using Trace parser</span></span>
    - <span data-ttu-id="7b8e8-175">Durch die Verwendung von PerfView</span><span class="sxs-lookup"><span data-stu-id="7b8e8-175">By using PerfView</span></span>

#### <a name="collecting-data-in-a-production-environment"></a><span data-ttu-id="7b8e8-176">Sammeln von Daten in einer Produktionsumgebung</span><span class="sxs-lookup"><span data-stu-id="7b8e8-176">Collecting data in a production environment</span></span>

<span data-ttu-id="7b8e8-177">Manchmal können Probleme nur in einer Produktionsumgebung reproduziert werden.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-177">Sometimes, issues can be reproduced only in a production environment.</span></span> <span data-ttu-id="7b8e8-178">Sie können Daten auf folgende Arten sammeln:</span><span class="sxs-lookup"><span data-stu-id="7b8e8-178">Data can be collected in the following ways:</span></span>

- <span data-ttu-id="7b8e8-179">Mit [Trace Parser](../perf-test/trace-trace-tutorial.md)-Spuren</span><span class="sxs-lookup"><span data-stu-id="7b8e8-179">By using [Trace parser](../perf-test/trace-trace-tutorial.md) traces</span></span>
- <span data-ttu-id="7b8e8-180">Durch die Nutzung von [ER-Ausführung](trace-execution-er-troubleshoot-perf.md)-Spuren</span><span class="sxs-lookup"><span data-stu-id="7b8e8-180">By using [ER execution](trace-execution-er-troubleshoot-perf.md) traces</span></span>
- <span data-ttu-id="7b8e8-181">Durch Nutzung der gesamten Ausführungszeit</span><span class="sxs-lookup"><span data-stu-id="7b8e8-181">By using the total execution time</span></span>

#### <a name="collecting-data-in-a-development-environment"></a><span data-ttu-id="7b8e8-182">Sammeln von Daten in einer Entiwcklungsumgebung</span><span class="sxs-lookup"><span data-stu-id="7b8e8-182">Collecting data in a development environment</span></span>

<span data-ttu-id="7b8e8-183">Neben den Tools, die in einer Produktionsumgebung verwendet werden können, gibt es mehrere Tools, die Sie in einer Entwicklungsumgebung verwenden können:</span><span class="sxs-lookup"><span data-stu-id="7b8e8-183">In addition to the tools that can be used in a production environment, there are several tools that you can use in a development environment:</span></span>

- <span data-ttu-id="7b8e8-184">Ereignisprotokoll (Microsoft-Dynamics-ElectronicReporting).</span><span class="sxs-lookup"><span data-stu-id="7b8e8-184">Event log (Microsoft-Dynamics-ElectronicReporting).</span></span> <span data-ttu-id="7b8e8-185">Dieses Protokoll kann Ihnen die Gesamtausführungszeit anzeigen.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-185">This log can give you the total execution time.</span></span>
- <span data-ttu-id="7b8e8-186">Gängige .NET-Tools wie PerfView.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-186">Common .NET tools, such as PerfView.</span></span>

<span data-ttu-id="7b8e8-187">Darüber hinaus bietet Ihnen eine Entwicklungsumgebung mehr Flexibilität beim Experimentieren.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-187">Additionally, a development environment gives you more flexibility to experiment.</span></span> <span data-ttu-id="7b8e8-188">Sie können beispielsweise Teile von Berichten deaktivieren, um zu sehen, wie sich dies auf die Ausführungszeit auswirkt.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-188">For example, you can turn off parts of reports to see how the execution time is affected.</span></span>

### <a name="tools"></a><a name="tools"></a><span data-ttu-id="7b8e8-189">Extras</span><span class="sxs-lookup"><span data-stu-id="7b8e8-189">Tools</span></span>

#### <a name="execution-time-in-the-action-center"></a><a name="infolog-time"></a><span data-ttu-id="7b8e8-190">Ausführungszeit im Action Center</span><span class="sxs-lookup"><span data-stu-id="7b8e8-190">Execution time in the Action center</span></span>

<span data-ttu-id="7b8e8-191">ER kann die Ausführungszeit der Konfiguration im Action Center anzeigen.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-191">ER can show the execution time of the configuration in the Action center.</span></span> <span data-ttu-id="7b8e8-192">Diese Option funktioniert nur für einen bestimmten Benutzer und ein bestimmtes Unternehmen und nur für interaktive Sitzungen.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-192">This option works only for a specific user and a specific company, and only for interactive sessions.</span></span> <span data-ttu-id="7b8e8-193">Gehen Sie folgendermaßen vor, um diese Funktion verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-193">To make this feature available, follow these steps.</span></span>

1. <span data-ttu-id="7b8e8-194">Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-194">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="7b8e8-195">Auf der Seite **Konfigurationen** im Aktivitätsbereich, auf der Registerkarte **Konfigurationen** in der Gruppe **Erweiterte Einstellungen** wählen Sie **Benutzerparameter** aus.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-195">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="7b8e8-196">Im Dialogfeld **Benutzerparameter** setzen Sie die Option **Dateierstellungszeit anzeigen** auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-196">In the **User parameters** dialog box, set the **Show file generation time** option to **Yes**.</span></span>

#### <a name="execution-time-in-the-event-log"></a><a name="event-log-time"></a><span data-ttu-id="7b8e8-197">Ausführungszeit im Ereignisprotokoll</span><span class="sxs-lookup"><span data-stu-id="7b8e8-197">Execution time in the event log</span></span>

1. <span data-ttu-id="7b8e8-198">Öffnen Sie die Windows-Ereignisanzeige.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-198">Open Windows Event Viewer.</span></span>
2. <span data-ttu-id="7b8e8-199">Öffnen Sie unter **Anwendungs- und Dienstprotokolle** die Option **Microsoft-Dynamics-ElectronicReporting/Operational**.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-199">Under **Applications and Services logs**, open **Microsoft-Dynamics-ElectronicReporting/Operational**.</span></span>
3. <span data-ttu-id="7b8e8-200">Suchen Sie nach **FormatMappingRun**-Ereignissen, bei denen **Ereignis-ID=2**, da diese Ereignisse die Informationen über die verstrichene Zeit enthalten.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-200">Look for **FormatMapingRun** events where **EventID=2**, because these events contain the information about elapsed time.</span></span>

#### <a name="trace-parser-traces"></a><a name="trace-parser"></a><span data-ttu-id="7b8e8-201">Spuren von Trace Parsern</span><span class="sxs-lookup"><span data-stu-id="7b8e8-201">Trace parser traces</span></span> 

<span data-ttu-id="7b8e8-202">Da ER in X++ implementiert ist, können Sie gängige X++-Tools verwenden, um die Leistung zu analysieren.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-202">Because ER is implemented in X++, you can use common X++ tools to analyze performance.</span></span> <span data-ttu-id="7b8e8-203">Weitere Informationen finden Sie unter [Erfassen von Spuren mit dem Trace Parser](../perf-test/trace-trace-tutorial.md).</span><span class="sxs-lookup"><span data-stu-id="7b8e8-203">For more information, see [Take traces by using Trace parser](../perf-test/trace-trace-tutorial.md).</span></span>

<span data-ttu-id="7b8e8-204">Dieser Ansatz unterliegt einigen Einschränkungen.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-204">There are a few limitations to this approach.</span></span> <span data-ttu-id="7b8e8-205">Da ein Teil von ER in C# implementiert ist, sind nicht alle Details verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-205">Because part of ER is implemented in C#, not all the details will be available.</span></span> <span data-ttu-id="7b8e8-206">Sie können jedoch die Datennutzungsdetails anzeigen.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-206">However, you can view the data usage details.</span></span> <span data-ttu-id="7b8e8-207">Darüber hinaus können lange Berichtsausführungen die Speicherbeschränkungen für Traces überschreiten.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-207">Additionally, long report runs can exceed trace storage limitations.</span></span>

#### <a name="er-traces"></a><a name="electronic-reporting-traces"></a><span data-ttu-id="7b8e8-208">ER-Spuren</span><span class="sxs-lookup"><span data-stu-id="7b8e8-208">ER traces</span></span>

<span data-ttu-id="7b8e8-209">ER kann seine eigenen Spuren sammeln und verfügt über Visualisierungs- und Analysetools für diese Spuren.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-209">ER can collect its own traces, and it has visualization and analysis tools for those traces.</span></span> <span data-ttu-id="7b8e8-210">Weitere Informationen finden Sie unter [Überwachen der Ausführung von EB-Formaten zur Behebung von Leistungsproblemen](trace-execution-er-troubleshoot-perf.md).</span><span class="sxs-lookup"><span data-stu-id="7b8e8-210">For more information, see [Trace the execution of ER formats to troubleshoot performance issues](trace-execution-er-troubleshoot-perf.md).</span></span>

#### <a name="perfview"></a><a name="perfview"></a><span data-ttu-id="7b8e8-211">PerfView</span><span class="sxs-lookup"><span data-stu-id="7b8e8-211">PerfView</span></span>

<span data-ttu-id="7b8e8-212">Da sowohl X++ als auch ER auf der .NET-Plattform implementiert sind, können Sie gängige .NET-Tools verwenden.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-212">Because both X++ and ER are implemented on top of the .NET platform, you can use common .NET tools.</span></span> <span data-ttu-id="7b8e8-213">Sie können zum Beispiel das kostenlose [PerfView](https://github.com/Microsoft/perfview)-Tool verwenden.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-213">For example, you can use the free [PerfView](https://github.com/Microsoft/perfview) tool.</span></span>

<span data-ttu-id="7b8e8-214">Sie können auch Daten über die Befehlszeile sammeln.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-214">You can also collect data from the command line.</span></span> <span data-ttu-id="7b8e8-215">Das folgende Windows PowerShell-Skript erfasst beispielsweise die Ausführungszeit, bis die Formatausführung auf dem Computer beendet wird.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-215">For example, the following Windows PowerShell script collects the execution time until any format execution is stopped on the machine.</span></span>

```powershell
c:\programs\PerfView collect "e:\traces\$(date -format "ddMMyyyy_hhmm").etl" `
    -CircularMB:20000 -ThreadTime `
    -NoNGenRundown `
    -StopOnEtwEvent:Microsoft-Dynamics-ElectronicReporting/FormatMappingRun/Stop
```

<span data-ttu-id="7b8e8-216">Dieser Ansatz unterliegt einigen Einschränkungen.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-216">There are a few limitations to this approach.</span></span> <span data-ttu-id="7b8e8-217">Sie müssen Administratorzugriff auf den Computer besitzen.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-217">You must have administrative access to the machine.</span></span> <span data-ttu-id="7b8e8-218">Darüber hinaus müssen Sie ein erfahrener Entwickler sein, da die Lernkurve steil ist.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-218">Additionally, you must be an experienced developer, because there is a steep learning curve.</span></span>

### <a name="making-changes"></a><a name="making-changes"></a><span data-ttu-id="7b8e8-219">Änderungen vornehmen</span><span class="sxs-lookup"><span data-stu-id="7b8e8-219">Making changes</span></span>

#### <a name="use-caching"></a><a name="use-caching"></a><span data-ttu-id="7b8e8-220">Caching verwenden</span><span class="sxs-lookup"><span data-stu-id="7b8e8-220">Use caching</span></span>

<span data-ttu-id="7b8e8-221">Das Caching verkürzt zwar die Zeit, die zum erneuten Abrufen von Daten erforderlich ist, kostet jedoch Speicher.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-221">Although caching reduces the amount of time that is required to fetch data again, it costs memory.</span></span> <span data-ttu-id="7b8e8-222">Verwenden Sie Caching in Fällen, in denen die Menge der abgerufenen Daten nicht sehr groß ist.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-222">Use caching in cases where the amount of fetched data isn't very large.</span></span> <span data-ttu-id="7b8e8-223">Weitere Informationen und ein Beispiel zur Verwendung von Caching finden Sie unter [Verbessern der Modellzuordnung basierend auf Informationen aus dem Ausführungsspur](trace-execution-er-troubleshoot-perf.md#improve-the-model-mapping-based-on-information-from-the-execution-trace).</span><span class="sxs-lookup"><span data-stu-id="7b8e8-223">For more information and an example that shows how to use caching, see [Improve the model mapping based on information from the execution trace](trace-execution-er-troubleshoot-perf.md#improve-the-model-mapping-based-on-information-from-the-execution-trace).</span></span>

#### <a name="use-a-cached-parameterized-calculated-field"></a><a name="cached-parameterized"></a><span data-ttu-id="7b8e8-224">Verwenden Sie ein zwischengespeichertes, parametrisiertes berechnetes Feld</span><span class="sxs-lookup"><span data-stu-id="7b8e8-224">Use a cached, parameterized calculated field</span></span>

<span data-ttu-id="7b8e8-225">Manchmal müssen Werte wiederholt nachgeschlagen werden.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-225">Sometimes, values must be looked up repeatedly.</span></span> <span data-ttu-id="7b8e8-226">Beispiele sind Kontonamen und Kontonummern.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-226">Examples include account names and account numbers.</span></span> <span data-ttu-id="7b8e8-227">Um Zeit zu sparen, können Sie ein berechnetes Feld mit Parametern auf der obersten Ebene erstellen und das Feld dann zum Cache hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-227">To help save time, you can create a calculated field that has parameters on the top level, and then add the field to the cache.</span></span>

<span data-ttu-id="7b8e8-228">Es wird empfohlen, diesen Ansatz nur zu verwenden, wenn die Größe der zwischengespeicherten Daten gering ist.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-228">We recommend that you use this approach only when the size of the cached data is small.</span></span> <span data-ttu-id="7b8e8-229">Weitere Informationen finden Sie unter [Verbessern der Leistung von ER-Lösungen durch Hinzufügen parametrisierter CALCULATED FIELD-Datenquellen](er-calculated-field-ds-performance.md).</span><span class="sxs-lookup"><span data-stu-id="7b8e8-229">For more information, see [Improve the performance of ER solutions by adding parameterized CALCULATED FIELD data sources](er-calculated-field-ds-performance.md).</span></span>

#### <a name="use-a-join-data-source"></a><a name="use-join-datasource"></a><span data-ttu-id="7b8e8-230">JOIN-Datenquelle verwenden</span><span class="sxs-lookup"><span data-stu-id="7b8e8-230">Use a JOIN data source</span></span>

<span data-ttu-id="7b8e8-231">Eine **JOIN**-Datenquelle ermöglicht das Abrufen mehrerer verbundener Datensätze mit einer Abfrage.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-231">A **JOIN** data source enables several connected records to be fetched by one query.</span></span> <span data-ttu-id="7b8e8-232">Es muss nicht eine separate Abfrage verwendet werden, um jeden verbundenen Datensatz abzurufen.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-232">A separate query doesn't have to be used to fetch each connected record.</span></span> <span data-ttu-id="7b8e8-233">Wenn Sie beispielsweise 1.000 Zeilen haben und Artikeldaten für jede Zeile nach Relation abrufen, haben Sie 1.001 Abfragen (= 1.000 + 1).</span><span class="sxs-lookup"><span data-stu-id="7b8e8-233">For example, if you have 1,000 lines, and you fetch item data for each line by relation, you will have 1,001 queries (= 1,000 + 1).</span></span> <span data-ttu-id="7b8e8-234">Wenn Sie eine **JOIN**-Datenquelle verwenden, verwenden Sie nur eine Abfrage, um dieselben Daten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-234">If you use a **JOIN** data source, you will use only one query to fetch the same data.</span></span> <span data-ttu-id="7b8e8-235">Weitere Informationen finden Sie unter [JOIN-Datenquellenzuordnungen verwenden, um Daten aus mehreren Anwendungstabellen abzurufen](er-join-data-sources.md).</span><span class="sxs-lookup"><span data-stu-id="7b8e8-235">For more information, see [Use JOIN data sources in ER model mappings to get data from multiple application tables](er-join-data-sources.md).</span></span>

#### <a name="use-the-filter-function-instead-of-the-where-function"></a><a name="filter"></a><span data-ttu-id="7b8e8-236">Verwenden Sie die FILTER-Funktion anstelle der WHERE-Funktion</span><span class="sxs-lookup"><span data-stu-id="7b8e8-236">Use the FILTER function instead of the WHERE function</span></span>

<span data-ttu-id="7b8e8-237">Die **[FILTER](er-functions-list-filter.md)**-Funktion führt Bedingungen auf SQL Server aus, während die **WHERE**-Funktion alle Daten aus der Liste abruft, einen Datensatz nach dem anderen, und die Bedingung für jeden Datensatz anwendet.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-237">The **[FILTER](er-functions-list-filter.md)** function runs conditions on SQL Server, whereas the **WHERE** function fetches all data from the list, one record at a time, and applies the condition for each record.</span></span> <span data-ttu-id="7b8e8-238">Sie möchten beispielsweise einen Datensatz aus 1.000 Datensätzen auswählen.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-238">For example, you want to select one record out of 1,000 records.</span></span> <span data-ttu-id="7b8e8-239">Wenn Sie **WHERE** verwenden, werden alle 1.000 Datensätze abgerufen.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-239">If you use **WHERE**, all 1,000 records will be fetched.</span></span> <span data-ttu-id="7b8e8-240">Wenn Sie jedoch **FILTER** verwenden, wird genau ein Datensatz geholt.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-240">However, if you use **FILTER**, exactly one record will be fetched.</span></span> <span data-ttu-id="7b8e8-241">**FILTER** kann auch datenbankseitig Indizes verwenden.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-241">**FILTER** can also use indexes on the database side.</span></span>

#### <a name="using-collected-data-functions-or-an-accumulated-data-data-source"></a><a name="collected-data"></a><span data-ttu-id="7b8e8-242">Verwenden von Funktionen für gesammelte Daten oder einer Datenquelle für gesammelte Daten</span><span class="sxs-lookup"><span data-stu-id="7b8e8-242">Using collected data functions or an accumulated data data source</span></span>

<span data-ttu-id="7b8e8-243">Wenn Ihre Konfiguration ein *gruppiere nach*-Komponente hat, die zuvor abgerufene Daten nach Bericht zusammenfasst, ruft die Komponente alle Daten erneut ab.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-243">If your configuration has a *group by* component that summarizes previously fetched data by report, the component will fetch all the data again.</span></span> <span data-ttu-id="7b8e8-244">Durch die Verwendung von Funktionen für gesammelte Daten ermöglichen Sie ER, Daten während des ersten Abrufs zu sammeln.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-244">By using collected data functions, you enable ER to accumulate data during the first fetch.</span></span> <span data-ttu-id="7b8e8-245">Weitere Informationen finden Sie unter [Konfigurieren des ER-Formats für Inventuren und Summierungen](tasks/er-format-counting-summing-2.md).</span><span class="sxs-lookup"><span data-stu-id="7b8e8-245">For more information, see [ER Configure format to do counting and summing](tasks/er-format-counting-summing-2.md).</span></span>

#### <a name="rewrite-parts-of-the-configuration-in-x"></a><span data-ttu-id="7b8e8-246">Teile der Konfiguration in X++ umschreiben</span><span class="sxs-lookup"><span data-stu-id="7b8e8-246">Rewrite parts of the configuration in X++</span></span>

<span data-ttu-id="7b8e8-247">ER unterstützt Aufrufmethoden von Tabellen und Klassen, einschließlich Erweiterungen.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-247">ER supports calling methods of tables and classes, including extensions.</span></span> <span data-ttu-id="7b8e8-248">Ziehen Sie in Betracht, Teile der Modellzuordnung in X++ umzuschreiben, um die Leistung zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-248">Consider rewriting parts of the model mapping in X++ to help improve performance.</span></span>

<span data-ttu-id="7b8e8-249">ER kann Daten aus den folgenden Quellen verbrauchen:</span><span class="sxs-lookup"><span data-stu-id="7b8e8-249">ER can consume data from the following sources:</span></span>

- <span data-ttu-id="7b8e8-250">Klassen (Datenquellen **Objekt** und **Klasse**)</span><span class="sxs-lookup"><span data-stu-id="7b8e8-250">Classes (**object** and **class** data sources)</span></span>
- <span data-ttu-id="7b8e8-251">Tabellen (Datenquellen **Tabelle** und **Tabellendatensätze** Datenquellen)</span><span class="sxs-lookup"><span data-stu-id="7b8e8-251">Tables (**table** and **table records** data sources)</span></span>

<span data-ttu-id="7b8e8-252">Das [ER-API](er-apis-app73.md#how-to-access-internal-x-objects-by-using-erobjectsfactory) bietet auch eine Möglichkeit, vorberechnete Daten aus dem aufrufenden Code zu senden.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-252">The [ER API](er-apis-app73.md#how-to-access-internal-x-objects-by-using-erobjectsfactory) also provides a way to send precalculated data from the calling code.</span></span> <span data-ttu-id="7b8e8-253">Die Anwendungssuite enthält zahlreiche Beispiele für diesen Ansatz.</span><span class="sxs-lookup"><span data-stu-id="7b8e8-253">The application suite contains numerous examples of this approach.</span></span>
