---
title: "Bedarfsplanungsüberblick"
description: "Die Bedarfsplanung wird verwendet, um unabhängigen Bedarf aus Aufträgen und abhängigen Bedarf an jedem Entkopplungspunkt für Kundenaufträge vorauszusagen. Die erweiterten Bedarfsplanungsverringerungsregeln ideale ermöglichen eine Lösung für Massenanpassung bereit."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72004
ms.assetid: 916707c9-1333-460f-a0fa-4e95f6fda2ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 9152616b81e7873426f296376b5e57c94439379d
ms.lasthandoff: 03/31/2017


---

# <a name="demand-forecasting-overview"></a>Bedarfsplanungsüberblick

Die Bedarfsplanung wird verwendet, um unabhängigen Bedarf aus Aufträgen und abhängigen Bedarf an jedem Entkopplungspunkt für Kundenaufträge vorauszusagen. Die erweiterten Bedarfsplanungsverringerungsregeln ideale ermöglichen eine Lösung für Massenanpassung bereit.

Um die Grundplanung zu generieren, wird eine Zusammenfassung mit historischen Transaktionen an Microsoft Azure Machine Learning übergeben, das auf Azure gehostet wird. Da dieser Dienst nicht unter Benutzern freigegeben wird, kann er problemlos angepasst werden, um den branchenspezifischen Anforderungen zu entsprechen. Sie können Dynamics 365 verwenden, um Arbeitsgänge die Planung visuell darstellen, Planung ändern und Key Performance Indicators (KPIs) zu Planungsrichtigkeit anzeigen.

## <a name="key-features-of-demand-forecasting"></a>Wichtigste Funktionen der Bedarfsplanung
Nachfolgend sind einige der Hauptmerkmale der Bedarfsplanung aufgeführt:

-   Eine statistische Grundplanung generieren, die auf historischen Daten basiert
-   Einen dynamischen Satz von Planungsdimensionen verwenden
-   Bedarfstrends, Zuverlässigkeitsintervalle und Regulierungen der Planung visualisieren
-   Die angepasste Planung für die Verwendung in Planungsprozessen autorisieren
-   Ausreißer entfernen
-   Messungen für die Planungsgenauigkeit erstellen

## <a name="major-themes-in-demand-forecasting"></a>Wichtige Themen der Bedarfsplanung
Drei wichtige Themen wurden in die Bedarfsplanung implementiert:

