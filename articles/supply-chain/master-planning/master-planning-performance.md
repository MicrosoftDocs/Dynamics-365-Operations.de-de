---
title: Produktprogrammplanung optimieren
description: In diesem Artikel werden die verschiedenen Optionen beschrieben, die Ihnen helfen können, die Leistung der Produktprogrammplanung zu verbessern und Probleme zu beheben.
author: t-benebo
ms.date: 12/18/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-05-31
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: b2c4b7e2197d312d22f9851121a9e6d4d4d03ba3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8897602"
---
# <a name="improve-master-planning-performance"></a>Produktprogrammplanung optimieren

[!include [banner](../includes/banner.md)]

In diesem Artikel werden die verschiedenen Optionen beschrieben, die Ihnen helfen können, die Leistung der Produktprogrammplanung zu verbessern und Probleme zu beheben. Er umfasst Informationen zu Parametern und Einstellungen sowie empfohlene Konfigurationen und Aktivitäten. Er enthält außerdem eine Zusammenfassung aller wichtigen Parameter, die Sie berücksichtigen sollten, wenn Sie langfristige Produktprogrammplanungsaufträge haben.

Dieser Artikel ist für Systemadministratoren oder IT-Benutzer vorgesehen, die Fehlerbehebungen durchführen können. Es ist außerdem für Produktions- oder Beschaffungsplaner vorgesehen, da es Informationen zu Parametern enthält, die den Unternehmensplanungsanforderungen zugeordnet werden. 

## <a name="parameters-related-to-master-planning-performance"></a>Parameter, die der Produktprogrammplanungsleistung zugeordnet sind

Verschiedene Parameter betreffen die Laufzeit der Produktprogrammplanung und sollten berücksichtigt werden.

### <a name="number-of-threads"></a>Anzahl der Threads

Mit dem Parameter **Anzahl der Threads** können Sie die Produktprogrammplanung anpassen, um die Leistung beim bestimmten Datensatz zu verbessern. Dieser Parameter gibt die Gesamtanzahl der Threads an, die verwendet werden, um die Produktprogrammplanung ausführen. Er verursacht eine Umwandlung der Produktprogrammplanungsausführung, die bei der Verringerung der Ausführungszeit hilft. 

Sie können den Parameter **Number of threads** im Dialogfeld **Produktprogrammplanungslauf** festlegen. Zum Öffnen dieses Dialogfelds, wechseln Sie zu **Produktprogrammplanung \> Produktprogrammplanung \> Ausführen \> Produktprogrammplanung** oder wählen Sie **Ausführen** im Arbeitsbereich **Produktprogrammplanung** aus. Um den besten Wert für diesen Parameter zu bestimmen, müssen Sie mehrere Versuche durchführen. Sie können jedoch die folgenden Formeln verwenden, um einen Ausgangswert zu berechnen:

- **Bei der Fertigungsbranche:** (Anzahl der Threads) = (Anzahl der geplanten Bestellungen ÷ 1.000)
- **Andernfalls:** (Anzahl der Threads) = (Anzahl der Artikel ÷ 1.000)

Die Anzahl der Hilfsprogramme, die während der Produktprogrammplanung verwendet werden, muss kleiner oder gleich der maximalen Anzahl der Threads sein, die auf dem Chargenserver zulässig sind. Wenn die Anzahl der Hilfsprogramme überschreitet die Anzahl der Threads auf dem Chargenserver, die zusätzlichen Threads erledigen keine Arbeit.

> [!NOTE]
> Bei der Einstellung von **0** (Null) für den Parameter **Anzahl der Threads** wird die Laufzeit der Produktprogrammplanung erhöht. Daher wird empfohlen, dass Sie immer einen Wert größer als 0 festlegen.

### <a name="number-of-tasks-in-helper-task-bundle"></a>Anzahl der Aufgaben im Hilfsaufgabenbündel

Durch Änderung der Einstellung **Anzahl der Aufgaben im Aufgabenbündel** (das heißt, die Bündelgröße), können Sie möglicherweise die Ausführungszeit verringern. Diese Einstellung steuert die Anzahl der Elemente, die durch ein einzelnes Hilfsprogramm zusammen geplant werden.

