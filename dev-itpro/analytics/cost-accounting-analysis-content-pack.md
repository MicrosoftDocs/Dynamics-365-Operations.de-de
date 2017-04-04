---
title: "Kostenrechnungsanalyse Leistungsfähigkeit BIinhalt"
description: "In diesem Thema wird beschrieben, was im Kostenrechnungsanalyse Leistungsfähigkeit BIinhalt enthalten ist. Es wird erläutert, wie Sie die Leistungsfähigkeit BIberichte zugreift und enthält Informationen zum Datenmodell und die Entitäten, die verwendet wurde, um den Inhalt zu erstellen."
author: YuyuScheller
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 270274
ms.assetid: b74549df-35d5-4f2f-b3c7-405b0d38ea78
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 50e7bd92ee693f59fd013226aee22bd1a54c81e2
ms.lasthandoff: 03/31/2017


---

# <a name="cost-accounting-analysis-power-bi-content"></a>Kostenrechnungsanalyse Leistungsfähigkeit BIinhalt

In diesem Thema wird beschrieben, was im Kostenrechnungsanalyse Leistungsfähigkeit BIinhalt enthalten ist. Es wird erläutert, wie Sie die Leistungsfähigkeit BIberichte zugreift und enthält Informationen zum Datenmodell und die Entitäten, die verwendet wurde, um den Inhalt zu erstellen.

<a name="overview"></a>Überblick
--------

** Der Kostenrechnungsanalyse ** Microsoft-Energie wird für BIinhalt Controller oder alle Kosten bestimmt, der für die Ausführung der Kostensteuerung eine Organisation verantwortlich ist. Er umfasst die Schlüsselindikatoren, wie Kosten, Größe und Verrechnungssatz von Istkosten, Budgetkost und flexible Budgetkosten ein. Er verwendet Buchungsdaten aus der Kostenrechnung in Microsoft Dynamics 365 für Arbeitsgänge und stellt eine gesamte Ansicht von Kosten für die gesamte Organisation in einer Berichtswährung bereit. Manager können die Daten filtern, um nach Kostenträger der Kostensteuerung Organisationseinheiten auszuführen, wenn die Organisation mehrere juristische Personen haben kann. Da der Kostenrechnungsanalyse ** ** Leistungsfähigkeit BIinhalt Abweichungen zwischen den Istkosten und den budgetierten Kosten hervorhebt, können Manager über die positiven und negativen Trends für ihre Einsatzkräfte informiert werden. Manager können zu den Kostenfaktorhierarchien oder den einzelnen Kostenfaktoren navigieren, verschaffen des in detaillierten Einblickes, wie Kostenabweichungen aufgetreten sind, und von wirksamer Maßnahme dann ausgeführt werden. ** Der Kostenrechnungsanalyse ** Leistungsfähigkeit BIinhalt ermöglicht Buchhalter Kosten analysieren, wie Kosten die Kostenträger der gesamten Organisation. durchfließen Weitere Informationen zur Kostenrechnung zu ermitteln, finden Sie Kostenrechnungsstartseite [] (- /dynamics365/operations/financials/costbuchhaltung/Kostenrechnung - home-page.md ). Wenn Sie ZugriffEbenensicherheit in der Kostenrechnung festgelegt haben und mit Sicherheit auf Positionsebene Leistung in BI kombinieren, können Sie alle Kostenträgereigentümern Zugriff auf Kostenrechnungsanalyse ** ** Leistungsfähigkeit BIinhalt gewähren. Alle Daten in den Visualisierungen werden anschließend auf Basis die Zugriffsebene gefiltert, die in der Kostenrechnung gesteuert wird. Weitere Informationen zu ZugriffEbenensicherheit und Sicherheit zu ermitteln auf Positionsebene, [für Sicherheit finden Sie Kostenrechnungsinhalt für Leistung BI] (setup-security-cost-accounting-content-pack.md) einrichten.

