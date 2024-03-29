---
title: Bedarfsplanung – Überblick
description: Die Bedarfsplanung wird verwendet, um unabhängigen Bedarf aus Aufträgen und abhängigen Bedarf an jedem Entkopplungspunkt für Kundenaufträge vorauszusagen. Die Reduzierungsregeln der erweiterten Bedarfsplanung stellen eine ideale Lösung für die Massenanpassung bereit.
author: t-benebo
ms.date: 07/07/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "72004"
- intro-internal
ms.assetid: 916707c9-1333-460f-a0fa-4e95f6fda2ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5c764cc186b5c8742ccfd90b5928f6625f3360c8
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/29/2022
ms.locfileid: "9065596"
---
# <a name="demand-forecasting-overview"></a>Bedarfsplanung – Überblick

[!include [banner](../includes/banner.md)]

Die Bedarfsplanung wird verwendet, um unabhängigen Bedarf aus Aufträgen und abhängigen Bedarf an jedem Entkopplungspunkt für Kundenaufträge vorauszusagen. Die Reduzierungsregeln der erweiterten Bedarfsplanung stellen eine ideale Lösung für die Massenanpassung bereit.

Um die Grundplanung zu generieren, wird eine Zusammenfassung mit historischen Transaktionen an Microsoft Azure Machine Learning übergeben, das auf Azure gehostet wird. Da dieser Dienst nicht unter Benutzern freigegeben wird, kann er problemlos angepasst werden, um den branchenspezifischen Anforderungen zu entsprechen. Sie können Supply Chain Management verwenden, um die Planung zu visualisieren, die Planung anzupassen und KPIs (Key Performance Indicators) zur Planungsgenauigkeit anzuzeigen.

