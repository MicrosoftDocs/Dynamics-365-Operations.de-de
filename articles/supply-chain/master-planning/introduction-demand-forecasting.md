---
title: Bedarfsplanung – Überblick
description: Die Bedarfsplanung wird verwendet, um unabhängigen Bedarf aus Aufträgen und abhängigen Bedarf an jedem Entkopplungspunkt für Kundenaufträge vorauszusagen. Die Reduzierungsregeln der erweiterten Bedarfsplanung stellen eine ideale Lösung für die Massenanpassung bereit.
author: roxanadiaconu
manager: AnnBe
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 72004
ms.assetid: 916707c9-1333-460f-a0fa-4e95f6fda2ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ca463d821292a2ad53462a3575f2d5712b9e53cc
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004041"
---
# <a name="demand-forecasting-overview"></a>Bedarfsplanung – Überblick

[!include [banner](../includes/banner.md)]

Die Bedarfsplanung wird verwendet, um unabhängigen Bedarf aus Aufträgen und abhängigen Bedarf an jedem Entkopplungspunkt für Kundenaufträge vorauszusagen. Die Reduzierungsregeln der erweiterten Bedarfsplanung stellen eine ideale Lösung für die Massenanpassung bereit.

Um die Grundplanung zu generieren, wird eine Zusammenfassung mit historischen Transaktionen an Microsoft Azure Machine Learning übergeben, das auf Azure gehostet wird. Da dieser Dienst nicht unter Benutzern freigegeben wird, kann er problemlos angepasst werden, um den branchenspezifischen Anforderungen zu entsprechen. Sie können Supply Chain Management verwenden, um die Planung zu visualisieren, die Planung anzupassen und KPIs (Key Performance Indicators) zur Planungsgenauigkeit anzuzeigen.

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
    -   Sie können die Bedarfsplanungsexperimente herunterladen, sie ändern und an Ihre geschäftlichen Anforderungen anpassen, sie als Webdienst auf Azure veröffentlichen und sie verwenden, um Bedarfsplanungen zu generieren. Die Experimente sind zum Download verfügbar, wenn Sie ein Supply Chain Management-Abonnement für einen Produktionsplaner als Benutzer auf Unternehmensebene besitzen.
    -   Sie können eines der aktuell verfügbaren Bedarfsvorhersagenexperimente aus dem [Cortana Analytics-Katalog](https://gallery.cortanaanalytics.com/) herunterladen. Während die Bedarfsplanungsexperimente automatisch mit Supply Chain Management integriert werden, müssen Kunden und Partner die Integration von Experimenten abwickeln, die sie aus dem [Cortana Analytics-Katalog](https://gallery.cortanaanalytics.com/) herunterladen. Daher sind Experimente aus dem [Cortana Analytics-Katalog](https://gallery.cortanaanalytics.com/) nicht so einfach zu verwenden wie die Finance and Operations Bedarfsplanungsexperimente. Sie müssen den Code der Experimente ändern, sodass sie die Finance and Operations Anwendungprogrammschnittstelle verwenden.
    -   Sie können eigene Experimente in Microsoft Azure Machine Learning Studio (klassisch) erstellen, als Dienste auf Azure veröffentlichen und sie verwenden, um Bedarfsplanungen zu generieren.
    -   Wenn Sie keine hohe Leistung benötigen oder wenn Sie keine großen Datenmengen verarbeiten müssen, können Sie die kostenlose Machine Learning-Schicht verwenden. Es wird empfohlen, dass Sie immer über diese Schicht beginnen, besonders während der Implementierungs- und Testphasen. Wenn Sie höhere Leistung und zusätzlichen Speicherplatz benötigen, können Sie die Standardschicht von Machine Learning verwenden. Diese Schicht erfordert ein Azure-Abonnement und beinhaltet zusätzliche Kosten. Einzelheiten zur den Machine Learning-Preisen finden Sie unter [Machine Learning Studio-Preise](https://aka.ms/machine-learning-price-info).
-   **Planungsverringerung an jedem Entkopplungspunkt** – Bedarfsplanung baut auf dieser Funktionalität auf, mit der Sie abhängigen und unabhängigen Bedarf an jedem Entkopplungspunkt planen können.

## <a name="basic-flow-in-demand-forecasting"></a>Grundlegender Ablauf in der Bedarfsplanung
Das folgende Diagramm zeigt den grundlegenden Ablauf in der Bedarfsplanung. 

[![Einführung in die Bedarfsplanung](./media/demand-forecasting-introduction.png)](./media/demand-forecasting-introduction.png)

Bedarfsplanungsgenerierung beginnt mit Supply Chain Management. Historische transaktionsbezogene Daten aus der Supply Chain Management-Transaktionsdatenbank werden gesammelt und in einer Stagingtabelle angezeigt. Diese Staging-Tabelle wird später an den Machine Learning-Service übergeben. Durch minimale Anpassungen können Sie verschiedene Datenquellen mit der Stagingtabelle verbinden. Die Datenquellen können Microsoft Excel-Dateien, kommagetrennte Wert (CSV)-Dateien und Daten von Microsoft Dynamics AX 2009 und Microsoft Dynamics AX 2012 einschließen. Sie können deshalb Bedarfsplanungen generieren, die historische Daten entscheiden, die von mehreren Systemen beschränkt wird. Allerdings müssen die Masterdaten, wie Artikelnamen und Maßeinheiten, in den unterschiedlichen Datenquellen übereinstimmen.

Wenn Sie die Machine Learning-Experimente der Bedarfsplanung verwenden, prüfen diese fünf Planungsmethoden für Zeitserien auf die beste Eignung, um eine Grundplanung zu berechnen. Die Parameter für diese Planungsmethode werden in Supply Chain Management verwaltet. 

Die Planungen, die historischen Daten und Änderungen, die an den Bedarfsplanungen in den vorherigen Iterationen vorgenommen wurden, sind dann in Supply Chain Management verfügbar. 

Sie können Supply Chain Management verwenden, um die Grundplanungen zu visualisieren und zu ändern. Manuelle Regulierungen müssen autorisiert werden, bevor die Planungen für die Planung verwendet werden können.

## <a name="limitations"></a>Einschränkungen
Die Bedarfsplanung ist ein Tool, das Kunden in der Fertigungsindustrie hilft, Planungsprozesse zu erstellen. Es bietet der Kernfunktionen von einer Bedarfsplanungslösung anzeigen und soll, sodass einfacher erweitert werden kann. Bedarfsplanung ist möglicherweise nicht die beste Art für Debitoren in Branchen wie beispielsweise Commerce, Großhandel, Warehousing, Transport oder anderen freiberuflichen Dienstleistungen abgeglichen wird.

<a name="additional-resources"></a>Zusätzliche Ressourcen
--------

[Einrichten einer Bedarfsplanung](demand-forecasting-setup.md)

[Eine statistische Grundplanung generieren](generate-statistical-baseline-forecast.md)

[Manuelle Anpassungen an der Grundplanung](manual-adjustments-baseline-forecast.md)

[Eine angepasste Planung autorisieren](authorize-adjusted-forecast.md)

[Planungsgenauigkeit überwachen](monitor-forecast-accuracy.md)

[Entfernen Sie Ausreißer aus den historischen Buchungsdaten, wenn Sie eine Bedarfsplanung berechnen.](remove-historical-outliers-calculating-demand-forecast.md)

[Bedarfsplanungsfunktionen erweitern](https://www.youtube.com/watch?v=4OIKIXLiNjI&feature=youtu.be)



