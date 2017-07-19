---
title: "Bedarfsplanung – Überblick"
description: "Die Bedarfsplanung wird verwendet, um unabhängigen Bedarf aus Aufträgen und abhängigen Bedarf an jedem Entkopplungspunkt für Kundenaufträge vorauszusagen. Die Reduzierungsregeln der erweiterten Bedarfsplanung stellen eine ideale Lösung für die Massenanpassung bereit."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 72004
ms.assetid: 916707c9-1333-460f-a0fa-4e95f6fda2ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 6b4498ae05b9495918c0a079cc88903820192a59
ms.contentlocale: de-de
ms.lasthandoff: 06/13/2017

---

# <a name="demand-forecasting-overview"></a>Bedarfsplanung – Überblick

[!include[banner](../includes/banner.md)]


Die Bedarfsplanung wird verwendet, um unabhängigen Bedarf aus Aufträgen und abhängigen Bedarf an jedem Entkopplungspunkt für Kundenaufträge vorauszusagen. Die Reduzierungsregeln der erweiterten Bedarfsplanung stellen eine ideale Lösung für die Massenanpassung bereit.

Um die Grundplanung zu generieren, wird eine Zusammenfassung mit historischen Transaktionen an Microsoft Azure Machine Learning übergeben, das auf Azure gehostet wird. Da dieser Dienst nicht unter Benutzern freigegeben wird, kann er problemlos angepasst werden, um den branchenspezifischen Anforderungen zu entsprechen. Sie können Finance and Operations verwenden, um die Planung zu visualisieren, die Planung anzupassen und KPIs (Key Performance Indicators) zur Planungsgenauigkeit anzuzeigen.

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