> [!NOTE]
> Microsoft Azure Machine Learning Studio (klassisch) ist für die Prognoseerstellung mit maschinellem Lernen erforderlich. Ab dem 1. Dezember 2021 können Sie keine neuen Machine Learning Studio-Ressourcen (klassisch) erstellen. Sie können jedoch bis zum 31. August 2024 weiterhin Ihre vorhandenen (klassischen) Ressourcen des Machine Learning Studio verwenden. Aktualisierte Informationen finden Sie unter [Azure Machine Learning Studio](/azure/machine-learning/overview-what-is-machine-learning-studio#ml-studio-classic-vs-azure-machine-learning-studio).
> 
> Dynamics 365 Supply Chain Management Version 10.0.23 und höher unterstützen das neue Azure Machine Learning Studio.

## <a name="key-features-of-demand-forecasting"></a>Wichtigste Funktionen der Bedarfsplanung

Nachfolgend sind einige der Hauptmerkmale der Bedarfsplanung aufgeführt:

- Eine statistische Grundplanung generieren, die auf historischen Daten basiert
- Einen dynamischen Satz von Planungsdimensionen verwenden
- Bedarfstrends, Zuverlässigkeitsintervalle und Regulierungen der Planung visualisieren
- Die angepasste Planung für die Verwendung in Planungsprozessen autorisieren
- Ausreißer entfernen
- Messungen für die Planungsgenauigkeit erstellen

## <a name="major-themes-in-demand-forecasting"></a>Wichtige Themen der Bedarfsplanung

Drei wichtige Themen wurden in die Bedarfsplanung implementiert:

- **Modularität** - Die Bedarfsplanung ist modular und einfach zu konfigurieren. Sie können die Funktionalität aktivieren und deaktivieren, indem Sie den Konfigurationsschlüssel unter **Art** &gt; **Bestandsprognose** &gt; **Bedarfsplanung** ändern.
- **Wiederverwenden von Microsoft Stack** – Machine Learning ist jetzt Teil der Microsoft Cortana Analytics Suite und mit ihr können Sie schnell und einfach Predictive Analytics-Experimente erstellen, wie Experimente zur Bedarfsvorkalkulation mithilfe von Algorithmen R oder Python-Programmiersprachen und einer einfachen Drag & Drop-Schnittstelle.
  - Sie können die Bedarfsplanungsexperimente herunterladen, sie ändern und an Ihre geschäftlichen Anforderungen anpassen, sie als Webdienst auf Azure veröffentlichen und sie verwenden, um Bedarfsplanungen zu generieren. Die Experimente sind zum Download verfügbar, wenn Sie ein Supply Chain Management-Abonnement für einen Produktionsplaner als Benutzer auf Unternehmensebene besitzen.
  - Sie können eines der aktuell verfügbaren Bedarfsvorhersagenexperimente aus dem [Cortana Analytics-Katalog](https://gallery.cortanaanalytics.com/) herunterladen. Während die Bedarfsplanungsexperimente automatisch mit Supply Chain Management integriert werden, müssen Kunden und Partner die Integration von Experimenten abwickeln, die sie aus dem [Cortana Analytics-Katalog](https://gallery.cortanaanalytics.com/) herunterladen. Daher sind die Experimente aus der [Cortana Analytics Gallery](https://gallery.cortanaanalytics.com/) nicht so einfach zu handhaben wie die Experimente zur Planung des Bedarfs im Bereich Finanzen und Betrieb. Sie müssen den Code der Experimente so ändern, dass sie die Programmierschnittstelle (API) für Finanzen und Betrieb verwenden.
  - Sie können eigene Experimente in Microsoft Azure Machine Learning Studio (klassisch) erstellen, als Dienste auf Azure veröffentlichen und sie verwenden, um Bedarfsplanungen zu generieren.
  - Wenn Sie keine hohe Leistung benötigen oder wenn Sie keine großen Datenmengen verarbeiten müssen, können Sie die kostenlose Machine Learning-Schicht verwenden. Es wird empfohlen, dass Sie immer über diese Schicht beginnen, besonders während der Implementierungs- und Testphasen. Wenn Sie höhere Leistung und zusätzlichen Speicherplatz benötigen, können Sie die Standardschicht von Machine Learning verwenden. Diese Schicht erfordert ein Azure-Abonnement und beinhaltet zusätzliche Kosten. Einzelheiten zur den Machine Learning-Preisen finden Sie unter [Machine Learning Studio-Preise](https://aka.ms/machine-learning-price-info).
- **Planungsverringerung an jedem Entkopplungspunkt** – Bedarfsplanung baut auf dieser Funktionalität auf, mit der Sie abhängigen und unabhängigen Bedarf an jedem Entkopplungspunkt planen können.

## <a name="basic-flow-in-demand-forecasting"></a>Grundlegender Ablauf in der Bedarfsplanung

Das folgende Diagramm zeigt den grundlegenden Ablauf in der Bedarfsplanung.

[![Diagramm zur Einführung in die Bedarfsplanung.](./media/demand-forecasting-introduction.png)](./media/demand-forecasting-introduction.png)

Bedarfsplanungsgenerierung beginnt mit Supply Chain Management. Historische transaktionsbezogene Daten aus der Supply Chain Management-Transaktionsdatenbank werden gesammelt und in einer Stagingtabelle angezeigt. Diese Staging-Tabelle wird später an den Machine Learning-Service übergeben. Durch minimale Anpassungen können Sie verschiedene Datenquellen mit der Stagingtabelle verbinden. Die Datenquellen können Microsoft Excel-Dateien, kommagetrennte Wert (CSV)-Dateien und Daten von Microsoft Dynamics AX 2009 und Microsoft Dynamics AX 2012 einschließen. Sie können deshalb Bedarfsplanungen generieren, die historische Daten entscheiden, die von mehreren Systemen beschränkt wird. Allerdings müssen die Masterdaten, wie Artikelnamen und Maßeinheiten, in den unterschiedlichen Datenquellen übereinstimmen.

Wenn Sie die Machine Learning-Experimente der Bedarfsplanung verwenden, prüfen diese fünf Planungsmethoden für Zeitserien auf die beste Eignung, um eine Grundplanung zu berechnen. Die Parameter für diese Planungsmethode werden in Supply Chain Management verwaltet.

Die Planungen, die historischen Daten und Änderungen, die an den Bedarfsplanungen in den vorherigen Iterationen vorgenommen wurden, sind dann in Supply Chain Management verfügbar.

Sie können Supply Chain Management verwenden, um die Grundplanungen zu visualisieren und zu ändern. Manuelle Regulierungen müssen autorisiert werden, bevor die Planungen für die Planung verwendet werden können.

## <a name="limitations"></a>Einschränkungen

Die Bedarfsplanung ist ein Tool, das Kunden in der Fertigungsindustrie hilft, Planungsprozesse zu erstellen. Es bietet der Kernfunktionen von einer Bedarfsplanungslösung anzeigen und soll, sodass einfacher erweitert werden kann. Bedarfsplanung ist möglicherweise nicht die beste Art für Debitoren in Branchen wie beispielsweise Commerce, Großhandel, Warehousing, Transport oder anderen freiberuflichen Dienstleistungen abgeglichen wird.

### <a name="demand-forecast-variant-conversion-limitation"></a>Bedarfsplanungsvarianten-Konvertierungsbegrenzung

Maßeinheit (UOM) pro Variantenkonvertierung wird beim Generieren der Bedarfsplanung nicht vollständig unterstützt, wenn sich die Bestandsmaßeinheit von der Bedarfsplanungs-Maßeinheit unterscheidet.

Prognosen generieren (**Bestandsmaßeinheit > Bedarfsplanungsmaßeinheit**) verwendet die Produktmaßeinheit-Konvertierung. Beim Laden historischer Daten für die Bedarfsplanungsgenerierung wird die Produktebenen-Maßeinheitskonvertierung immer verwendet, wenn von einer Bestandsmaßeinheit zu einer Bedardsplanungsmaßeinheit konvertiert wird, selbst wenn Konvertierungen auf Variantenebene definiert werden.

Der erste Teil der Autorisierung der Planung (**Bedarfsplanungsmaßeinheit > Bestandsmaßeinheit**) verwendet Produktmaßeinheit-Konvertierung. Der zweite Teil der Autorisierung der Planung (**Bestandsmaßeinheit> Verkaufsmaßeinheit**) verwendet die Variantenmaßeinheits-Konvertierung. Wenn die generierte Bedarfsplanung autorisiert ist, erfolgt die Konvertierung in die Bestandsmaßeinheit von der Bedarfsplanungsmaßeinheit mithilfe der Maßeinheitskonvertierung auf Produktebene. Gleichzeitig werden bei der Konvertierung zwischen der Bestandsmaßeinheit und der Verkaufsmaßeinheit die von der Variantenebene definierten Konvertierungen berücksichtigt.

Beachten Sie, dass die Bedarfsplanungsmaßeinheit keine spezifische Bedeutung haben muss. Es kann als „Bedarfsplanungseinheit“ definiert werden. Für jedes der Produkte können Sie die Konvertierung als 1:1 mit der Bestandsmaßeinheit definieren.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Einrichten einer Bedarfsplanung](demand-forecasting-setup.md)
- [Eine statistische Grundplanung generieren](generate-statistical-baseline-forecast.md)
- [Manuelle Anpassungen an der Grundplanung](manual-adjustments-baseline-forecast.md)
- [Eine angepasste Planung autorisieren](authorize-adjusted-forecast.md)
- [Planungsgenauigkeit überwachen](monitor-forecast-accuracy.md)
- [Entfernen Sie Ausreißer aus den historischen Buchungsdaten, wenn Sie eine Bedarfsplanung berechnen.](remove-historical-outliers-calculating-demand-forecast.md)
- [Video: Bedarfsplanungsfunktionen erweitern](https://www.youtube.com/watch?v=4OIKIXLiNjI&feature=youtu.be)
- [Webinar: Reihe „Bedarfsplanung mit Azure Machine Learning“](https://aka.ms/DemandForecastingwithAzureMachineLearningSeries)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

