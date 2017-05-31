---
title: Power BI-Inhalt des Practice Manager
description: "In diesem Thema wird beschrieben, was im Power Bl-Inhalt des Practice Manager enthalten ist. Es wird zudem beschrieben, wie das Dashboard und die Berichte, die im Inhaltspaket enthalten sind, verwendet werden und enthält Informationen zum Datenmodell und den Entitäten, die verwendet werden, um das Inhaltspaket zu erstellen."
author: knelson
manager: AnnBe
ms.date: 04/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer/IT Pro
ms.assetid: 
ms.search.region: Global
ms.author: knelson
ms.dyn365.intro: 2017/04/27
ms.dyn365.version: 
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 0f2a1a9df8e5036c60b74b8a710e606b0b1e312a
ms.contentlocale: de-de
ms.lasthandoff: 05/25/2017


---

# <a name="practice-manager-power-bi-content"></a>Power BI-Inhalt des Practice Manager

[!include[banner](../includes/banner.md)]


In diesem Thema wird beschrieben, was im Microsoft Power Bl-Inhalt des **Practice Manager** enthalten ist. Es wird erläutert, wie Sie auf die Power Bl-Berichte zugreifen und enthält Informationen zum Datenmodell und zu den Entitäten, die verwendet werden, um den Inhalt zu erstellen.

## <a name="overview"></a>Überblick

Der Power BI-Inhalt des **Practice Manager** wurde für Methodenmanager und Projektmanager erstellt. Er stellt Schlüsselmetrik bereit, die sich auf die Projekte bezieht, an denen die Organisation gerade arbeitet. Das Dashboard bietet eine Übersicht der Projekte und zugehörigen Debitoren. Ein Berichtsebenenfilter kann verwendet werden, um für bestimmte juristische Personen Meldung zu erteilen. Dieser Power BI-Inhalt bezieht Daten aus den aggregierten Messungen der Projektbuchhaltung für Microsoft Dynamics 365 for Operations.

Der Power BI-Inhalt des **Practice Manager** umfasst fünf Berichtsseiten: eine Übersichtsseite und vier Seiten, die Details zu Projektkosten, Umsatzerlösen, Ertragswertverwaltung und Stundenmetrik enthalten, die über unterschiedliche Dimensionen hinweg unterteilt und gewürfelt werden.

Alle Beträge im Inhalt werden in der Systemwährung angezeigt. Sie können die Systemwährung auf der Seite **Systemparameter** festlegen.

## <a name="accessing-the-power-bi-content"></a>Zugreifen au Power BI Inhalt

Sie finden den Power BI-Inhalt **Practice Manager** in der Bibliothek freigegebener Anlagen in Microsoft Dynamics Lifecycle Services (LCS). Weitere Informationen dazu, wie Sie das Inhaltspaket herunterladen und mit Ihren Microsoft Dynamics 365 for Operations-Daten verbinden, finden Sie unter [Power BI-Inhalt in LCS von Microsoft und Ihren Partnern](power-bi-content-microsoft-partners.md).

Um eine Vorführung anzusehen, die zeigt, wie der Power BI-Inhalt impementiert wird, zeigen Sie den Office Mix [Power BI-Inhalt von Microsoft und Ihren Partnern in Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) an.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Berichte, die im Power BI Inhalt enthalten sind

Die folgende Tabelle enthält Details zur Metrik, die sich auf jeder Berichtsseite im BI-Inhalt **Practice Manager** befinden.

