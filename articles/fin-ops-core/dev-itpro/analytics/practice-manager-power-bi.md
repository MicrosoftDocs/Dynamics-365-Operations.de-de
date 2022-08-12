---
title: Power BI-Inhalt – Practice Manager
description: In diesem Artikel wird beschrieben, was im Power BI-Inhalt – Practice Manager enthalten ist.
author: sericks007
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.assetid: ''
ms.search.form: ProjManagementWorkspace
ms.openlocfilehash: 92c2881c89da0b23e3a66c0f8bbcafd91c38c6e3
ms.sourcegitcommit: 3c4dd125ed321af8a983e89bcb5bd6e5ed04a762
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/28/2022
ms.locfileid: "9206503"
---
# <a name="practice-manager-power-bi-content"></a>Power BI-Inhalt – Practice Manager

[!include [banner](../includes/banner.md)]

In diesem Artikel wird beschrieben, was im Microsoft Power BI-Inhalt – **Practice Manager** enthalten ist. Es erläutert, wie Sie auf die Power BI-Berichte zugreifen und enthält Informationen zum Datenmodell und zu den Entitäten, die verwendet werden, um den Inhalt zu erstellen.

## <a name="overview"></a>Übersicht

Der Power BI-Inhalt – **Practice Manager** wurde für Methodenmanager und Projektmanager erstellt. Er stellt Schlüsselmetrik bereit, die sich auf die Projekte bezieht, an denen die Organisation gerade arbeitet. Das Dashboard bietet eine Übersicht der Projekte und zugehörigen Debitoren. Ein Berichtsebenenfilter kann verwendet werden, um für bestimmte juristische Personen Meldung zu erteilen. Dieses Power BI-Inhalt extrahiert Daten aus aggregierenden Messungen der Projektbuchhaltung.

Der Power BI-Inhalt – **Practice Manager** umfasst fünf Berichtsseiten: eine Übersichtsseite und vier Seiten, die Details zu Projektkosten, Umsatzerlösen, Ertragswertverwaltung und Stundenmetrik enthalten, die über unterschiedliche Dimensionen hinweg unterteilt sind.

Alle Beträge im Inhalt werden in der Systemwährung angezeigt. Sie können die Systemwährung auf der Seite **Systemparameter** festlegen.

## <a name="accessing-the-power-bi-content"></a>Zugreifen auf den Power BI-Inhalt

Der Power BI-Inhalt – **Practice Manager** wird im **Projektmanagement**-Arbeitsbereich angezeigt.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Berichte, die im Power BI-Inhalt enthalten sind

Die folgende Tabelle enthält Details zur Metrik, die sich auf jeder Berichtsseite im Power BI-Inhalt – **Practice Manager** befinden.

| Berichtsseiten       | Metriken |
|-------------------|---------|
| Projektüberblick | <ul><li>Erstelltes Projekte</li><li>Vorkalkulierte Projekte</li><li>In Bearbeitung befindliche Projekte</li><li>Tatsächlicher Umsatz nach Debitor</li><li>Budgetbruttogewinn nach Projekt</li><li>Übersicht der Ertragswertverwaltung</li></ul> |
| Kosten              | <ul><li>Istwert im Vergleich zu Budgetkosten nach Monat</li><li>Istwert im Vergleich zu Budgetkosten nach Jahr</li><li>Istwert im Vergleich zu Budgetkosten nach Kategorie</li><li>Istkosten nach Buchungstyp</li></ul> |
| Umsatzerlös           | <ul><li>Tatsächlicher Umsatz nach Monat</li><li>Tatsächlicher Umsatz nach Postleitzahl</li><li>Istwert im Vergleich zu Budgetumsatz nach Kategorie</li><li>Tatsächlicher Umsatz nach Debitorenbranche</li></ul> |
| EVM               | Kosten- und Zeitplan-Leistungsindex nach Projekt |
| Stunden             | <ul><li>Tatsächliche fakturierbare verwendete Stunden im Vergleich zu tatsächlichen, fakturierbaren, nicht berechenbaren Stunden im Vergleich zu Budgetstunden</li><li>Tatsächliche, fakturierbare, verwendete Stunden im Vergleich zu tatsächlichen, fakturierbaren, nicht berechenbaren Stunden nach Projekt</li><li>Tatsächliche, fakturierbare, verwendete Stunden im Vergleich zu tatsächlichen, fakturierbaren, nicht berechenbaren Stunden nach Ressource</li><li>Verhältnis tatsächlicher, fakturierbarer Stunden nach Projekt</li><li>Verhältnis tatsächlicher, fakturierbarer Stunden nach Ressource</li></ul> |

