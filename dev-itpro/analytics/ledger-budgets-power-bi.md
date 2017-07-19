---
title: Ist-Wert im Vergleich mit Budget-Power BI-Inhalt
description: "In diesem Thema wird der Ist-Wert im Vergleich mit Budget-Power BI-Inhalt beschrieben. Es wird beschrieben, wie auf die Berichte, die im Inhalt enthalten sind, zugegriffen wird und es werden Informationen zum Datenmodell und den Entitäten bereitgestellt, die zum Erstellen des Inhalts verwendet wurden."
author: ryansandness
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application user, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations, UnifiedOperations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2017-06-30T00:00:00.000Z
ms.dyn365.ops.version: July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 5d52cce3cccb16f0645d9de1832ebeffbfaf3a09
ms.contentlocale: de-de
ms.lasthandoff: 06/13/2017

---

# <a name="actual-vs-budget-power-bi-content"></a>Ist-Wert im Vergleich mit Budget-Power BI-Inhalt

[!include[banner](../includes/banner.md)]


In diesem Thema wird der **Istwert verglichen mit Budget**-Inhalt von Microsoft Power BI beschrieben. Es wird erläutert, wie Sie auf die Power Bl-Berichte zugreifen und enthält Informationen zum Datenmodell und zu den Entitäten, die verwendet werden, um den Inhalt zu erstellen. 

# <a name="overview"></a>Überblick

Der **Istwert verglichen mit Budget**-Inhalt von Power BI wurde für Personen erstellt, die für die Überwachung der tatsächlichen Leistung im Vergleich zur Budgetleistung in ihrer Organisation verantwortlich sind. Der **Ist-Wert im Vergleich mit Budget**-Inhalt für Power BI bietet Einblicke in Budgetabweichungen. Sie können Budgets für das aktuelle Jahr nach Firmenkategorie, Budgetcode, Hauptkonto, Hauptkontobeschreibungen oder Finanzzeitraum analysieren, um ein besseres Verständnis für die Ursache von Abweichungen zu bekommen. 

# <a name="accessing-the-power-bi-content"></a>Zugreifen au Power BI Inhalt
Wenn Sie das Update von Juli 2017 für Microsoft Dynamics 365 for Finance and Operations, Enterprise-Edition, verwenden, werden Berichte vom **Ist-Wert im Vergleich mit Budget**-Inhalt von Power BI in den Arbeitsbereichen **Sachkontobudget und Planungen** und **Finanzabteilungsleiter** angezeigt.

# <a name="reports-that-are-included-in-the-power-bi-content"></a>Berichte, die im Power BI Inhalt enthalten sind
Die folgende Tabelle enthält Details zur Metrik, die sich auf jeder Berichtsseite im **Ist-Wert im Vergleich mit Budget**-Power BI-Inhalt befindet.

| Bericht                      | Metriken |
|-----------------------------|---------|
| Ausgaben – Istwert verglichen mit Budget | <ul><li>Diesjährige Gesamtausgaben</li><li>Diesjährige Budgetgesamtausgaben</li></ul> |
| Umsatzerlös – Istwert im Vergleich zu Budget  | <ul><li>Diesjähriger Gesamtumsatz</li><li>Diesjähriger Budgetgesamtumsatz</li><ul> |
| Spesen                     | <ul><li>Diesjährige Gesamtausgaben</li><li>Ziel der Ausgaben basierend auf Budget </li><ul> |
| Umsatzerlös                     | <ul><li>Diesjähriger Gesamtumsatz</li><li>Ziel der Umsatzerlöse basierend auf Budget </li><ul> |
| Nettoeinkommen                  | <ul><li>Diesjähriges Nettoeinkommen</li><li>Ziel des Nettoeinkommens basierend auf Budget </li><ul> |

## <a name="extending-the-power-bi-content"></a>Erweitern des Power BI-Inhalts
Wenn Sie die Inhaltspakete verwenden, die in Microsoft Dynamics Lifecycle Services (LCS) verfügbar sind, können Sie großartige Analysen für Person bereitstellen, die sich nicht in Microsoft Dynamics 365 anmelden. Sie können diese Inhaltspakete so ändern, dass sie andere Berichte oder grafische Elemente umfassen, und die Inhaltspakete dann für die Analyse auf Ihrem Power BI.com-Mandanten veröffentlichen. 

Sie können den **Ist-Wert im Vergleich mit Budget**-Power BI-Inhalt in der freigebenen Anlagenbibliothek in LCS finden. Weitere Informationen dazu, wie Sie Power BI-Inhalte herunterladen und in Ihrer Organisation implementieren, finden Sie unter [Power BI-Inhalt in LCS von Microsoft und Ihren Partnern](power-bi-content-microsoft-partners.md). Um eine Vorführung anzusehen, die zeigt, wie der Power BI-Inhalt impementiert wird, zeigen Sie den Office Mix [Power BI-Inhalt von Microsoft und Ihren Partnern in Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) an.

# <a name="understanding-the-data-model-and-entities"></a>Das Datenmodells und die Entitäten verstehen

| Entität                    | Inhalt |
|---------------------------|----------|
| Hauptbuchaktivitäten | Buchungsbeträge für das Hauptbuch |
| Budgetaktivitäten         | Buchungsbeträge für das Budgetregister |
| Hauptkonten             | Hauptkonten, nach denen Berichte gefiltert werden können |
| Steuerkalender          | Steuerkalender, nach denen Berichte gefiltert werden können |
| Sachkonten                   | Sachkonten, die verwendet werden können, um den Bericht nach dem aktuellen Sachkonto zu filtern |
| Budgetcodes              | Budgetcodes, nach denen Berichte gefiltert werden können |
| Juristische Personen            | Juristische Personen, die verwendet werden können, um nach der aktuellen juristischen Person zu filtern. |

