---
title: Feinterminierung
description: "Dieser Artikel enthält Informationen zur Einzelvorgangsterminierung, die ein ausführlicheres Formular der Planung der Grobterminierung ist. Sie können die Feinterminierung verwenden, um Einzelvorgänge oder Bestellungen zu planen und die Fertigungsumgebung zu steuern."
author: ChristianRytt
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdSchedule
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19431
ms.assetid: aef37341-91d8-4263-80eb-35d9584be156
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 53923db7cbd3b74c1d1db72f51076640815c7df4
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---

# <a name="job-scheduling"></a>Feinterminierung

[!include[banner](../includes/banner.md)]


Dieser Artikel enthält Informationen zur Einzelvorgangsterminierung, die ein ausführlicheres Formular der Planung der Grobterminierung ist. Sie können die Feinterminierung verwenden, um Einzelvorgänge oder Bestellungen zu planen und die Fertigungsumgebung zu steuern.

Sie können die Feinterminierung verwenden, um Einzelvorgänge oder Bestellungen zu planen und die Fertigungsumgebung zu steuern. Bei der Feinterminierung werden die einzelnen Arbeitsgänge in individuelle Einzelaufgaben oder ‑vorgänge aufgeteilt. Diese Einzelvorgänge werden dann den betrieblichen Ressourcen zugewiesen, die sie ausführen. Die Feinterminierung ermöglicht Ihnen zudem, alle Einzelvorgänge zu synchronisieren, auf die beim ausgewählten Einzelvorgang verwiesen wird. Sie können ein Startdatum sowie eine Startuhrzeit oder ein Enddatum und eine Enduhrzeit für den Einzelvorgang angeben und führen dann die Planung aus. Abhängig von der Planungsrichtung, kann der Start- oder Endzeitpunkt angegeben werden. Diese Funktion ist beispielsweise hilfreich, wenn ein Einzelvorgang nicht auf mehreren Maschinen gleichzeitig ausgeführt werden kann, oder wenn Sie den Einzelvorgang optimieren möchten, der für jede Ressource ausgeführt wird.

## <a name="tasks-in-the-job-scheduling-process"></a>Aufgaben in der Feinterminierung
Der Feinterminierung umfasst die folgenden Aufgaben:

-   Teilen Sie die Arbeitsgänge in Einzelvorgänge auf.
-   Planen Sie Einzelvorgänge, basierend auf den Datums- und Uhrzeitangaben für die Ressourcen, die für den zugehörigen Arbeitsgang angegeben werden.
-   Berechnen Sie Start- und Endzeiten für jeden Einzelvorgang. Sie können die Kapazität begrenzen, um sicherzustellen, dass sich die Zeiten nicht überlappen.
-   Bestimmen Sie, auf welchen Ressourcen in der Ressourcengruppe der Einzelvorgang ausgeführt werden soll. Diese Aufgabe erfordert, dass eine Ressourcengruppe für einen Arbeitsgang angegeben wurde. Bei der Feinterminierung werden die Ressourcen oder Ressourcengruppen anhand der kürzesten Vorlaufzeit ausgewählt und auch alle vorherigen Reservierungen für die Ressourcen berücksichtigt.
-   Lösen Sie Arbeitsgänge in Einzelvorgänge auf, wenn Sie die Feinterminierung ausführen. Die Einzelvorgänge werden nach Datum und Uhrzeit entsprechend der Reihenfolge terminiert, die durch den Produktionsarbeitsplan vorgegeben ist. Die Einrichtung des Arbeitsgangs bestimmt, welche Einzelvorgänge während des Planungsvorgangs aufgelöst werden. Die Arbeitsgangsteuerungsgruppe, die dem Arbeitsgang zugewiesen ist, steuert, ob Einzelvorgänge generiert werden. Ein Einzelvorgang wird nur erzeugt, wenn er eine bestimmte Dauer aufweist. Zum Beispiel wird ein Transportzeit-Einzelvorgang erzeugt, wenn für den ausgewählten Arbeitsgang eine Transportzeit angegeben wurde.

## <a name="scheduling-direction"></a>Planungsrichtung
Sie können die Einzelvorgänge vorwärts oder rückwärts planen.

-   **Vorwärts** - Verwenden Sie die Vorwärtsterminierung, um die Produktion so früh wie möglich zu starten. Diese Methode wird auch als Schubmethode bezeichnet, da die Produktion schnellstmöglich durch den Produktionsprozess geschleust wird. Die Produktion wird so geplant, dass sie zu den frühest möglichen Daten gestartet und beendet wird.
-   **Vorwärts** - Verwenden Sie die Rückwärtsterminierung, um die Produktion so spät wie möglich zu starten. Dies ist auch als Zugmethode bezeichnet, da sie auf dem Datum basiert, zu dem die Produktion abgeschlossen sein muss. Bei der Rückwärtsplanung wird rückwärts bis zum spätesten möglichen Datum gezählt, an dem die Produktion beginnen kann, ohne die gesetzte Frist zu gefährden.

