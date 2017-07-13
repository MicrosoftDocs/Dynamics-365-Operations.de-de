---
title: Power BI-Inhalt des Practice Manager
description: "In diesem Thema wird beschrieben, was im Power Bl-Inhalt des Practice Manager enthalten ist. Es wird beschrieben, wie auf die Berichte, die im Inhalt enthalten sind, zugegriffen wird und es werden Informationen zum Datenmodell und den Entitäten bereitgestellt, die zum Erstellen des Inhalts verwendet werden."
author: KimANelson
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Core, Operations, UnifiedOperations
ms.assetid: 
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-06-30
ms.dyn365.version: Enterprise edition, July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 993e88703f19dbeec435d07a4599cbbfcda563bc
ms.openlocfilehash: b63e31f3e4993c1fda229a54b4e5ef2fed824355
ms.contentlocale: de-de
ms.lasthandoff: 06/20/2017


---

# <a name="practice-manager-power-bi-content"></a>Power BI-Inhalt des Practice Manager

[!include[banner](../includes/banner.md)]

In diesem Thema wird beschrieben, was im Microsoft Power Bl-Inhalt des **Practice Manager** enthalten ist. Es wird erläutert, wie Sie auf die Power Bl-Berichte zugreifen und enthält Informationen zum Datenmodell und zu den Entitäten, die verwendet werden, um den Inhalt zu erstellen.

## <a name="overview"></a>Überblick

Der Power BI-Inhalt des **Practice Manager** wurde für Methodenmanager und Projektmanager erstellt. Er stellt Schlüsselmetrik bereit, die sich auf die Projekte bezieht, an denen die Organisation gerade arbeitet. Das Dashboard bietet eine Übersicht der Projekte und zugehörigen Debitoren. Ein Berichtsebenenfilter kann verwendet werden, um für bestimmte juristische Personen Meldung zu erteilen. Dieses Power BI Inhalt extrahiert Daten aus aggregierten Messungen der Projektbuchhaltung.

Der Power BI-Inhalt des **Practice Manager** umfasst fünf Berichtsseiten: eine Übersichtsseite und vier Seiten, die Details zu Projektkosten, Umsatzerlösen, Ertragswertverwaltung und Stundenmetrik enthalten, die über unterschiedliche Dimensionen hinweg unterteilt sind.

Alle Beträge im Inhalt werden in der Systemwährung angezeigt. Sie können die Systemwährung auf der Seite **Systemparameter** festlegen.

## <a name="accessing-the-power-bi-content"></a>Zugreifen au Power BI Inhalt
Wenn Sie das Update für Juli 2017 von Microsoft Dynamics 365 for Finance and Operations, Enterprise-Edition, verwenden, wird der Power BI-Inhalt **Practice Manager** im Arbeitsbereich **Projektverwaltung** angezeigt.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Berichte, die im Power BI Inhalt enthalten sind

Die folgende Tabelle enthält Details zur Metrik, die sich auf jeder Berichtsseite im BI-Inhalt **Practice Manager** befinden.

| Berichtsseiten       | Metriken |
|-------------------|---------|
| Projektüberblick | <ul><li>Erstelltes Projekte</li><li>Vorkalkulierte Projekte</li><li>In Bearbeitung befindliche Projekte</li><li>Anzahl der Projekte nach Phase</li><li>Anzahl der Projekte nach Ort</li><li>Tatsächlicher Umsatz nach Debitor</li><li>Budgetbruttogewinn nach Projekt</li><li>Übersicht der Ertragswertverwaltung</li></ul> |
| Kosten              | <ul><li>Istwert im Vergleich zu Budgetkosten nach Monat</li><li>Istwert im Vergleich zu Budgetkosten nach Jahr</li><li>Istwert im Vergleich zu Budgetkosten nach Kategorie</li><li>Istkosten nach Buchungstyp</li></ul> |
| Umsatzerlös           | <ul><li>Tatsächlicher Umsatz nach Monat</li><li>Tatsächlicher Umsatz nach Postleitzahl</li><li>Istwert im Vergleich zu Budgetumsatz nach Kategorie</li><li>Tatsächlicher Umsatz nach Debitorenbranche</li></ul> |
| EVM               | Kosten- und Zeitplan-Leistungsindex nach Projekt |
| Stunden             | <ul><li>Tatsächliche fakturierbare verwendete Stunden im Vergleich zu tatsächlichen, fakturierbaren, nicht berechenbaren Stunden im Vergleich zu Budgetstunden</li><li>Tatsächliche, fakturierbare, verwendete Stunden im Vergleich zu tatsächlichen, fakturierbaren, nicht berechenbaren Stunden nach Projekt</li><li>Tatsächliche, fakturierbare, verwendete Stunden im Vergleich zu tatsächlichen, fakturierbaren, nicht berechenbaren Stunden nach Ressource</li><li>Verhältnis tatsächlicher, fakturierbarer Stunden nach Projekt</li><li>Verhältnis tatsächlicher, fakturierbarer Stunden nach Ressource</li></ul> |