Sie können den Parameter **Aznahl der Aufgaben im Aufgabenbündel** im Abschnitt **Leistung** auf der Registerkarte **Allgemein** der Seite **Parameter für Produktprogrammplanung** (**Produktprogrammplanung \> Einstellungen \>-Parameter für Produktprogrammplanung**) festlegen. Der beste Wert für diesen Parameter hängt von Ihren Daten ab. Daher wird empfohlen, dass Sie mit dem Wert **1** beginnen und dann durch Versuche den besten Wert für diese Einstellung bestimmen.

Im Allgemeinen wird empfohlen, dass Sie die Anzahl der Aufgaben erhöhen, wenn die Anzahl der Elemente sehr groß ist (bei mehreren Hunderttausenden). Andernfalls sollten Sie die Anzahl der Aufgaben verringern. Bei folgenden speziellen Branchen sollten Sie die folgenden Empfehlungen berücksichtigen:

- In den Einzelhandel- und Verteilungsbranchen, in denen viele unabhängige Elemente vorhanden sind, verwenden Sie viele Hilfsprogramme, da es hier keine Abhängigkeit zwischen Elementen gibt. 
- In der Fertigungsindustrie bei denen es zahlreiche Stücklisten (BOMs) und freigegebene Unterkomponenten gibt, verwenden Sie weniger Hilfsprogramme, da die Abhängigkeiten zwischen Elementen zu Wartezeiten führen können.

> [!TIP]
> Bei Leistungsproblemen wird empfohlen, dass Sie die Einstellung **Anzahl der Hilfsprogramme im Aufgabenbündel** auf **1** reduzieren. Sie können dann die Versuchsreihe starten, um den besten Wert für diese Einstellungen zu finden. Im Allgemeinen treten Leistungsprobleme auf, wenn die Verarbeitung eines Elements länger dauert, als die der verbleibenden Elemente. In diesem Fall dauert die Ausführung von zwei folgenden Elementen mit dem Status **Disposition** im Produktprogrammplanungslauf deutlich unterschiedlich lange. In Extremfällen kann diese Differenz bis zu 30 Minuten betragen. Sie können die Zeit, die die Ausführung einer Aufgabe benötigt, ableiten, indem Sie die Dauer der einzelnen Aufgaben betrachten.

### <a name="use-of-cache"></a>Cachverwendung

Mit dem **Cachverwendung**-Parameter können Sie die Produktprogrammplanung anpassen, um die Leistung beim bestimmten Datensatz zu verbessern. Beispielsweise können Sie ihn anpassen, um die folgenden Ergebnisse zu erzielen:

- Bei mehr Zwischenspeicherung werden im Datenspeicher mehr Daten gesammelt. Die Erwartung ist, dass die Daten später erneut verwendet werden. Wenn sich die Daten im Arbeitsspeicher befinden, speichern Sie möglicherweise einige Datenbankanforderungen. Bei mehr Zwischenspeicherung allerdings vergrößern sich die Arbeitsspeicheranforderungen.
- Bei weniger Zwischenspeicherung müssen die gleichen Daten möglicherweise häufiger aus der Datenbank abgerufen werden. Darüber hinaus speichert Application Object Server (AOS) während des Prozesses weniger Daten im Arbeitsspeicher.

Es ist schwer vorherzusagen welcher Option besser ist, da jeder Fall nicht nur von den Daten, sondern auch von der Hardware abhängt. Da weniger Zwischenspeicherung beispielsweise weniger Last auf dem Datenbankserver bedeutet, sollte diese Option wahrscheinlich nicht verwendet werden, wenn Ihr Datenbankserver bereits überlastet ist.

Sie können den Parameter **Cacheverwendung** im Abschnitt **Leistung** auf der Registerkarte **Allgemein** der Seite **Parameter für Produktprogrammplanung** (**Produktprogrammplanung \> Einstellungen \>-Parameter für Produktprogrammplanung**) festlegen. Die Effizienz der Zwischenspeicherung hängt deutlich von den Kundendaten ab. Wenn die zwischengespeicherten Daten beispielsweise niemals benötigt werden, verschwenden Sie nur Speicherplatz, wenn Sie Daten bis zum Ende des Planungsprozesses speichern. Wenn Sie in diesem Fall weniger Zwischenspeicherung konfigurieren, kann dies die Leistung möglicherweise erhöhen, da AOS weniger Arbeitsspeicher erfordert und Serverressourcen für andere Aufgaben freigegeben werden.