Die Diagramme und die Kacheln auf allen diesen Berichten können gefiltert und an das Dashboard geheftet werden. Weitere Informationen dazu, wie Sie in Power BI filtern und anheften, finden Sie unter [Erstellen und Konfigurieren eines Dashboard](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards/). Sie können auch die Funktionen zum Export zugrunde liegender Daten verwenden, um die zugrunde liegenden Daten zu exportieren, die in einer Visualisierung zusammengefasst sind.

## <a name="understanding-the-data-model-and-entities"></a>Das Datenmodells und die Entitäten verstehen

Die folgenden Daten werden verwendet, um die Berichtsseiten im Power BI-Inhalt – **Practice Manager** auszufüllen. Diese Daten werden als gesamte Messungen dargestellt, die im Entitätsshop bereitgestellt werden. Der Entitätsshop ist eine Microsoft SQL Server-Datenbank, die für die Analyse optimiert ist. Weitere Informationen finden Sie unter [Power BI Integration mit Entity Store](power-bi-integration-entity-store.md).

In den folgenden Abschnitten werden die aggregierten Messungen, die in jeder Entität verwendet werden, beschrieben.

### <a name="entity-projectaccountingcube_actualhourutilization"></a>Entität: ProjectAccountingCube\_ActualHourUtilization
**Datenquelle:** ProjEmplTrans

| Zentrale aggregierte Messungen      | Feld                              | Beschreibung |
|--------------------------------|------------------------------------|-------------|
| Tatsächlich berechenbar - Auslastungsstunden | Sum(ActualUtilizationBillableRate) | Die Gesamtsumme tatsächlich verwendeter, fakturierbarer Stunden. |
| Tatsächlich berechenbar - Nicht berechenbare Stunden   | Sum(ActualBurdenBillableRate)      | Die Gesamtsumme der tatsächlichen Belastungsrate. |

### <a name="entity-projectaccountingcube_actuals"></a>Entität: ProjectAccountingCube\_Actuals
**Datenquelle:** ProjTransPosting

| Zentrale aggregierte Messungen | Feld              | Beschreibung |
|---------------------------|--------------------|-------------|
| Tatsächlicher Umsatzerlös            | Sum(ActualRevenue) | Die Gesamtsumme gebuchter Umsatzerlöse für alle Buchungen. |
| Istkosten               | Sum(ActualCost)    | Die Gesamtsumme der gebuchten Kosten für alle Buchungsarten. |

### <a name="entity-projectaccountingcube_customer"></a>Entität: ProjectAccountingCube\_Customer
**Datenquelle:** CustTable

| Zentrale aggregierte Messungen | Feld                                             | Beschreibung |
|---------------------------|---------------------------------------------------|-------------|
| Anzahl von Projekten        | COUNTA(ProjectAccountingCube\_Projects\[PROJEKTE\]) | Die Anzahl verfügbarer Projekte. |

### <a name="entity-projectaccountingcube_forecasts"></a>Entität: ProjectAccountingCube\_Forecasts
**Datenquelle:** ProjTransBudget

| Zentrale aggregierte Messungen | Feld                  | Beschreibung |
|---------------------------|------------------------|-------------|
| Budgetkosten               | Sum(BudgetCost)        | Die Gesamtsumme der geplanten Kosten für alle Buchungsarten. |
| Umsatzerlös gemäß Budget            | Sum(BudgetRevenue)     | Die Gesamtsumme des geplanten, antizipierten/fakturierten Umsatzerlöses. |
| Bruttogewinn gemäß Budget       | Sum(BudgetGrossMargin) | Die Differenz zwischen der Gesamtsumme des geplanten Umsatzerlöses und die Summe der gesamten geplanten Kosten. |