## <a name="accessing-the-power-bi-content"></a>Zugreifen Leistung des BIinhalts
Sie können den Kostenrechnungsanalyse ** ** Leistungsfähigkeit BIinhalt in der Bibliothek der kommenden Anlagen in den Microsoft Dynamics Lifecycle Services (LCS) suchen. Weitere Informationen dazu, wie der Inhalt herunterlädt und diesen für Ihr Dynamics 365 für Arbeitsgänge, Daten finden Sie in BIinhalt herstellt [Energie Kreditbriefen von Microsoft und von den Partnern]( power-bi-content-microsoft-partners.md). ** Hinweis: ** KB4011327 ** ** ist eine Voraussetzung für den Kostenrechnungsanalyse ** ** Leistungsfähigkeit BIinhalt.  Nachdem Sie in Lebenszyklus-Dienstleistungen signieren, können Sie hier das KB zugreifen: <https://fix.lcs.dynamics.com/issue/results/?q=kb4011327>.

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Metrik, das im BIinhalt Energie enthalten sind
Der Inhalt enthält einen Satz Berichtsseiten. Jede Seite enthält einen Satz Metriken, das als Diagramme, Kacheln und Tabellen visuell dargestellt werden. Die folgende Tabelle enthält eine Übersicht der im Kostenrechnungsanalyse Visualisierungen ** ** Leistungsfähigkeit BIinhalt.

| Berichtsseite                      | Diagramm                                                                                                                         | Kachel                                          |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| Kostenkontrolle nach Finanzzeitraum    | Istkosten und Budgetkost nach Kostenfaktorhierarchieebene                                                                   | Istkosten im Vergleich Budgetkost                    |
|                                  | Planabweichung nach Kostenfaktorhierarchieebene                                                                               | Istkostensatz für Budgetkostsatz          |
|                                  | Liste der ersten 10 Debitoren Planabweichung in Prozent von Ausgaben                                                                          | Tatsächliche Größe für Budgetgröße          |
| Kostenkontrolle nach Seit Jahresbeginn     | Istkosten und Budgetkost nach Kalenderjahrs-Periode                                                                           | Istkosten im Vergleich Budgetkost                    |
|                                  | Planabweichung nach Kalenderjahrs-Periode                                                                                       | Istkostensatz für Budgetkostsatz          |
|                                  | Liste der ersten 10 Debitoren Planabweichung in Prozent von Ausgaben                                                                          | Tatsächliche Größe für Budgetgröße          |
| Verrechnungssatz nach Geschäftsjahr         | Verhalten Istkostensatz von Kosten                                                                                             | Istkostensatz für Budgetkostsatz          |
|                                  | Istkostensatz, Budgetkostsatzabweichung, Budgetkostsatzprozentsatz und Budgetkost bewerten nach Kostenfaktorhierarchieebene | Tatsächliche Größe für Budgetgröße          |
|                                  | Planabweichung nach Kostenfaktorhierarchieebene                                                                               |                                               |
|                                  | Liste der ersten 10 Debitoren Planabweichung in Prozent von Ausgaben                                                                          |                                               |
| Flexibles Budget nach Finanzzeitraum | Istkosten, und Budgetkost flexibles Budget nach Kostenfaktorhierarchieebene im                                             | Tatsächliche Größe für Budgetgröße          |
|                                  | Planabweichung und Variante des flexiblen Budgets nach Kostenfaktorhierarchieebene                                                  | Istkosten mit flexiblen Budgetkosten           |
|                                  | Istkosten, Budgetkost und flexible Kosten nach Verhalten Kosten und Kostenfaktorhierarchieebene                                  | Istkostensatz anhand Verrechnungssatz für flexible Budgets |
| Kostenaufstellung nach Finanzzeitraum  | Istkosten nach Kostenfaktorhierarchieebenen- und Kostenträgerdimensionsmitgliedsnamen                                             |                                               |
|                                  | Istkosten nach Mitgliedsnamen des Kostenträgerdimensionsmitgliedsnamens und der Kostenfaktordimension                                       |                                               |