Die Diagramme und die Kacheln auf allen diesen Berichten können gefiltert und an das Dashboard geheftet werden. Weitere Informationen dazu, wie Sie in Power BI filtern und anheften, finden Sie unter [Erstellen und Konfigurieren eines Dashboard](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards/). Sie können auch die Funktionen zum Export zugrunde liegender Daten verwenden, um die zugrunde liegenden Daten zu exportieren, die in einer Visualisierung zusammengefasst sind.

## <a name="extending-the-power-bi-content"></a>Erweitern des Power BI-Inhalts
Wenn Sie die Inhaltspakete verwenden, die in Microsoft Dynamics Lifecycle Services (LCS) verfügbar sind, können Sie großartige Analysen für Person bereitstellen, die sich nicht in Microsoft Dynamics 365 anmelden. Sie können diese Inhaltspakete so ändern, dass sie andere Berichte oder grafische Elemente umfassen, und diese dann für die Analyse auf Ihrem Power BI.com-Mandanten veröffentlichen. 

Sie können den **Practice Manager**-Power BI-Inhalt in der freigebenen Anlagenbibliothek in LCS finden. Weitere Informationen dazu, wie Sie Power BI-Inhalte herunterladen und in Ihrer Organisation implementieren, finden Sie unter [Power BI-Inhalt in LCS von Microsoft und Ihren Partnern](power-bi-content-microsoft-partners.md). Um eine Vorführung anzusehen, die zeigt, wie der Power BI-Inhalt impementiert wird, zeigen Sie den Office Mix [Power BI-Inhalt von Microsoft und Ihren Partnern in Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) an.

Stellen Sie sicher, dass Sie den **Practice Manager**-Inhalt herunterladen, der der von Ihnen verwendeten Dynamics 365-Version entspricht.

## <a name="understanding-the-data-model-and-entities"></a>Das Datenmodells und die Entitäten verstehen

Die folgenden Daten werden verwendet, um die Berichtsseiten im Power BI-Inhalt **Practice Manager** auszufüllen. Diese Daten werden als gesamte Messungen dargestellt, die im Entitätsshop bereitgestellt werden. Der Entitätsshop ist eine Microsoft SQL Server-Datenbank, die zwecks Analyse optimiert ist. Weitere Informationen finden Sie in der [Übersicht Power BI Integration mit Entitätsspeicher](power-bi-integration-entity-store.md).

In den folgenden Abschnitten werden die aggregierten Messungen, die in jeder Entität verwendet werden, beschrieben.

### <a name="entity-projectaccountingcubeactualhourutilization"></a>Entität: ProjectAccountingCube_ActualHourUtilization
**Datenquelle:** ProjEmplTrans

| Zentrale aggregierte Messungen      | Feld                              | Beschreibung | 
|--------------------------------|------------------------------------|-------------|
| Tatsächlich berechenbar - Auslastungsstunden | Sum(ActualUtilizationBillableRate) | Die Gesamtsumme tatsächlich verwendeter, fakturierbarer Stunden. |
| Tatsächlich berechenbar - Nicht berechenbare Stunden   | Sum(ActualBurdenBillableRate)      | Die Gesamtsumme der tatsächlichen Belastungsrate. |

### <a name="entity-projectaccountingcubeactuals"></a>Entität: ProjectAccountingCube_Actuals
**Datenquelle:** ProjTransPosting

| Zentrale aggregierte Messungen | Feld              | Beschreibung | 
|---------------------------|--------------------|-------------|
| Tatsächlicher Umsatzerlös            | Sum(ActualRevenue) | Die Gesamtsumme gebuchter Umsatzerlöse für alle Buchungen. |   
| Istkosten               | Sum(ActualCost)    | Die Gesamtsumme der gebuchten Kosten für alle Buchungsarten. |

### <a name="entity-projectaccountingcubecustomer"></a>Entität: ProjectAccountingCube_Customer
**Datenquelle:** CustTable