### <a name="entity-projectaccountingcube_projectplancostsview"></a>Entität: ProjectAccountingCube\_ProjectPlanCostsView
**Datenquelle:** Projekt

| Zentrale aggregierte Messungen | Feld                    | Beschreibung |
|---------------------------|--------------------------|-------------|
| Geplante Kosten              | Sum(SumOfTotalCostPrice) | Der Gesamteinstandspreis in Vorkalkulationen für alle Projektbuchungsarten mit geplanten Aufgaben. |

### <a name="entity-projectaccountingcube_projects"></a>Entität: ProjectAccountingCube\_Projects
**Datenquelle:** Projekt

| Zentrale aggregierte Messungen    | Feld | Beschreibung |
|------------------------------|-------|-------------|
| Kostenleistungsindex       | ProjectAccountingCube\_Projects\[Ertragswert\] ÷ ProjectAccountingCube\_Projects\[Gesamte Istkosten der abgeschlossenen Aufgaben\] | Die Berechnung das gesamte Ertragswerts geteilt durch die Summe der Istkosten. |
| Zeitplan-Leistungsindex   | ProjectAccountingCube\_Projects\[Ertragswert\] ÷ ProjectAccountingCubeProjects\_\[Gesamte geplante Kosten der abgeschlossenen Aufgaben\] | Die Berechnung das gesamte Ertragswerts geteilt durch die Summe der geplanten Istkosten. |
| Prozentsatz der abgeschlossenen Arbeit | Prozentsatz der abgeschlossenen Arbeit = ProjectAccountingCube\_Projects\[Summe der Istkosten der abgeschlossenen Aufgaben\] ÷ (ProjectAccountingCube\_Projects\[Summe der tatsächlichen Kosten der abgeschlossenen Aufgaben\] + ProjectAccountingCube\_Projects\[Gesamte geplante Kosten des Projekts\] – ProjectAccountingCube\_Projects\[Gesamte geplante Kosten der abgeschlossenen Aufgaben\]) | Der Gesamtprozentsatz der abgeschlossenen Arbeit basierend auf der Gesamtsumme der Istkosten der abgeschlossenen Aufgaben und der geplanten Kosten des Projekts. |
| Tatsächliches Verhältnis berechenbarer Stunden  | ProjectAccountingCube\_Projects\[Gesamte tatsächliche, fakturierbare, nicht berechenbare Stunden des Projekts\] ÷ (ProjectAccountingCube\_\[Gesamte tatsächliche, fakturierbare, nicht berechenbare Stunden des Projekts\] + ProjectAccountingCube\_+ Projects\[Gesamte tatsächliche, fakturierbare, nicht berechenbare Stunden des Projekts\]) | Die gesamten tatsächlichen berechenbaren Stunden basierend auf den verwendeten und nicht berechenbaren Stunden. |
| Ertragswert                 | ProjectAccountingCube\_Projects\[Gesamte geplante Kosten des Projekts\] × ProjectAccountingCube\_Projects\[Prozentsatz der abgeschlossenen Arbeit\] | Die gesamten geplanten Kosten multipliziert mit dem Prozentsatz der abgeschlossenen Arbeit. |

### <a name="entity-projectaccountingcube_totalestimatedcosts"></a>Entität: ProjectAccountingCube\_TotalEstimatedCosts 
**Datenquelle:** ProjTable

| Zentrale aggregierte Messungen       | Feld               | Beschreibung |
|---------------------------------|---------------------|-------------|
| Geplante Kosten für abgeschlossene Aktivität | Sum(TotalCostPrice) | Der Gesamteinstandspreis in Vorkalkulationen für alle Projektbuchungsarten mit abgeschlossenen Aufgaben. |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