-   **Modularität** - Die Bedarfsplanung ist modular und einfach zu konfigurieren. Sie können die Funktionalität aktivieren und deaktivieren, indem Sie den Konfigurationsschlüssel unter **Art** &gt; **Bestandsprognose** &gt; **Bedarfsplanung** ändern.
-   **Wiederverwendung des Microsoft-Stapels** – Microsoft hat die Machine Learning-Plattform im Februar 2015 veröffentlicht. Machine Learning ist jetzt Teil der Microsoft Cortana Analytics Suite und kann schnell und einfach vorbestimmte erstellt Analyseexperimente, wie Bedarfsvorkalkulationsexperimente über Algorithmen in R oder Python und eine einfache Drag & Drop-Schnittstelle verwendet.
    -   Sie können die Finance and Operations-Bedarfsplanungsexperimente herunterladen, sie ändern und an Ihre geschäftlichen Anforderungen anpassen, sie als Webdienst auf Azure veröffentlichen und sie verwenden, um Bedarfsplanungen zu generieren. Die Experimente sind zum Download verfügbar, wenn Sie ein Finance and Operations-Abonnement für einen Produktionsplaner als Benutzer auf Unternehmensebene besitzen.
    -   Sie können eines der aktuell verfügbaren Bedarfsvorhersagenexperimente aus dem [Cortana Analytics-Katalog](https://gallery.cortanaanalytics.com/) herunterladen. Während die Finance and Operations-Bedarfsplanungsexperimente automatisch mit Finance and Operations integriert werden, müssen Kunden und Partner die Integration von Experimenten abwickeln, die sie aus dem [Cortana Analytics-Katalog](https://gallery.cortanaanalytics.com/) herunterladen. Daher sind Experimente aus dem [Cortana Analytics-Katalog](https://gallery.cortanaanalytics.com/) nicht so einfach zu verwenden wie die Finance and Operations-Bedarfsplanungsexperimente. Sie müssen den Code der Experimente ändern, sodass sie die Finance and Operations-API verwenden können.
    -   Sie können eigene Experimente in Microsoft Azure Machine Learning Studio erstellen, als Dienste auf Azure veröffentlichen und sie verwenden, um Bedarfsplanungen zu generieren.
    -   Wenn Sie keine hohe Leistung benötigen oder wenn Sie keine großen Datenmengen verarbeiten müssen, können Sie die kostenlose Machine Learning-Schicht verwenden. Es wird empfohlen, dass Sie immer über diese Schicht beginnen, besonders während der Implementierungs- und Testphasen. Wenn Sie höhere Leistung und zusätzlichen Speicherplatz benötigen, können Sie die Standardschicht von Machine Learning verwenden. Diese Schicht erfordert ein Azure-Abonnement und beinhaltet zusätzliche Kosten. Einzelheiten zur den Machine Learning-Preisen finden Sie unter <http://aka.ms/machine-learning-price-info>.
-   **Planungsverringerung an jedem Entkopplungspunkt** – Die Bedarfsplanung in Finance and Operations baut auf dieser Funktionalität auf, mit der Sie abhängigen und unabhängigen Bedarf an jedem Entkopplungspunkt planen können.

## <a name="basic-flow-in-demand-forecasting"></a>Grundlegender Ablauf in der Bedarfsplanung
Das folgende Diagramm zeigt den grundlegenden Ablauf in der Bedarfsplanung. 

[![Einführung in die Bedarfsplanung](./media/demand-forecasting-introduction.png)](./media/demand-forecasting-introduction.png)

Die Erstellung der Bedarfsplanung beginnt in Finance and Operations. Historische transaktionsbezogene Daten aus der Finance and Operations-Transaktionsdatenbank werden gesammelt und in einer Stagingtabelle angezeigt. Diese Staging-Tabelle wird später an den Machine Learning-Service übergeben. Durch minimale Anpassungen können Sie verschiedene Datenquellen mit der Stagingtabelle verbinden. Die können Datenquellen wie Microsoft Excel-Dateien, kommagetrennte Wert (CSV)- Dateien und Daten aus Microsoft Dynamics AX 2009 und Microsoft Dynamics AX 2012 verwenden. Sie können deshalb Bedarfsplanungen generieren, die historische Daten entscheiden, die von mehreren Systemen beschränkt wird. Allerdings müssen die Masterdaten, wie Artikelnamen und Maßeinheiten, in den unterschiedlichen Datenquellen übereinstimmen.

Wenn Sie die Machine Learning-Experimente der Finance and Operations-Bedarfsplanung verwenden, prüfen diese fünf Planungsmethoden für Zeitserien auf die beste Eignung, um eine Grundplanung zu berechnen. Die Parameter für diese Planungsmethode werden in Finance and Operations verwaltet. 

Die Planungen, die historischen Daten und Änderungen, die an den Bedarfsplanungen in den vorherigen Iterationen vorgenommen wurden, sind dann in Finance and Operations verfügbar. 

Sie können Finance and Operations verwenden, um die Grundplanungen zu visualisieren und zu ändern. Manuelle Regulierungen müssen autorisiert werden, bevor die Planungen für die Planung verwendet werden können.

## <a name="limitations"></a>Einschränkungen
Die Bedarfsplanung in Finance and Operations ist ein Tool, das Kunden in der Fertigungsindustrie hilft, Planungsprozesse zu erstellen. Es bietet der Kernfunktionen von einer Bedarfsplanungslösung anzeigen und soll, sodass einfacher erweitert werden kann. Bedarfsplanung möglicherweise nicht die Anzahl, die für Debitoren in Branchen verwendet, beispielsweise Einzelhandel Großhandel, Warehousing, Transport oder anderen freiberuflichen Dienstleistungen abgeglichen wird.

<a name="see-also"></a>Siehe auch
--------

[Einrichten einer Bedarfsplanung](demand-forecasting-setup.md)

[Generieren einer statistischen Grundplanung](generate-statistical-baseline-forecast.md)

[Manuelle Anpassungen an die Grundplanung](manual-adjustments-baseline-forecast.md)

[Autorisieren der angepassten Planung](authorize-adjusted-forecast.md)

[Überwachen der Planungsgenauigkeit](monitor-forecast-accuracy.md)

[Entfernen Sie Ausreißer aus den historischen Buchungsdaten, wenn Sie eine Bedarfsplanung berechnen.](remove-historical-outliers-calculating-demand-forecast.md)