> [!TIP]
> Im Allgemeinen sollten Sie den Parameter **Cachverwendung** auf **Maximum** festlegen, da der Parameter als eine Leistungsverbesserungsfunktion gedacht ist. Es wird empfohlen, dass Sie den Parameter auf **Minimum** festlegen, wenn Sie lokal ausführen und nur eingeschränkter Speicher (ungeführ 2 Gigabytes \[GB\]) verfügbar ist.

### <a name="number-of-orders-in-firming-bundle"></a>Zahl der Produktionsaufträge im Anlagebündel

Der Parameter **Zahl der Produktionsaufträge im Anlagebündel** gibt die Gesamtanzahl der Aufträge an, die jeweils von jedem Thread/jeder Charge ausgeführt werden. Es bewirkt eine Parallelisierung der automatischen Umwandlung.

Sie können den Parameter **Zahl der Produktionsaufträge im Anlagebündel** im Abschnitt **Leistung** auf der Registerkarte **Allgemein** der Seite **Parameter für Produktprogrammplanung** (**Produktprogrammplanung \> Einstellungen \>-Parameter für Produktprogrammplanung**) festlegen. Die Parallelisierung der automatischen Umwandlung basiert auf den Aufträgen, die zusammen verarbeitet werden müssen. Wenn der Parameter beispielsweise auf **50** festgelegt wird, nimmt jeder Thread oder Batchauftrag 50 Aufträge auf einmal an und verarbeitet diese zusammen. Es wird empfohlen, einen den besten Wert mithilfe einer Versuchsreihe zu bestimmen. Sie können jedoch die folgende Formel verwenden, um einen Ausgangswert zu berechnen:

(Anzahl der Aufträge pro Bündel) = (Anzahl der Bedarfsartikel ÷ Anzahl der Threads)

> [!NOTE]
> Wenn Sie den Parameter **Anzahl der Aufträge im bündeln** auf **0** (Null) festlegen, findet keine Parallelisierung der automatischen Umwandlung statt. Der ganze Prozess wird in einem einzelnen Chargenauftrag ausgeführt und hat eine kumulative Ausführungszeit. Daher steigt die Ausführungszeit der Produktprogrammplanung. Aus diesem Grund sollten Sie diesen Parameter auf einen Wert über **0** (Null) festlegen.

### <a name="time-fences"></a>Planungszeiträume

Planungszeiträume geben an, wie weit Berechnungen und andere Voraussetzungen in der Zukunft liegen müssen, um von der Produktprogrammplanung berechnet zu werden. Je größer der Planungszeitraum ist, desto länger dauert die Ausführung der Produktprogrammplanung. Richten Sie die Planungszeiträume daher gemäß der Geschäftsanforderungen ein. Weitere Informationen über Planungszeiträume finden Sie unter [Einrichten der Produktprogrammplanung](master-planning-setup.md).

### <a name="actions"></a>Aktionen

Unter den Planungszeiträumen können Sie auch den Parameter **Aktivitätsmeldung** finden. Die Berechnung der Aktivitätsmeldungen bewirkt eine längere Laufzeit der Produktprogrammplanung. Wenn Aktivitätsmeldungen nicht regelmäßig analysiert und angewendet werden (täglich, wöchentlich, usw.), sollten Sie die Berechnung beim Produktprogrammplanungslauf deaktivieren. Um die Berechnung auszuschalten, legen Sie auf der Seite **Produktprogrammplanung** (**Produktprogrammplanung \> Einstellungen \> Pläne \> Produktprogrammplan**) den Planungszeitraum **Aktionsnachricht** auf **0** (null) fest. Überprüfen Sie außerdem, dass die Einstellung **Aktivitätsmeldung** für alle Dispositionssteuerungsgruppen deaktiviert ist.

### <a name="futures"></a>Verfügbarkeit