-   **Modularität** - Die Bedarfsplanung ist modular und einfach zu konfigurieren. Sie können die Funktionen an und beenden, indem Sie den Variantenschlüssel ** Handel ** ** &gt; am geplanten Lagerbestand ändern ** &gt; ** Bedarfsplanung **.
-   ** Wiederverwendung des Microsoft-Stapels ** – Microsoft ausgelöst hat die Lernfähigkeit- einer Maschineplattform.im Februar 2015 Lernfähigkeit einer Maschine, die jetzt Teil der Analyse-Suite Microsoft Cortana ist, können schnell und einfach vorbestimmte erstellt Analyseexperimente, wie Bedarfsvorkalkulationsexperimente, indem Algorithmen R oder Python-Programmiersprachen und eine einfache Drag & Drop-Schnittstelle verwendet.
    -   Sie können das Dynamics 365 für Arbeitsgangs-Bedarfsplanungsexperimente herunterladen, indem sie ändern, um Ihren geschäftlichen Anforderungen zu erfüllen, als im Azure Webdienst, veröffentlichen und diese verwenden, Bedarfsplanungen um zu generieren. Die Experimente sind für den Download verfügbar, wenn Sie für Arbeitsgangsdauerauftrag Dynamics 365 für einen Unternehmensebenenbenutzer Produktionsplaner als besitzen.
    -   Sie können eines der aktuell verfügbaren Bedarfsvorhersagenexperimente aus dem [Cortana Analytics-Katalog](https://gallery.cortanaanalytics.com/) herunterladen. Während das Dynamics 365 für Arbeitsgangs-Bedarfsplanungsexperimente automatisch mit Dynamics 365 für Arbeitsgänge integriert werden, müssen Debitoren und bietet die Integration von Experimenten verarbeiten, die vom Cortana-Analyse-Katalog herunterladen []( https://gallery.cortanaanalytics.com/). Daher Experimente von Cortana-Analyse-Katalog [] (https://gallery.cortanaanalytics.com/) sind nicht so einfach, als das Dynamics 365 für Arbeitsgangs-Bedarfsplanungsexperimente zu verwenden. Sie müssen den Code der Experimente ändern, sodass sie das Dynamics 365 für Arbeitsgangsanwendungsprogrammierschnittstelle (API) verwenden.
    -   Sie können eigene Experimente in Microsoft Azure Machine Learning Studio erstellen, als Dienste auf Azure veröffentlichen und sie verwenden, um Bedarfsplanungen zu generieren.
    -   Wenn Sie keine hohe Leistung benötigen oder wenn Sie keine großen Datenmengen verarbeiten müssen, können Sie die kostenlose Machine Learning-Schicht verwenden. Es wird empfohlen, dass Sie immer über diese Schicht beginnen, besonders während der Implementierungs- und Testphasen. Wenn Sie höhere Leistung und zusätzlichen Speicherplatz benötigen, können Sie die Standardschicht von Machine Learning verwenden. Diese Schicht erfordert ein Azure-Abonnement und beinhaltet zusätzliche Kosten. Einzelheiten zur den Machine Learning-Preisen finden Sie unter <http://aka.ms/machine-learning-price-info>.
-   ** Planungsverringerung zu jedem Zeitpunkt entkoppelnden ** – Bedarfsplanung in Dynamics 365 für erstellten Arbeitsgänge auf dieser Funktionen, die zum Unterhaltsberechtigten und unabhängiger Bedarf an irgendeinem Punkt entkoppelnden planen können.

## <a name="basic-flow-in-demand-forecasting"></a>Grundlegender Ablauf in der Bedarfsplanung
Das folgende Diagramm zeigt den grundlegenden Ablauf in der Bedarfsplanung. 

![Bedarfsplanungs-Einführungsdiagramm( [] . /media/demand-forecasting-introduction.png)]". /media/demand-forecasting-introduction.png)

Bedarfsplanungsgenerierungsanfänge in Dynamics 365 für Arbeitsgänge. Historische Transaktionsdaten vornehmen vom Dynamics 365 für buchungsbezogene Datenbank der Arbeitsgänge werden gesammelt und eine Stagingtabelle auffüllen. Einem Lernfähigkeit- einer Maschineservice diese Stagingtabelle wird später gespeist. Wenn von Minimum- Anpassung ausführen, können diesem verschiedene Datenquellen in die Stagingtabelle einstecken. Die können Datenquellen Microsoft Excel-Dateien, kommagetrennte Wert (CSV)- Dateien und Daten aus Microsoft Dynamics AX 2009 und aus Microsoft Dynamics AX 2012 sind. Sie können deshalb Bedarfsplanungen generieren, die historische Daten entscheiden, die von mehreren Systemen beschränkt wird. Allerdings müssen die Masterdaten, wie Artikelnamen und Maßeinheiten, in den unterschiedlichen Datenquellen übereinstimmen.

Wenn Sie das Arbeitsgangs-Bedarfsplanungs-Lernfähigkeit-einer Dynamics 365 für Maschineexperimente verwenden, sucht nach einer Besteignung mit fünf Zeitreihenprognoseverfahren, eine Basisplanung zu berechnen. Die Parameter werden für diese Methode in Dynamics 365 für Arbeitsgänge verwaltet. 

Die Planungen, die vergleichende und um Änderungen, die sich auf Auffüllung in früheren Iterationen vorgenommen wurden, werden dann in Dynamics 365 für Arbeitsgänge verfügbar. 

Sie können Dynamics 365 verwenden, damit die Basisplanungen visuell Arbeitsgänge angezeigt und geändert werden. Manuelle Regulierungen müssen autorisiert werden, bevor die Planungen für die Planung verwendet werden können.

## <a name="limitations"></a>Einschränkungen
Bedarfsplanung in Dynamics 365 für Arbeitsgänge ist ein Tool, das Debitoren in derFertigungsindustrie können, Planungs prozesse zu erstellen. Es bietet der Kernfunktionen von einer Bedarfsplanungslösung anzeigen und soll, sodass einfacher erweitert werden kann. Bedarfsplanung möglicherweise nicht die Anzahl, die für Debitoren in Branchen verwendet, beispielsweise Einzelhandel Großhandel, Warehousing, Transport oder anderen freiberuflichen Dienstleistungen abgeglichen wird.

<a name="see-also"></a>Siehe auch
--------

[Demand forecasting setup](demand-forecasting-setup.md)

[Generating a statistical baseline forecast](generate-statistical-baseline-forecast.md)

[Making manual adjustments to the baseline forecast](manual-adjustments-baseline-forecast.md)

[Authorizing the adjusted forecast](authorize-adjusted-forecast.md)

[Monitoring forecast accuracy](monitor-forecast-accuracy.md)

[Remove outliers from historical transaction data when calculating a demand forecast](remove-historical-outliers-calculating-demand-forecast.md)