## <a name="understanding-the-data-model-and-entities"></a>Das Datenmodells und die Entitäten verstehen
Dynamics 365 für Arbeitsgangsdaten wird verwendet, um in der Berichtsseiten ** Kostenrechnungsanalyse ** Leistungsfähigkeit BIinhalt auszufüllen. Diese Daten werden als gesamte Messungen dargestellt, die im Entitätsshop bereitgestellt werden, der eine Microsoft SQL-Datenbank ist, die zwecks Analyse optimiert ist. Weitere Informationen finden Sie in der Übersicht [Power BI-Integration mit Entitätsshop] (power-bi-integration-entity-store.md ). Die folgenden Schlüsselaggregatsmessungen werden als Grundlage des Inhalts verwendet.

| Entität                  | Gesamte Messung des Schlüssels | Datenquelle für Dynamics 365 für Arbeitsgänge | Feld     | Beschreibung                                   |
|-------------------------|---------------------------|---------------------------------------------|-----------|-----------------------------------------------|
| Kostenrechnungseinträge | SUMME (Betrag)               | CAMDATAAggregatedCostEntry                  | Betrag    | Betrag in der Kostenrechnungssachkontowährung |
| Statistische Einträge     | SUMME (Größe)            | CAMDATAAggregatedStatisctialEntry           | Größe |                                               |

Die folgende Tabelle zeigt, wie die Tastenfunktionen gesamten Messungen verwendet werden, um mehrere berechnete Kennzahlen im Dataset des Inhalts zu erstellen.

