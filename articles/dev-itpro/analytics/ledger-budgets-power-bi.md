---
title: Power BI-Inhalt zu Ist im Vergleich mit Budget
description: In diesem Thema wird der Power BI-Inhalt zu Ist im Vergleich mit Budget beschrieben. Es wird beschrieben, wie auf die Berichte, die im Inhalt enthalten sind, zugegriffen wird und es werden Informationen zum Datenmodell und den Entitäten bereitgestellt, die zum Erstellen des Inhalts verwendet wurden.
author: ryansandness
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetTrackingWorkspace
audience: Application user, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: a577ab24aaf86c1f7a22953e03f397a2e8213c78
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/02/2019
ms.locfileid: "1849430"
---
# <a name="actual-vs-budget-power-bi-content"></a>Power BI-Inhalt zu Ist im Vergleich mit Budget

[!include [banner](../includes/banner.md)]

In diesem Thema wird der Power BI-Inhalt zu **Ist im Vergleich mit Budget** beschrieben. Es erläutert, wie Sie auf die Power BI-Berichte zugreifen, und enthält Informationen zum Datenmodell und zu den Entitäten, die verwendet wurden, um den Inhalt zu erstellen.

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