Die Berechnung der Verfügbarkeiten bewirkt eine längere Laufzeit der Produktprogrammplanung. Wenn Sie keine Stücklisten planen oder wenn Verzögerungen bei der Planung nicht von der Lieferung zum Bedarf weitergeleitet werden müssen, sollten Sie die Verfügbarkeitsberechnung bei der Produktprogrammplanung ausschalten. Um die Berechnungen auszuschalten, legen Sie den Planungszeitraum **Verfügbarkeit** für den Produktprogrammplan, den Sie ausführen, auf **0** (Null) fest. Überprüfen Sie außerdem, dass die Einstellung **Verfügbarkeit** für alle Dispositionssteuerungsgruppen deaktiviert ist.

## <a name="one-heavy-routine-at-a-time"></a>Eine wichtige Routine gleichzeitig

Bei der Planung von Produktprogrammplanung, planen Sie keinen anderen Batchauftrag gleichzeitig. Geben Sie vor allem darauf acht, gleichzeitig keine anderen wichtigen Routinen, wie ein Bestandabschluss, zu planen.

## <a name="review-the-session-log"></a>Sitzungsprotokoll überprüfen

Das System kann zusätzliche Informationen zu den Aufgaben sammeln, die während der Produktprogrammplanung ausgeführt werden. Damit das System diese Informationen sammelt, schalten Sie die Einstellungen **Verarbeitungszeit nachverfolgen** im Dialogfeld **Produktprogrammplanungslauf** ein. Die Informationen, die erfasst werden, helfen Ihnen bei der Suche nach Engpässen bei der Ausführung. Wenn zum Beispiel der Parameter **Anzahl der Aufgaben im Hilfsaufgabenbündel** auf **1** festgelegt wird, können Sie das Element bestimmen, das die längste Laufzeit hat. Sie können auch die für die verschiedenen Laufzeiten für die verschiedenen Threads vergleichen, die den Status **Disposition** besitzen und die Dauer für jede Aufgabe vergleichen.

Zur Überprüfung der Produktprogrammplanungläufe Ihres Systems führen Sie einen dieser Schritte aus.

- Wählen Sie im Arbeitsbereich **Produktprogrammplanung** einen Produktprogrammplan im Feld Drop-Down-Feld aus und wählen Sie dann auf der Kachel **Produktprogrammplanung** die Option **Verlauf** aus. Wählen Sie eine Stelle aus, wählen Sie auf dem Inforegister **Abfragen** aus, und wählen Sie dann **Prozessaufgabendauer** aus.
- Wählen Sie auf der Seite **Produktprogrammpläne** im linken Bereich einen Plan aus, und wählen Sie dann auf dem Inforegister **Verlauf** aus. Wählen Sie eine Stelle aus, wählen Sie auf dem Inforegister **Abfragen** aus, und wählen Sie dann **Prozessaufgabendauer** aus.

Wenn Sie das Sitzungsprotokoll prüfen, beachten Sie die folgenden Punkte:

- **Aktualisieren** sollte nicht lange Dauern (allgemein sollte es 30 Minuten in Anspruch nehmen.) Es ist allerdings Singlethread.
- **Plan kopieren** sollte eine lange dauern (es dauert ungefähr eine Minute).
- **Automatische Umwandlung** dauert normalerweise ungefähr 30 Minuten. Es kann jedoch bis zu mehrere Stunden dauern, abhängig von der Anzahl der Aufträge und der Komplexität der Elemente.
- **Automatische Umwandlung** sollte weniger Zeit als **Disposition** in Anspruch nehmen.
- **Disposition** sollte im Vergleich mit dem Rest am längsten dauern.
- **Aktivität** und **zukünftige Meldungen** können lange dauern, abhängig von den Daten und der Anzahl der Stücklisten.

## <a name="filtering-of-items"></a>Das Filtern von Elementen

Filter, die im Dialogfeld **Produktprogrammplanungslauf** ausgeführt werden, beeinflussen die Dauer des Produktprogrammplanungslaufs. Wechseln Sie zu **Produktprogrammplanung \> Produktprogrammplanung \> Ausführen \> Produktprogrammplanung** oder wählen Sie **Ausführen** im Arbeitsbereich **Produktprogrammplanung** aus. Um Elemente von der Ausführung auszuschließen, wird empfohlen, dass Sie nach Lebenszykluszustand des Elements filtern (nicht nach Artikelnummern). Wenn Sie nach Lebenszykluszustand filtern, nimmt der Aktualisierungsvorgang weniger Zeit in Anspruch als bei der Filterung nach Artikelnummern.