| Berichtsseiten                                          | Metriken               |
|------------------------------------------------------|-----------------------------------------------|
| Dashboard  | Erstelltes Projekte<br>Vorkalkulierte Projekte<br>In Bearbeitung befindliche Projekte<br>Anzahl der Projekte nach Phase<br>Anzahl der Projekte nach Ort<br>Tatsächlicher Umsatz nach Debitor<br>Budgetbruttogewinn nach Projekt<br>Übersicht der Ertragswertverwaltung |
| Kosten                                                 | Istwert im Vergleich zu Budgetkosten nach Monat<br>Istwert im Vergleich zu Budgetkosten nach Jahr<br>Istwert im Vergleich mit Budgetkosten nach Kategorie<br>Istkosten nach Buchungstyp       |
| Umsatzerlös                                              | Tatsächlicher Umsatz nach Monat<br>Tatsächlicher Umsatz nach Postleitzahl<br>Istwert im Vergleich zu Budgetumsatz nach Kategorie<br>Tatsächlicher Umsatz nach Debitorenbranche        |
| EVM                                                  | Kosten- und Zeitplan-Leistungsindex nach Projekt                 |
| Stunden                                                | Tatsächliche fakturierbare verwendete Stunden im Vergleich zu tatsächlichen, fakturierbaren, nicht berechenbaren Stunden im Vergleich zu Budgetstunden<br>Tatsächliche, fakturierbare, verwendete Stunden im Vergleich zu tatsächlichen, fakturierbaren, nicht berechenbaren Stunden nach Projekt<br>Tatsächliche, fakturierbare, verwendete Stunden im Vergleich zu tatsächlichen, fakturierbaren, nicht berechenbaren Stunden nach Ressource<br>Verhältnis tatsächlicher, fakturierbarer Stunden nach Projekt<br>Verhältnis tatsächlicher, fakturierbarer Stunden nach Ressource |

Die Diagramme und die Kacheln auf allen diesen Berichten können gefiltert und an das Dashboard geheftet werden. Weitere Informationen dazu, wie Sie in Power BI filtern und anheften, finden Sie unter [Erstellen und Konfigurieren eines Dashboard](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards/). Sie können auch die Funktionen zum Export zugrunde liegender Daten verwenden, um die zugrunde liegenden Daten zu exportieren, die in einer Visualisierung zusammengefasst sind.

## <a name="understanding-the-data-model-and-entities"></a>Das Datenmodells und die Entitäten verstehen

Dynamics 365 for Operations-Daten werden verwenden, um die Berichtsseiten im Power BI-Inhalt des **Practice Manager** auszufüllen. Diese Daten werden als gesamte Messungen dargestellt, die im Entitätsshop bereitgestellt werden, der eine Microsoft SQL-Datenbank ist, die zwecks Analyse optimiert ist. Weitere Informationen finden Sie in der [Übersicht Power BI Integration mit Entitätsspeicher](power-bi-integration-entity-store.md).

In den folgenden Abschnitten werden die aggregierten Messungen, die in jeder Entität verwendet werden, erklärt.

### <a name="entity-projectaccountingcubeactualhourutilization"></a>Entität: ProjectAccountingCube_ActualHourUtilization
**Datenquelle**: ProjEmplTrans

| Zentrale aggregierte Messungen                | Feld                                | Beschreibung                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
| ActualBillableUtilizedHours              | Sum(ActualUtilizationBillableRate)   | Summe tatsächlich verwendeter, fakturierbarer Stunden |
| ActualBillableBurdenHours                | Sum(ActualBurdenBillableRate)        | Summe der tatsächlichen Belastungsrate             |

### <a name="entity-projectaccountingcubeactuals"></a>Entität: ProjectAccountingCube_Actuals
**Datenquelle**: ProjTransPosting

| Zentrale aggregierte Messungen                | Feld                                | Beschreibung                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
| ActualRevenue                            |     Sum(ActualRevenue)               |  Summe gebuchter Umsatzerlöse für alle Transaktionen |   
| ActualCost   |                             Sum(ActualCost)           |    Summe der gebuchten Kosten für alle Buchungsarten    |

### <a name="entity-projectaccountingcubecustomer"></a>Entität: ProjectAccountingCube_Customer
**Datenquelle**: CustTable

| Zentrale aggregierte Messungen                | Feld                                | Beschreibung                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
|    Anzahl von Projekten        |   COUNTA(ProjectAccountingCube_Projects[PROJECTS])       |         Anzahl verfügbarer Projekte    |


### <a name="entity-projectaccountingcubeforecasts"></a>Entität: ProjectAccountingCube_Forecasts
**Datenquelle**: ProjTransBudget