| Kennzahl                                       | Wie die festgelegte Kennzahl berechnet wird                                                                                          |
|-----------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| Istkosten                                   | BERECHNEN Sie "Kostenrechnung "entries'entity_PLACEHOLDER [Kennzahl \\]\ versions'entity_PLACEHOLDER Buchung ", [ISSOURCEVERSIONBUDGET\_WERT\] = 0)            |
| Budgetkosten                                   | BERECHNEN Sie "Kostenrechnung "entries'entity_PLACEHOLDER [Kennzahl \\]\ versions'entity_PLACEHOLDER Buchung ", [ISSOURCEVERSIONBUDGET\_WERT\] = 1)            |
| Budgetkostabweichung                          | Istkosten \]\[Budgetkost__ent_dict_PLACEHOLDER\] -                                                                                       |
| Planabweichungsprozentsatz                    | IF (\[Budgetkost\] = 0, blank(), Budgetkost\]\[Planabweichungs-__ent_dict_PLACEHOLDER\] / \[                                                |
| Tatsächliche Größe                              | Sie BERECHNEN Sie ("entries'entity_PLACEHOLDER statistisches [FullMagnitude \\]\ versions'entity_PLACEHOLDER Buchung ", [ISSOURCEVERSIONBUDGET\_WERT\] = 0)          |
| Budgetgröße                              | Sie BERECHNEN Sie \[,\]FullMagnitude ('Buchung versions'entity_PLACEHOLDER \ [ISSOURCEVERSIONBUDGET\_WERT\] = 1)                               |
| Statistische Planabweichung                   | tatsächliche Größe \]\[Budgetgrößen-__ent_dict_PLACEHOLDER\] -                                                                             |
| Statistischer Planabweichungsprozentsatz        | IF (\[Budgetgröße\] 0, blank()blank() Planabweichungs-__ent_dict_PLACEHOLDER\] / \[\[)                          |
| Istkostensatz                              | IF tatsächliche (Größe \]\[= 0, BLANK(), tatsächliche Größe\]\[Istkosten__ent_dict_PLACEHOLDER\] / \[                                          |
| Budgetverrechnungssatz                              | IF (\[Budgetgröße\] 0, BLANK()BLANK() Budgetgröße\]\[\]\] / \]                                          |
| Budgetkostsatzabweichung                     | Istkostensatz \]\[\] -                                                                             |
| Budgetkostsatz-Abweichungsprozentsatz          | IF (\[Budgetkost\] = 0, blank(), Budgetkostsatz\]\[\] / )                                 |
| Feste Budgetkost                             | Sie BERECHNEN Sie \[,\]Budgetkost ('Kostenrechnung entries'entity_PLACEHOLDER \ [COSTBEHAVIOR\] = 1)                                              |
| Variable Budgetkost                          | Sie BERECHNEN Sie \[,\]Budgetkost ('Kostenrechnung entries'entity_PLACEHOLDER \ [COSTBEHAVIOR\] = 2)                                              |
| Feste flexible Budgetkosten                    | \[Feste Budgetkost\]                                                                                                  |
| Variable Kosten des flexiblen Budgets                 | IF (\[Budgetgröße\] 0, BLANK()BLANK()" Budgetkost__ent_dict_PLACEHOLDER\] / \[\[) tatsächliche\]\]\*\]       |
| Flexible Budgetkosten                          | \[korrigierte flexibles Budget\]Kosten + \[variables flexibles Budget\]Kosten                                                     |
| Variante des flexiblen Budgets                      | Istkosten mit Kosten \]\] - \[\[flexiblen Budgets                                                                             |
| Prozentsatz für flexible Budgets           | IF (\[flexibles Budget\] Kosten mit = 0, BLANK(), Abweichungs-__ent_dict_PLACEHOLDER\] / \[\[Budgets flexibles Budget \[Kosten)                     |
| Verrechnungssatz für flexible Budgets                     | IF tatsächliche (Größe \]\[= 0, BLANK(), \[flexibles Budget\]Kosten / \[tatsächliche Größe\])                                 |
| Kostensatzabweichung für flexible Budgets            | Kostensatz__ent_dict_PLACEHOLDER \] - \[\[Budgets Istkostensatz\[                                                                   |
| Kostensatz-Abweichungsprozentsatz für flexible Budgets | IF (Verrechnungssatz \]\[flexiblen Budgets = 0, BLANK(), Kostensatzabweichungs__ent_dict_PLACEHOLDER\] / \[\[Verrechnungssatz \[Flexibles\]" |

Die folgenden wichtigen Dimensionen werden als Filter verwendet, um die gesamten Messungen ein Crossdocking, um größere Granularität zu erreichen tiefere und analytische Einblicke bereitzustellen.

| Entität                             | Beispiele für Attribute                                                                                               |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| Kostenrechnungssachkonten            | Kostenrechnungssachkonto                                                                                               |
| Kostensteuerungseinheiten                 | Name der Kostensteuerungseinheit                                                                                               |
| Kostenelementdimensionen            | Kostenfaktordimensionsname, Kostenfaktordimensionsmitgliedsname, Kostenfaktordimensionsmitgliedsbeschreibung          |
| Kostenobjektdimensionen             | Kostenträgerdimensionsname, Kostenträgerdimensions-Mitgliedsname, Kostenträgerdimensions-Mitgliedsbeschreibung              |
| Statistische Dimensionen             | Statistischer Dimensionsname, Dimensionsmitgliedsname, statistische Dimensionsmitgliedsbeschreibung statistischer              |
| Kostenträgerdimensionshierarchien  | Kostenträgerdimensionshierarchiename, Kostenträgerdimensionshierarchieebene, Kostenträgerdimensionshierarchiestruktur    |
| Kostenfaktordimensionshierarchien | Kostenfaktordimensionshierarchiename, Kostenfaktordimensionshierarchieebene, Kostenfaktordimensionshierarchiestruktur |
| Statistische Dimensionshierarchien  | Statistischer Dimensionshierarchiename, statistische Dimensionshierarchieebene, statistische Dimensionshierarchiestruktur    |
| Transaktionsversionen               | Versionsname                                                                                                         |
| Steuerkalender                   | Kalender, Kalenderbeschreibung                                                                                       |
| Geschäftsjahre                       | Kalenderjahr                                                                                                        |
| Finanzzeiträume                     | Kalenderjahrsperiode                                                                                                 |

## <a name="additional-resources"></a>Zusätzliche Ressourcen
Nachfolgend finden Sie einige hilfreiche Links zum Thema Entitäten und Erstellen von Power BI-Inhalten:

-   [Datenentitäten](..\data-entities\data-entities.md)
-   [Erstellen von Organisations-Inhaltspaketen](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Datenmodellierung mithilfe von Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Hinzufügen von Power BI-Kacheln zu Arbeitsbereichen](configure-power-bi-integration.md)
-   [Aufstellungssicherheit für Kostenrechnungsinhalt für Leistung BI] (setup-security-cost-accounting-content-pack.md )