## <a name="finite-capacity"></a>Begrenzte Kapazität
Sie können bei der Planung von Einzelvorgängen die Kapazitäten begrenzen. Wenn Sie die Kapazität begrenzen, kann die Kapazität, die geplant ist, nicht größer als die Kapazität sein, die für die Ressource verfügbar ist. Die verfügbare Zeit wird als Intervall definiert, in dem die Ressource verfügbar ist und keine anderen Reservierungen für die Kapazität vorhanden sind. Bei Planungen, die auf einer begrenzten Kapazität basieren, wird sichergestellt, dass sich die Start- und Endzeit für einen Arbeitsgang an einem bestimmten Datum nicht überschneiden. Die Ressourcenkapazität, die bereits reserviert ist, wird berücksichtigt, und Überschneidungen zwischen diesen Start- und Endzeiten werden ebenfalls berücksichtigt. Die begrenzte Kapazität bestimmt die Kapazität, der für eine Ressource verfügbar sein muss, um die optimale Verwendung dieser Ressource zu erreichen. Diese Bestimmung wird gegen eine Berechnung der kürzesten Durchlaufzeit zwischen Arbeitsgängen ausgeglichen.

## <a name="finite-materials"></a>Begrenztes Material
Bei einer Feinterminierung, die auf begrenztem Material basiert, wird sichergestellt, dass die erforderlichen Materialien verfügbar sind, wenn der Arbeitsgang beginnt. Die Dispositionsregeln für Artikel definieren diese Grenzwerte. Die Planung erfordert eine Bedarfsaufschlüsselung, um festzustellen, wann die Komponenten verfügbar sind. Wird die Planung ohne begrenztes Material vorgenommen, wird bei der Planung davon ausgegangen, dass alle Artikel verfügbar sind, wenn sie benötigt werden.

## <a name="finite-properties"></a>Begrenzte Eigenschaften
Zur Verwendung begrenzter Eigenschaften bei der Feinterminierung müssen diese Eigenschaften zunächst für die Arbeitsgänge des Produktionsarbeitsplans angegeben werden. Diese Eigenschaften müssen erfüllt sein, damit Kapazitäten reserviert werden können.

## <a name="references"></a>Referenzen
Bei der Feinterminierung werden sämtliche Produktionen, auf die die aktuelle Produktion verweist, mitgeplant. Bei Produktionen mit Unterproduktionen sollten die Unterproduktionen gleichzeitig mit der Hauptproduktion geplant werden, da die Hauptproduktion erst gestartet werden kann, wenn die zugehörigen Unterproduktionen abgeschlossen sind.

## <a name="schedule-resources"></a>Ressourcen planen
Vom Planungsmodul werden Ressourcenkombinationen untersucht, um diejenigen zu ermitteln, welche die Anforderungen erfüllen können. Sie können Auswahlkriterien angeben, indem Sie im Feld **Hauptressourcenauswahl** auf der Seite **Planungsparameter** einen der folgenden Werte auswählen:

-   **Dauer** – Vom Planungsmodul wird die Ressource mit der kürzesten Vorlaufzeit ausgewählt. **Hinweis:** Die Planung nach Dauer kann zu einer Beeinträchtigung der Leistung führen, wenn die gleiche Ressourcengruppe viele Ressourcen enthält und sekundäre Arbeitsgänge verwendet werden. Pro Arbeitsgang können maximal 32 Ressourcen geplant werden. Wird diese Menge überschritten, wird eine Infolog-Meldung angezeigt, und die Feinterminierung findet nicht die beste Ausweichressource.
-   **Priorität** – Wenn mehrere Ressourcen die gleichen Funktionen und Ebenen besitzen, wird vom Planungsmodul die Ressource mit der höchsten Priorität (also mit dem niedrigsten numerischen Wert) ausgewählt. Die Ressource, die den niedrigsten numerischen Wert in diesem Feld hat, hat die höchste Priorität.

Wenn die Feinterminierung ausgeführt wird, plant das System die Ressourcen basierend auf den Einschränkungen, die in den Ressourcenparametern definiert worden sind. Sie können die Kapazität von Ressourcen mithilfe von Kalendereinstellungen steuern. Das System berechnet während des Planungsprozesses die Arbeitslasten für Ressourcen. **Hinweis:** Bei Produktionen, bei denen die Grobterminierung zum Einsatz kommt, kann die Feinterminierung im Anschluss an die Grobterminierung vorgenommen werden. Wird auf die Verwendung der Grobterminierung verzichtet, kann die Feinterminierung auch eigenständig verwendet werden.

## <a name="maximum-capacities-for-resources-per-job-order"></a>Maximale Kapazitäten für Ressourcen pro Einzelvorgangsauftrag
Ressourcen werden über die Feinterminierung Einzelvorgängen zugewiesen. Sie können maximale Kapazitäten für Ressourcen pro Einzelvorgangsauftrag einrichten. So können das System beispielsweise so einrichten, dass nicht mehr als 50 Prozent der Gesamtkapazität für einen Produktionsauftrag eingeplant werden. Diese Einstellung bietet mehr Kontrolle über die Planung von Ressourcen auf Feinterminierungsebene. Dadurch wird dabei geholfen, Probleme zu vermeiden, wenn für gleichzeitige Produktionen nicht ausreichend Kapazitäten verfügbar sind.

## <a name="resource-efficiency"></a>Ressourceneffizienz
Bei der Feinterminierung werden die für die Ressourcen angegebenen Effizienzgrade berücksichtigt. Mithilfe des Effizienzgrads wird die für eine Ressource reservierte Zeit entweder verringert oder erhöht. Dies wirkt sich zugleich entsprechend auf die Durchlaufzeit aus. Die folgende Formel wird für die Berechnung verwendet: Terminierungszeit = Zeit × 100 ÷ Effizienzgrad. In dieser Formel umfasst *Zeit* sowohl die Fertigungszeit als auch die Rüstzeit.




