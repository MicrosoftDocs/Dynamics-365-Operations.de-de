---
title: "Startseite für die Produktprogrammplanung"
description: "Produktprogrammplanung ermöglicht es Unternehmen, die zukünftigen Anforderung für Rohmaterialen und Kapazität zu bestimmen und abzustimmen, um die Unternehmensziele zu erfüllen."
author: YuyuScheller
manager: AnnBe
ms.date: 11/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a24f75bf7e27702505d8a61ae3db83d03fe4a933
ms.openlocfilehash: a2e91cd2b72ffed78669fe3cc83b141db6f26aa2
ms.contentlocale: de-de
ms.lasthandoff: 11/29/2017

---

# <a name="master-planning-home-page"></a>Startseite für die Produktprogrammplanung

[!include[banner](../includes/banner.md)]


Produktprogrammplanung ermöglicht es Unternehmen, die zukünftigen Anforderung für Rohmaterialen und Kapazität zu bestimmen und abzustimmen, um die Unternehmensziele zu erfüllen. Produktprogrammplanung setzt Folgendes fest: 

-  Welche Rohmaterialien und Kapazitäten sind zurzeit verfügbar? 
-  Welche Rohmaterialien und Kapazitäten werden benötigt, um die Produktion zu vervollständigen? Beispielsweise was produziert, gekauft, übertragen oder zurückgestellt werden muss, bevor die Produktion ausgeführt werden kann.

Dient zum Berechnen des Bedarfs für die Produktprogrammplanung sowie zum Generieren von Bestellvorschlägen für den ausgewählten Artikel.

Die drei Hauptplanungsprozesse sind:

-  **Produktprogrammplanung** - Im Produktprogrammplan wird der Nettobedarf berechnet. Es basiert auf aktuellen und tatsächlichen Aufträgen, um gibt Unternehmen die Möglichkeit, Bestandswiederbeschaffung auf einer täglichen Basis zu steuern. Eine andere Bedingung, um dies zu beschreiben, ist der *Nettobedarfsplan*. Weitere Informationen unter [Masterplan](master-plans.md). 

-  **Absatzplanung** - Planungszeitplan der Bruttobedarf berechnet. Er basiert auf künftiger (oder geplanter) Projektionen und aktiviert Unternehmen, langfristig Material- und Kapazitätsplanung zu tätigen. Weitere Informationen unter [Künftige Planung](introduction-demand-forecasting.md). 

-  **Intergesellschaftsproduktprogrammplanung** - Die Intercompany-Produktprogrammplan berechnet den Bedarfsverlauf zu juristischen Personen. Er umfasst Angebot und Nachfrage zwischen Unternehmen nicht nur für kurzfristige, feste und nachgefragte, sondern auch für langfristige (die noch nicht fest sind), geplante Angebot und Nachfrage. Weitere Informationen finden Sie unter [Intergesellschaftsp roduktprogrammplanung](https://mbspartner.microsoft.com/AX/CourseOverview/1276) (E-Learning) (erfordert CustomerSource-Konto). 

Unternehmen können die Ausgabe des Plans ändern. Sie können verbessernde Nettoveränderung oder beides ausführen. Verbessernde Pläne aktualisieren alle Anforderungen, während Nettoveränderungspläne nur den Plan an Artikeln mit neuen Anforderungen aktualisieren, die seit den letzten hereingekommen den Planungslauf sind.

Produktprogrammpläne umfassen in der Regel das Kurzfristige mit ein, das alles von einer Woche bis zu sechs Monaten sein kann. Das Produktprogrammplanungsmodul bestimmt die Anforderungen der Lieferung "Materialien" und der Kapazität (Ressourcen), der aktuellen Bedarfs (Nettoanforderungen). In den meisten Unternehmen wird dieses erweitert, um die längste kumulierte Vorlaufzeit mit Produkten einzubeziehen, die empfangen werden.

## <a name="learning-map"></a>Lernkarte

Die folgende Lernenzuordnung zeigen die wichtigsten Konzepte und die Aufgaben, die vom Framework des Modul "Masterplanung" bestehen. Klicken Sie auf die Links im [Direktlinks](#quick-links)-Abschnitt, um zu erfahren, wie das Modul verwendet wird.

[![Lernkarte für die Masterplanung](./media/master-planning-learning-map.png)](./media/master-planning-learning-map.png)

## <a name="quick-links"></a>Direktlinks
|      |   |
|------|---|
|        [Produktprogrammpläne](master-plans.md)       |     [Plan mit Einschränkungen erstellen](./tasks/constrained-plan.md)  |
| [Materialplan für Co-Produkte erstellen](./tasks/create-material-plan-co-products.md)   |  [Produktprogrammplanung und Funktion für mehrere Standorte](master-plan-multisite-functionality.md)  |
| [Intercompany-Plan erstellen](./tasks/create-intercompany-plan.md) | [Bedarfsplanung – Überblick](introduction-demand-forecasting.md)  | 
|[Planzahlenverrechnungsschlüssel](reduction-keys.md)| [Notwendige Planungsgrundlagen](https://mbspartner.microsoft.com/AX/CourseOverview/1275) (e-Learning) (erfordert CustomerSource-Konto)     |
|  [Notwendige Planungsgrundlagen für die Prozessproduktion](https://mbspartner.microsoft.com/D365E/CourseOverview/1514) (e-Learning) (erfordert CustomerSource-Konto) | [Intercompany-Planungsgrundlagen](https://mbspartner.microsoft.com/AX/CourseOverview/1276) (e-Learning) (erfordert CustomerSource-Konto)|
                                  
## <a name="additional-resources"></a>Zusätzliche Ressourcen

### <a name="roadmaps"></a>Roadmaps
Besuchen Sie [Microsoft Dynamics 365 – Produktplan](https://roadmap.dynamics.com/), um zu erfahren, welche neue Funktionen veröffentlicht wurden und welche neuen Funktionen gerade entwickelt werden.

### <a name="blogs"></a>Blogs
Sie finden Meinungen, Neuigkeiten und weitere Informationen zur Bestandsverwaltung unter [Dynamics AX – Team für Produktionsforschung und Entwicklung – Blog](https://blogs.msdn.microsoft.com/axmfg) [Lieferkettenverwaltung im Dynamics AX Forschungs- und Entwicklungsteam-Blog](https://blogs.msdn.microsoft.com/dynamicsaxscm)

### <a name="task-guides"></a>Aufgabenleitfäden
Weitere Hilfe finden Sie als Aufgabenleitfäden innerhalb von Finance and Operations. Um auf Aufgabenleitfäden zuzugreifen, klicken Sie auf einer beliebigen Seite auf die Schaltfläche **Hilfe**.

### <a name="webinars"></a>Webinars
[Azure Machine Learning Bedarfsplanungsstrategie nutzen](https://www.youtube.com/watch?v=4nQsccdFFDA&feature=youtu.be)





