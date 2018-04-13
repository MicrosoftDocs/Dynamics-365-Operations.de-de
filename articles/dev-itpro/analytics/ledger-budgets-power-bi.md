---
title: Ist-Wert im Vergleich mit Budget-Power BI-Inhalt
description: "In diesem Thema wird der Ist-Wert im Vergleich mit Budget-Power BI-Inhalt beschrieben. Es wird beschrieben, wie auf die Berichte, die im Inhalt enthalten sind, zugegriffen wird und es werden Informationen zum Datenmodell und den Entitäten bereitgestellt, die zum Erstellen des Inhalts verwendet wurden."
author: ryansandness
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BudgetTrackingWorkspace
audience: Application user, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: aac6439bb54b3b9cab066b06c01763e880efef8e
ms.openlocfilehash: fa0c56f4773b9062d616772e2bca9a576ad37ce2
ms.contentlocale: de-de
ms.lasthandoff: 12/18/2017

---

# <a name="actual-vs-budget-power-bi-content"></a>Ist-Wert im Vergleich mit Budget-Power BI-Inhalt

[!INCLUDE [banner](../includes/banner.md)]

In diesem Thema wird der **Istwert verglichen mit Budget**-Inhalt von Microsoft Power BI beschrieben. Es wird erläutert, wie Sie auf die Power Bl-Berichte zugreifen und enthält Informationen zum Datenmodell und zu den Entitäten, die verwendet werden, um den Inhalt zu erstellen. 

## <a name="overview"></a>Überblick

Der **Istwert verglichen mit Budget**-Inhalt von Power BI wurde für Personen erstellt, die für die Überwachung der tatsächlichen Leistung im Vergleich zur Budgetleistung in ihrer Organisation verantwortlich sind. Der **Ist-Wert im Vergleich mit Budget**-Inhalt für Power BI bietet Einblicke in Budgetabweichungen. Sie können Budgets für das aktuelle Jahr nach Firmenkategorie, Budgetcode, Hauptkonto, Hauptkontobeschreibungen oder Finanzzeitraum analysieren, um ein besseres Verständnis für die Ursache von Abweichungen zu bekommen. 

## <a name="accessing-the-power-bi-content"></a>Zugreifen au Power BI Inhalt
Berichte vom **Istwert verglichen mit Budget** Power BI-Inhalt werden in **Sachkontobudget und Planungen** in **CFO** angezeigt.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Berichte, die im Power BI Inhalt enthalten sind
Die folgende Tabelle enthält Details zur Metrik, die sich auf jeder Berichtsseite im **Ist-Wert im Vergleich mit Budget**-Power BI-Inhalt befindet.


|           Bericht            |                                       Metriken                                        |
|-----------------------------|--------------------------------------------------------------------------------------|
| Ausgaben – Istwert verglichen mit Budget |  <ul><li>Diesjährige Gesamtausgaben</li><li>Diesjährige Budgetgesamtausgaben</li></ul>  |
| Umsatzerlös – Istwert im Vergleich zu Budget  |   <ul><li>Diesjähriger Gesamtumsatz</li><li>Diesjähriger Budgetgesamtumsatz</li><ul>    |
|           Spesen           | <ul><li>Diesjährige Gesamtausgaben</li><li>Ziel der Ausgaben basierend auf Budget </li><ul> |
|           Umsatzerlös           |  <ul><li>Diesjähriger Gesamtumsatz</li><li>Ziel der Umsatzerlöse basierend auf Budget </li><ul>  |
|         Nettoeinkommen          |  <ul><li>Diesjähriges Nettoeinkommen</li><li>Ziel des Nettoeinkommens basierend auf Budget </li><ul>  |

## <a name="understanding-the-data-model-and-entities"></a>Das Datenmodells und die Entitäten verstehen

|          Entität           |                                     Inhalt                                     |
|---------------------------|----------------------------------------------------------------------------------|
| Hauptbuchaktivitäten |                    Buchungsbeträge für das Hauptbuch                    |
|     Budgetaktivitäten     |                   Buchungsbeträge für das Budgetregister                    |
|       Hauptkonten       |                        Hauptkonten, nach denen Berichte gefiltert werden können                        |
|     Steuerkalender      |                      Steuerkalender, nach denen Berichte gefiltert werden können                       |
|          Sachkonten          |       Sachkonten, die verwendet werden können, um den Bericht nach dem aktuellen Sachkonto zu filtern        |
|       Budgetcodes        |                        Budgetcodes, nach denen Berichte gefiltert werden können                         |
|      Juristische Personen       | Juristische Personen, die verwendet werden können, um nach der aktuellen juristischen Person zu filtern. |