## <a name="automatically-filter-by-items-with-direct-demand"></a>Automatisch nach Artikeln mit direktem Bedarf filtern

Um die Laufzeit der Produktprogrammplanung zu verbessern, können Sie nur Artikel mit direktem Bedarf einbeziehen. Dieser Filter kann nur für einen vollständigen Produktprogrammplanungslauf verwendet werden, ohne dass andere Filter im Feld **Einzuschließende Datensätze** angewendet werden. Ein Produktprogrammplanungslauf, der mit Filtern ausgeführt wird, ignoriert die Einstellung **Automatisch nach Artikeln mit direktem Bedarf filtern**.

Das Feld **Automatisch nach Artikeln mit direktem Bedarf filtern** befindet sich auf der Seite **Parameter für Produktprogrammplanung** und kann mit Einstellungen zur Vor- und Nachverarbeitung verwendet werden.

### <a name="pre-processing"></a>Vorverarbeitung
Der Parameter **Vorverarbeitung: Automatisch nach Artikeln mit direktem Bedarf filtern** stellt sicher, dass die Vorbearbeitungsphase des Produktplans nur Elemente enthält, die mindestens eine der folgenden Bedingungen erfüllt:
  - Der Artikel hat einen erwarteten Eingang oder eine erwartete Ausgabe, z. B. eine Bestellung, einen Kundenauftrag, ein Angebot, einen Überweisungsauftrag oder einen Fertigungsauftrag. 
  - Der Artikel verfügt über eine Artikeldeckung mit Sicherheitsbestand (Mindestbestand).
  - Für den Artikel besteht ein prognostizierter Bedarf nach dem heutigen Tag.
  - Für den Artikel besteht eine prognostizierte Beschaffung nach dem heutigen Tag.
  - Das Element enthält alle noch zu erstellenden Durchgangsleitungen aus dem Callcenter-Modul.

> [!NOTE]
> Bei einem Artikel, der physisch verfügbar ist, wird keine Anforderungstransaktion angezeigt, da für den Artikel keine Nachfrage besteht.

### <a name="post-processing"></a>Nachbearbeitung
Die Option **Nachbearbeitung: Automatisch nach Artikeln mit direktem Bedarf filtern** ist nur relevant, wenn Sie **Stücklistenversionsverwendung** in Ihrer Deckungsgruppe festlegen. Andernfalls müssen Sie den Parameter nicht aktivieren. 

Bevor der Deckungsschritt beginnt, gibt es einen Vorerfassungsschritt, in dem Elemente mit der aktivierten Deckungseinstellung **Stücklistenversionsverwendung** erneut verarbeitet werden. Dadurch wird sichergestellt, dass Artikel aus der erforderlichen Stücklistenversion geplant werden. Artikel, bei denen während der Vorverarbeitung ein Bedarf besteht, haben keinen Bedarf mehr und sollten daher vom Planungslauf ausgeschlossen werden.

## <a name="performance-checklist-summary"></a>Zusammenfassung der Leistungscheckliste

- **Anzahl der Threads** – Auf einen Wert über **0** (Null) festlegen.
- **Anzahl der Aufgaben im Hilfsaufgabenbündel** – Auf einen Wert über **0** (Null) festlegen. (Die Formeln verwenden, die weiter oben in diesem Artikel angegeben wurden.)
- **Cachverwendung** – Auf **Maximum** festlegen, es sei denn, der Arbeitsspeicher Ihres Systems ist gering.
- **Zahl der Produktionsaufträge im Anlagebündel** – Auf einen Wert über **0** (Null) festlegen. (Die Formel verwenden, die weiter oben in diesem Artikel angegeben wurde.)
- **Planungszeiträume** – Auf Ihre Geschäftstätigkeit anpassen.
- **Aktivitäten und Verfügbarkeit** – Aktivitäten und Verfügbarkeiten deaktivieren, wenn Sie sie nicht verwenden.
- **Eine wichtige Routine gleichzeitig** – Keine Produktprogrammplanung zusammen mit einer anderen wichtigen Routine ausführen.
- **Sitzungsprotokoll überprüfen.**
- **Filtern von Artikeln** – Verwenden Sie den Lebenszykluszustand, um Artikel aus dem Produktprogrammplanungslauf auszuschließen. (Nicht die Artikelnummern verwenden).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]