| Zentrale aggregierte Messungen                | Feld                                | Beschreibung                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
|    BudgetCost    |       Sum(BudgetCost)  |       Summe der geplanten Kosten für alle Buchungsarten     |
|     BudgetRevenue    |         Sum(BudgetRevenue)    |    Summe des geplanten, antizipierten/fakturierten Umsatzerlöses         |
|BudgetGrossMargin | Sum(BudgetGrossMargin) |Differenz zwischen Summe des gesamten geplanten Umsatzerlöses und Summe der gesamten geplanten Kosten

### <a name="entity-projectaccountingcubeprojectplancostsview"></a>Entität: ProjectAccountingCube_ProjectPlanCostsView
**Datenquelle**: Projekt

| Zentrale aggregierte Messungen                | Feld                                | Beschreibung                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
|      PlannedCost      |        Sum(SumOfTotalCostPrice)   | Gesamteinstandspreis in Vorkalkulationen für alle Projektbuchungsarten mit geplanten Aufgaben |

### <a name="entity-projectaccountingcubeprojects"></a>Entität: ProjectAccountingCube_Projects
**Datenquelle**: Projekt

| Zentrale aggregierte Messungen                | Feld                                | Beschreibung                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
|   Kostenleistungsindex  |ProjectAccountingCube_Projects[Earned value] / ProjectAccountingCube_Projects[Summe der Istkosten der abgeschlossenen Aufgaben] |     Berechnung das gesamte Ertragswerts geteilt durch die Summe der Istkosten|
|  Zeitplan-Leistungsindex |ProjectAccountingCube_Projects[Earned value] / ProjectAccountingCube_Projects[Summe der geplanten Kosten der abgeschlossenen Aufgaben]|Berechnung das gesamte Ertragswerts geteilt durch die Summe der geplanten Kosten |
|Prozentsatz der abgeschlossenen Arbeit |Prozentsatz der abgeschlossenen Arbeit = ProjectAccountingCube_Projects[Summe der Istkosten der abgeschlossenen Aufgaben] / (ProjectAccountingCube_Projects[Summe der tatsächlichen Kosten der abgeschlossenen Aufgaben] + ProjectAccountingCube_Projects[Gesamte geplante Kosten des Projekts] - ProjectAccountingCube_Projects[Gesamte geplante Kosten der abgeschlossenen Aufgaben])|Gesamtprozentsatz der abgeschlossenen Arbeit basierend auf der Summe der Istkosten der abgeschlossenen Aufgabe und der geplanten Kosten des Projekts|
|Verhältnis tatsächlicher fakturierbarer Stunden des Projekts|ProjectAccountingCube_Projects[Gesamte tatsächliche, fakturierbare, verwendete Stunden des Projekts] / (ProjectAccountingCube_Projects[Gesamte tatsächliche, fakturierbare, verwendete Stunden des Projekts] + ProjectAccountingCube_Projects[Gesamte tatsächliche, fakturierbare, nicht berechenbare Stunden des Projekts])|Summe tatsächlicher, fakturierbarer Stunden, basierend auf nicht verwendeten und nicht berechenbaren Stunden|
|Ertragswert|ProjectAccountingCube_Projects[Gesamte geplante Kosten des Projekts] * ProjectAccountingCube_Projects[Prozentsatz der abgeschlossenen Arbeit]|Gesamte geplante Kosten multipliziert mit dem Prozentsatz der abgeschlossenen Arbeit|

### <a name="entity-projectaccountingcubetotalestimatedcosts"></a>Entität: ProjectAccountingCube_TotalEstimatedCosts 
**Datenquelle**: ProjTable

| Zentrale aggregierte Messungen                | Feld                                | Beschreibung                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
| CompletedActivityPlannedCost  |  Sum(TotalCostPrice)  |   Gesamteinstandspreis in Vorkalkulationen für alle Projektbuchungsarten mit abgeschlossenen Aufgaben|

## <a name="additional-resources"></a>Zusätzliche Ressourcen

Nachfolgend finden Sie einige hilfreiche Links zum Thema Entitäten und Erstellen von Power BI-Inhalten:

- [Datenentitäten](/dynamics365/operations/dev-itpro/data-entities/data-entities)
- [Erstellen von Organisations-Inhaltspaketen](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
- [Datenmodellierung mithilfe von Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
- [Power BI-Integration für Arbeitsbereiche konfigurieren](configure-power-bi-integration.md)

