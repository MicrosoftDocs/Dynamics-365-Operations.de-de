---
title: Startseite für die Produktprogrammplanung
description: Produktprogrammplanung ermöglicht es Unternehmen, die zukünftigen Anforderung für Rohmaterialen und Kapazität zu bestimmen und abzustimmen, um die Unternehmensziele zu erfüllen.
author: ShylaThompson
manager: AnnBe
ms.date: 12/03/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0588ad24cb28a32557361e1a2e5391502a8b46d7
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/18/2019
ms.locfileid: "2814260"
---
# <a name="master-planning-home-page"></a>Startseite für die Produktprogrammplanung

[!include [banner](../includes/banner.md)]

Produktprogrammplanung ermöglicht es Unternehmen, die zukünftigen Anforderung für Rohmaterialen und Kapazität zu bestimmen und abzustimmen, um die Unternehmensziele zu erfüllen. Produktprogrammplanung setzt Folgendes fest: 

-  Welche Rohmaterialien und Kapazitäten sind zurzeit verfügbar? 
-  Welche Rohmaterialien und Kapazitäten werden benötigt, um die Produktion zu vervollständigen? Beispielsweise was produziert, gekauft, übertragen oder zurückgestellt werden muss, bevor die Produktion ausgeführt werden kann.

Dient zum Berechnen des Bedarfs für die Produktprogrammplanung sowie zum Generieren von Bestellvorschlägen für den ausgewählten Artikel.

Die drei Hauptplanungsprozesse sind:

-  **Produktprogrammplanung** - Im Produktprogrammplan wird der Nettobedarf berechnet. Es basiert auf aktuellen und tatsächlichen Aufträgen, um gibt Unternehmen die Möglichkeit, Bestandswiederbeschaffung auf einer täglichen Basis zu steuern. Eine andere Bedingung, um dies zu beschreiben, ist der *Nettobedarfsplan*. Weitere Informationen finden Sie unter [Masterplanübersicht](master-plans.md). 

-  **Absatzplanung** - Planungszeitplan der Bruttobedarf berechnet. Er basiert auf künftiger (oder geplanter) Projektionen und aktiviert Unternehmen, langfristig Material- und Kapazitätsplanung zu tätigen. Weitere Informationen finden Sie unter [Übersicht der Bedarfsprognose](introduction-demand-forecasting.md). 

-  **Intergesellschaftsproduktprogrammplanung** - Die Intercompany-Produktprogrammplan berechnet den Bedarfsverlauf zu juristischen Personen. Er umfasst Angebot und Nachfrage zwischen Unternehmen nicht nur für kurzfristige, feste und nachgefragte, sondern auch für langfristige (die noch nicht fest sind), geplante Angebot und Nachfrage. Weitere Informationen finden Sie unter [Intercompany-Produktprogrammplanungslauf](https://mbspartner.microsoft.com/AX/CourseOverview/1276) (eLearning) (CustomerSource-Konto erforderlich). 

Unternehmen können die Ausgabe des Plans ändern. Sie können verbessernde Nettoveränderung oder beides ausführen. Verbessernde Pläne aktualisieren alle Anforderungen, während Nettoveränderungspläne nur den Plan an Artikeln mit neuen Anforderungen aktualisieren, die seit den letzten hereingekommen den Planungslauf sind.

Produktprogrammpläne umfassen in der Regel das Kurzfristige mit ein, das alles von einer Woche bis zu sechs Monaten sein kann. Das Produktprogrammplanungsmodul bestimmt die Anforderungen der Lieferung "Materialien" und der Kapazität (Ressourcen), der aktuellen Bedarfs (Nettoanforderungen). In den meisten Unternehmen wird dieses erweitert, um die längste kumulierte Vorlaufzeit mit Produkten einzubeziehen, die empfangen werden.

## <a name="learning-map"></a>Lernkarte

Die folgende Lernenzuordnung zeigen die wichtigsten Konzepte und die Aufgaben, die vom Framework des Modul "Masterplanung" bestehen. Klicken Sie auf die Links im [Direktlinks](#quick-links)-Abschnitt, um zu erfahren, wie das Modul verwendet wird.

[![Lernkarte für die Masterplanung](./media/master-planning-learning-map.png)](./media/master-planning-learning-map.png)

## <a name="quick-links"></a>Direktlinks

- [Hauptpläne – Übersicht](master-plans.md)  
- [Plan mit Einschränkungen erstellen](./tasks/constrained-plan.md)
- [Materialplan für Co-Produkte erstellen](./tasks/create-material-plan-co-products.md)
- [Hauptpläne und Funktion für mehrere Standorte – Übersicht](master-plan-multisite-functionality.md)
- [Intercompany-Plan erstellen](./tasks/create-intercompany-plan.md)
- [Bedarfsplanung – Übersicht](introduction-demand-forecasting.md)
- [Planzahlenverrechnungsschlüssel vorhersagen](reduction-keys.md)
                                  
## <a name="additional-resources"></a>Zusätzliche Ressourcen

### <a name="roadmaps"></a>Roadmaps
Besuchen Sie [Microsoft Dynamics 365 – Produktplan](https://roadmap.dynamics.com/), um zu erfahren, welche neue Funktionen veröffentlicht wurden und welche neuen Funktionen gerade entwickelt werden.

### <a name="blogs"></a>Blogs
Sie finden Meinungen, Neuigkeiten und weitere Informationen zur Produktprogrammplanung und zu anderen Lösungen im [Dynamics AX Manufacturing R&D Team-Blog](https://blogs.msdn.microsoft.com/axmfg) und [Supply Chain Management in Dynamics AX R&D Team-Blog](https://blogs.msdn.microsoft.com/dynamicsaxscm).

### <a name="task-guides"></a>Aufgabenleitfäden
Zusätzliche Hilfe steht über Aufgabenhandbücher zur Verfügung. Um auf Aufgabenleitfäden zuzugreifen, klicken Sie auf einer beliebigen Seite auf die Schaltfläche **Hilfe**.

### <a name="webinars"></a>Webinars
[Azure Machine Learning Bedarfsplanungsstrategie nutzen](https://www.youtube.com/watch?v=4nQsccdFFDA&feature=youtu.be)

### <a name="tech-conference-recordings"></a>Technologiekonferenzaufzeichnungen
-  [Bedarfsplanungsfunktionen erweitern](https://www.youtube.com/watch?v=4OIKIXLiNjI&feature=youtu.be)
-  [Produktprogrammplanung – Hinweise und Tricks zur Problembehebung im Bereich der Leistung](https://youtu.be/7v8BPmEs9Dg)
-  [Hilfe! PPS ist langsam!](https://youtu.be/RLXybx20B5o)