| Zentrale aggregierte Messungen | Feld                                            | Beschreibung | 
|---------------------------|--------------------------------------------------|-------------|
| Anzahl von Projekten        | COUNTA(ProjectAccountingCube_Projects[PROJECTS]) | Die Anzahl verfügbarer Projekte. |


### <a name="entity-projectaccountingcubeforecasts"></a>Entität: ProjectAccountingCube_Forecasts
**Datenquelle:** ProjTransBudget

| Zentrale aggregierte Messungen | Feld                  | Beschreibung | 
|---------------------------|------------------------|-------------|
| Budgetkosten               | Sum(BudgetCost)        | Die Gesamtsumme der geplanten Kosten für alle Buchungsarten. |
| Umsatzerlös gemäß Budget            | Sum(BudgetRevenue)     | Die Gesamtsumme des geplanten, antizipierten/fakturierten Umsatzerlöses.  |
| Bruttogewinn gemäß Budget       | Sum(BudgetGrossMargin) | Die Differenz zwischen der Gesamtsumme des geplanten Umsatzerlöses und die Summe der gesamten geplanten Kosten. |

### <a name="entity-projectaccountingcubeprojectplancostsview"></a>Entität: ProjectAccountingCube_ProjectPlanCostsView
**Datenquelle:** Projekt

| Zentrale aggregierte Messungen | Feld                    | Beschreibung | 
|---------------------------|--------------------------|-------------|
| Geplante Kosten              | Sum(SumOfTotalCostPrice) | Der Gesamteinstandspreis in Vorkalkulationen für alle Projektbuchungsarten mit geplanten Aufgaben. |

### <a name="entity-projectaccountingcubeprojects"></a>Entität: ProjectAccountingCube_Projects
**Datenquelle:** Projekt

| Zentrale aggregierte Messungen    | Feld | Beschreibung | 
|------------------------------|-------|-------------|
| Kostenleistungsindex       | ProjectAccountingCube_Projects[Earned value] / ProjectAccountingCube_Projects[Summe der Istkosten der abgeschlossenen Aufgaben] | Die Berechnung das gesamte Ertragswerts geteilt durch die Summe der Istkosten. |
| Zeitplan-Leistungsindex   | ProjectAccountingCube_Projects[Earned value] / ProjectAccountingCube_Projects[Summe der geplanten Kosten der abgeschlossenen Aufgaben] | Die Berechnung das gesamte Ertragswerts geteilt durch die Summe der geplanten Istkosten. |
| Prozentsatz der abgeschlossenen Arbeit | Prozentsatz der abgeschlossenen Arbeit = ProjectAccountingCube_Projects[Summe der Istkosten der abgeschlossenen Aufgaben] / (ProjectAccountingCube_Projects[Summe der tatsächlichen Kosten der abgeschlossenen Aufgaben] + ProjectAccountingCube_Projects[Gesamte geplante Kosten des Projekts] - ProjectAccountingCube_Projects[Gesamte geplante Kosten der abgeschlossenen Aufgaben]) | Der Gesamtprozentsatz der abgeschlossenen Arbeit basierend auf der Gesamtsumme der Istkosten der abgeschlossenen Aufgaben und der geplanten Kosten des Projekts. |
| Tatsächliches Verhältnis berechenbarer Stunden  | ProjectAccountingCube_Projects[Gesamte tatsächliche, fakturierbare, verwendete Stunden des Projekts] / (ProjectAccountingCube_Projects[Gesamte tatsächliche, fakturierbare, verwendete Stunden des Projekts] + ProjectAccountingCube_Projects[Gesamte tatsächliche, fakturierbare, nicht berechenbare Stunden des Projekts]) | Die gesamten tatsächlichen berechenbaren Stunden basierend auf den verwendeten und nicht berechenbaren Stunden. |
| Ertragswert                 | ProjectAccountingCube_Projects[Gesamte geplante Kosten des Projekts] * ProjectAccountingCube_Projects[Prozentsatz der abgeschlossenen Arbeit] | Die gesamten geplanten Kosten multipliziert mit dem Prozentsatz der abgeschlossenen Arbeit. |

### <a name="entity-projectaccountingcubetotalestimatedcosts"></a>Entität: ProjectAccountingCube_TotalEstimatedCosts 
**Datenquelle:** ProjTable

| Zentrale aggregierte Messungen       | Feld               | Beschreibung | 
|---------------------------------|---------------------|-------------|
| Geplante Kosten für abgeschlossene Aktivität | Sum(TotalCostPrice) | Der Gesamteinstandspreis in Vorkalkulationen für alle Projektbuchungsarten mit abgeschlossenen Aufgaben. |

