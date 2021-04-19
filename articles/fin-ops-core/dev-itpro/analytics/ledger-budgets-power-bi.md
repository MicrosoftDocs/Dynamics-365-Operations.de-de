---
title: Power BI-Inhalt zu Ist im Vergleich mit Budget
description: In diesem Thema wird der Power BI-Inhalt zu Ist im Vergleich mit Budget beschrieben. Es wird erläutert, wie auf Berichte zugegriffen wird, und es werden Informationen zum Datenmodell bereitgestellt.
author: panolte
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetTrackingWorkspace
audience: Application user, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 9cc52f4cdab3084c9ac43078b0b0d534119ab514
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744238"
---
# <a name="actual-vs-budget-power-bi-content"></a>Power BI-Inhalt zu Ist im Vergleich mit Budget

[!include [banner](../includes/banner.md)]

In diesem Thema wird der Microsoft Power BI-Inhalt **Istwert vs. Budget** beschrieben. Es erläutert, wie Sie auf die Power BI-Berichte zugreifen, und enthält Informationen zum Datenmodell und zu den Entitäten, die verwendet wurden, um den Inhalt zu erstellen.

## <a name="overview"></a>Übersicht

Der Power BI-Inhalt zu **Ist im Vergleich mit Budget** wurde für Personen erstellt, die für die Überwachung der tatsächlichen Leistung im Vergleich zur Budgetleistung in ihrer Organisation verantwortlich sind. Der Power BI-Inhalt zu **Ist im Vergleich mit Budget** bietet Einblicke in Budgetabweichungen. Sie können Budgets für das aktuelle Jahr nach Firmenkategorie, Budgetcode, Hauptkonto, Hauptkontobeschreibungen oder Finanzzeitraum analysieren, um ein besseres Verständnis für die Ursache von Abweichungen zu bekommen.

## <a name="accessing-the-power-bi-content"></a>Zugreifen auf den Power BI-Inhalt
Berichte vom Power BI-Inhalt zu **Ist im Vergleich mit Budget** werden in den Arbeitsbereichen **Sachkontobudget und Planungen** und **CFO** angezeigt.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Berichte, die im Power BI-Inhalt enthalten sind
Die folgende Tabelle enthält Details zur Metrik, die sich auf jeder Berichtsseite im Power BI-Inhalt zu **Ist im Vergleich mit Budget** befindet.

| Bericht                      | Metriken                                                                             |
|-----------------------------|-------------------------------------------------------------------------------------|
| Ausgaben – Istwert verglichen mit Budget | <ul><li>Diesjährige Gesamtausgaben</li><li>Diesjährige Budgetgesamtausgaben</li></ul>  |
| Umsatzerlös – Istwert im Vergleich zu Budget  | <ul><li>Diesjähriger Gesamtumsatz</li><li>Diesjähriger Budgetgesamtumsatz</li><ul>     |
| Spesen                     | <ul><li>Diesjährige Gesamtausgaben</li><li>Ziel der Ausgaben basierend auf Budget</li><ul> |
| Umsatzerlös                     | <ul><li>Diesjähriger Gesamtumsatz</li><li>Ziel der Umsatzerlöse basierend auf Budget</li><ul>   |
| Nettoeinkommen                  | <ul><li>Diesjähriges Nettoeinkommen</li><li>Ziel des Nettoeinkommens basierend auf Budget</li><ul>   |

## <a name="understanding-the-data-model-and-entities"></a>Das Datenmodells und die Entitäten verstehen

| Entität                    | Inhalt                                                                         |
|---------------------------|----------------------------------------------------------------------------------|
| Hauptbuchaktivitäten | Buchungsbeträge für das Hauptbuch                                       |
| Budgetaktivitäten         | Buchungsbeträge für das Budgetregister                                      |
| Hauptkonten             | Hauptkonten, nach denen Berichte gefiltert werden können                                               |
| Steuerkalender          | Steuerkalender, nach denen Berichte gefiltert werden können                                            |
| Sachkonten                   | Sachkonten, die verwendet werden können, um den Bericht nach dem aktuellen Sachkonto zu filtern              |
| Budgetcodes              | Budgetcodes, nach denen Berichte gefiltert werden können                                                |
| Juristische Personen            | Juristische Personen, die verwendet werden können, um nach der aktuellen juristischen Person zu filtern. |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]