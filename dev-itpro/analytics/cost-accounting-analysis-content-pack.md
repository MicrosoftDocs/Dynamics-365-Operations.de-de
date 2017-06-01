---
title: Kostenrechnungsanalyse Power BI Inhalt
description: "In diesem Thema wird beschrieben, was im Buchhaltungsanalyse Power Bl enthalten ist. Es wird erläutert, wie Sie auf die Power Bl-Berichte zugreifen und enthält Informationen zum Datenmodell und zu den Entitäten, die verwendet werden, um den Inhalt zu erstellen."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 270274
ms.assetid: b74549df-35d5-4f2f-b3c7-405b0d38ea78
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 5ce75a6145bde4a8c33ed785c7d2a60a52416676
ms.contentlocale: de-de
ms.lasthandoff: 05/25/2017


---

# <a name="cost-accounting-analysis-power-bi-content"></a>Kostenrechnungsanalyse Power BI Inhalt

[!include[banner](../includes/banner.md)]


In diesem Thema wird beschrieben, was im Buchhaltungsanalyse Power Bl enthalten ist. Es wird erläutert, wie Sie auf die Power Bl-Berichte zugreifen und enthält Informationen zum Datenmodell und zu den Entitäten, die verwendet werden, um den Inhalt zu erstellen.

<a name="overview"></a>Überblick
--------

Die **Kostenrechnungsanalyse** Microsoft Power BI Inhalt dient für die Kostencontroller oder alle jene, die für die Ausführung der Kostensteuerung für eine Organisation verantwortlich sind. Er umfasst die Schlüsselindikatoren, wie Kosten, Größe und Verrechnungssatz von Istkosten, Budgetkost und flexible Budgetkosten. Er verwendet Buchungsdaten aus der Kostenrechnung in Microsoft Dynamics 365 for Operations und erstellt eine gesamte Ansicht von Kosten für die gesamte Organisation in einer Berichtswährung bereit. Manager können die Daten nach Kostenträger filtern, um die Kostensteuerung der Organisationseinheiten vorzunehmen, selbst wenn die Organisation mehrere juristische Personen hat. Da der **Kostenrechnungsanalyse** Power BI Inhalt Abweichungen zwischen den Istkosten und den budgetierten Kosten hervorhebt, können Manager über die positiven und negativen Trends für ihre Einsatzkräfte informiert werden. Manager können zu den Kostenfaktorhierarchien oder den einzelnen Kostenfaktoren navigieren, sich detaillierte Einblicke verschaffen, wie Kostenabweichungen aufgetreten sind, und dannwirksame Maßnahmen ergreifen. Der **Kostenrechnungsanalyse** Power BI Inhalt ermöglicht es Buchhaltern,  Kosten zu analysieren, um zu sehen, wie Kosten die Kostenträger der gesamten Organisation durchlaufen. Weitere Informationen zur Kostenrechnung finden Sie unter [Startseite Kostenrechnung](/dynamics365/operations/financials/cost-accounting/cost-accounting-home-page). Durch das Festlegen der  Zugriffsebenensicherheit in der Kostenrechnung und durch die Kombination mit Zeilenebenensicherheit in Power BI können Sie allen Kostenträgereigentümern Zugriff auf den **Kostenrechnungsanalyse** Power BI Inhalt geben. Alle Daten in den Visualisierungen werden anschließend auf Basis der Zugriffsebene gefiltert, die in der Kostenrechnung gesteuert wird. Weitere Informationen zur Zugriffsebenensicherheit und zur Sicherheit auf Zeilenebene finden Sie unter [Sicherheit für Kostenbuchhaltung für Power BI einrichten](setup-security-cost-accounting-content-pack.md)..

## <a name="accessing-the-power-bi-content"></a>Zugreifen au Power BI Inhalt
Sie finden die  **Kostenbuchhaltungsanalyse** Power BI Inhalt in der Bibliothek für freigegebene Anlagen in Microsoft Dynamics Lifecycle Services (LCS). Weitere Informationen dazu, wie Sie Inhalte herunterladen und mit Ihrem Microsoft Dynamics 365 for Operations verbinden, finden Sie unter [Power Bi Inhalt in LCS von Microsoft und Ihren Partnern](power-bi-content-microsoft-partners.md). 

> HINWEIS **KB4011327** ist eine Voraussetzung für diesen Power BI Inhalt Nachdem Sie sich bei Lifecycle Services angemeldet haben, können Sie hier auf KB zugreifen: <https://fix.lcs.dynamics.com/issue/results/?q=kb4011327>.

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Metrik, die im Power BI Inhalt enthalten ist
Der Inhalt enthält einen Satz Berichtsseiten. Jede Seite enthält einen Satz Metriken, die als Diagramme, Kacheln und Tabellen visuell dargestellt werden. Die folgende Tabelle enthält eine Übersicht der Visualisierungen im **Kostenbuchhaltungsanalyse** Power Bl Inhalt.

| Berichtsseiten                      | Diagramm                                                                                                                         | Kachel                                          |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| Kostenkontrolle nach Finanzzeitraum    | Istkosten und Budgetkost nach Kostenfaktorhierarchieebene                                                                   | Ist-Kosten im Vergleich zu Budgetkosten                    |
|                                  | Planabweichung nach Kostenfaktorhierarchieebene                                                                               | Istkostenrate verglichen mit der Budgetkostenrate          |
|                                  | Liste der größten 10 Budgetabweichungen in Prozent nach Kostenenelement                                                                          | Tatsächliche Größe für Budgetgröße          |
| Kostenkontrolle seit Jahresbeginn     | Istkosten und Budgetkost nach Kalenderjahrs-Periode                                                                           | Ist-Kosten im Vergleich zu Budgetkosten                    |
|                                  | Planabweichung nach Kalenderjahrs-Periode                                                                                       | Istkostenrate verglichen mit der Budgetkostenrate          |
|                                  | Liste der größten 10 Budgetabweichungen in Prozent nach Kostenenelement                                                                          | Tatsächliche Größe für Budgetgröße          |
| Verrechnungssatz nach Geschäftsjahr         | Verhalten Istkostensatz nach Kosten                                                                                             | Istkostenrate verglichen mit der Budgetkostenrate          |
|                                  | Istkostensatz, Budgetkostsatzabweichung, Budgetkostsatzprozentsatz und Budgetkosten bewerten nach Kostenfaktorhierarchieebene | Tatsächliche Größe für Budgetgröße          |
|                                  | Planabweichung nach Kostenfaktorhierarchieebene                                                                               |                                               |
|                                  | Liste der größten 10 Budgetabweichungen in Prozent nach Kostenenelement                                                                          |                                               |
| Flexibles Budget nach Finanzzeitraum | Istkosten und Budgetkost nach flexiblen Budgetkosten nach Kostenfaktorhierarchieebene                                             | Tatsächliche Größe für Budgetgröße          |
|                                  | Budgetabweichungen und flexible Budgetabweichungen nach Kostenfaktorhierarchieebene                                                  | Ist-Kosten im Vergleich zu flexiblen Budgetkosten           |
|                                  | Istkosten, Budgetkost und flexible Budgetkosten nach Kostenverhalten und Kostenfaktorhierarchieebene                                  | Istkostenrate verglichen mit der fleixblen Budgetkostenrate |
| Kostenkontrolle nach Finanzzeitraum  | Istkosten nach Kostenelementhierarchie und Kostenobjektdimensions-Mitgliedsname                                             |                                               |
|                                  | Istkosten nach Kostenelementhierarchie und Kostenobjektdimensions-Mitgliedsname                                       |                                               |

## <a name="understanding-the-data-model-and-entities"></a>Das Datenmodells und die Entitäten verstehen
Dynamics 365 for Operations-Daten werden für die Berichte in **Kostenbuchhaltungsanalyse** Power BI Inhalt ergänzt. Diese Daten werden als gesamte Messungen dargestellt, die im Entitätsshop bereitgestellt werden, der eine Microsoft SQL-Datenbank ist, die zwecks Analyse optimiert ist. Weitere Informationen finden Sie in der [Übersicht Power BI Integration mit Entitätsspeicher](power-bi-integration-entity-store.md). Die folgenden aggregierten Messungen werden als Grundlage des Inhaltspakets verwendet.

| Entität                  | Zentrale aggregierte Messungen | Datenquelle für Dynamics 365 for Operations | Feld     | Beschreibung                                   |
|-------------------------|---------------------------|---------------------------------------------|-----------|-----------------------------------------------|
| Kostenrechnungseinträge | SUM (Betrag)               | CAMDATAAggregatedCostEntry                  | Betrag    | Betrag in der Kostenbuchhaltungs-Sachkontowährung |
| Statistische Einträge     | SUM(Größe)            | CAMDATAAggregatedStatisctialEntry           | Größe |                                               |

Die folgende Tabelle zeigt, wie die zentralen aggregierten Messungen verwendet werden, um mehrere berechnete Kennzahlen im Dataset des Inhalts zu erstellen.

| Kennzahl                                       | Wie die festgelegte Kennzahl berechnet wird                                                                                          |
|-----------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| Istkosten                                   | BERECHNEN Sie "Kostenrechnungeinträge'\[Messung\], Transaktionsversion\[ISSOURCEVERSIONBUDGET\_VALUE\] = 0)            |
| Budgetkosten                                   | BERECHNEN Sie "Kostenrechnungeinträge'\[Messung\], Transaktionsversion\[ISSOURCEVERSIONBUDGET\_VALUE\] = 1)            |
| Budgetabweichung                          | \[Budgetkosten\] - \[Istkosten\]                                                                                      |
| Budgetabweichung in Prozent                    | IF(\[Budgetkosten\] = 0, blank(), \[Budgetabweichung\] / \[Budgetkosten\])                                                |
| Tatsächliche Größe                              | BERECHNEN('Statische Einträge'\[FullMagnitude\], 'Transaktionsversionen'\[ISSOURCEVERSIONBUDGET\_VALUE\] = 0)          |
| Budgetgröße                              | BERECHNEN(\[FullMagnitude\], 'Transaktionsversionen'\[ISSOURCEVERSIONBUDGET\_WERT\] = 1)                               |
| Statistische Planabweichung                   | \[Budgetgröße\] - \[Tatsächliche Größe\]                                                                            |
| Statische Budgetabweichung in Prozent        | IF(\[Budgetgröße\] = 0, blank(), \[Statistische Budgetabweichung\] / \[Budgetgröße\])                          |
| Istkostensatz                              | IF(\[Tatsächliche Größe\] = 0, BLANK(), \[Aktuelle Kosten\] / \[Aktuelle Größe\])                                          |
| Budgetverrechnungssatz                              | IF(\[Budgetgröße\] = 0, BLANK(), \[Budgetkosten\] / \[Budgetgröße\])                                          |
| Abweichung Budgetkostensatz                     | \[Budgetkostensatz\] - \[Tatsächlicher Kostensatz\]                                                                            |
| Budgetkostensatz-Abweichung in Prozent          | IF(\[Budgetkosten\] = 0, blank(), \[Budgetkostensatz Abweichung\] / \[Budgetkostensatz\])                                 |
| Anlagenbudgetkosten                             | BERECHNE(\[Budgetkosten\], 'Buchhaltungskosten-Einträge'\[KOSTENVERHALTEN\] = 1)                                              |
| Varialbe Budgetkosten                          | BERECHNE(\[Budgetkosten\], 'Buchhaltungskosten-Einträge'\[KOSTENVERHALTEN\] = 2)                                              |
| Flexible Anlagenbudgetkosten                    | \[Anlagenbudgetkosten\]                                                                                                  |
| Variable Anlagenbudgetkosten                 | IF(\[Budgetgröße\] = 0, BLANK(), (\[Variable Budgetkosten\] / \[Budgetgröße\]) \* \[Tatsächliche Größe\])       |
| Flexible Budgetkosten                          | \[Flexibles Anlagebudget\] + \[Variable flexible Budgetkosten\]                                                     |
| Flexibles Budgetabweichungen                      | \[Flexible Budgetkosten\] - \[Tatsächliche Kosten\]                                                                             |
| Flexible Budgetabweichung in Prozent           | IF(\[Flexible Budgetkosten\] = 0, BLANK(), \[Flexible Budgetabweichungen\] / \[Flexible Budgetkosten\])                     |
| Flexibler Budgetkostensatz                     | IF(\[Tatsächliche Größe\] = 0, BLANK(), \[Flexible Budgetkosten\] / \[Tatsächliche Größe\])                                 |
| Flexible Budgetkostensatz-Abweichung in Prozent            | \[Flexibler Budgetkostensatz\] - \[Aktueller Kostensatz\]                                                                   |
| Flexible Budgetkostensatz-Abweichung in Prozent | IF(\[Flexibler Budgetkostensatz\] = 0, BLANK(), \[Flexibler Budgetkostensatz, Abweichung\] / \[Flexibler Budgetkostensatz\]) |

Die folgenden wichtigen Dimensionen werden als Filter verwendet, um die aggregierte Messungen zu teilen, um eine größere Granularität zu erreichen und tiefere und analytische Einblicke bereitzustellen.

| Entität                             | Beispiele für Attribute                                                                                               |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| Kostenrechnungssachkonten            | Kostenrechnungssachkonto                                                                                               |
| Kostensteuerungseinheiten                 | Name der Kostensteuerungseinheit                                                                                               |
| Kostenelementdimensionen            | Kostenelementdimensionsname, Kostenelementdimensionsmitgliedsname, Kostenelementdimensions-Mitgliedsbeschreibung          |
| Kostenobjektdimensionen             | Kostenelementdimensionsname, Kostenelementdimensionsmitgliedsname, Kostenelementdimensions-Mitgliedsbeschreibung              |
| Statistische Dimensionen             | Statistischer Dimensionsname, Statistischer Dimensionsmitgliedsname, Statistischer Dimensionsmitgliedsbeschfreibung              |
| Kostenobjekt-Dimensionshierarchie  | Kostenträgerdimensionshierarchiename, Kostenträgerdimensionshierarchieebene, Kostenträgerdimensionshierarchiestruktur    |
| Kostenelement-Dimensionshierarchie | Kostenelementdimensionshierarchiename, Kostenelementdimensionshierarchieebene, Kostenelementdimensionshierarchiestruktur |
| Statistische Dimensionshierarchie  | Statistische Dimensionshierarchiename, Statistischer Dimenstionhierarchieebene, statistische Kostenträgerdimensionshierarchiestruktur    |
| Transaktionsversionen               | Versionsname                                                                                                         |
| Steuerkalender                   | Kalender, Beschreibung des Kalenders                                                                                       |
| Geschäftsjahr                       | Kalenderjahr                                                                                                        |
| Finanzzeiträume                     | Kalenderperioden                                                                                                 |

## <a name="additional-resources"></a>Zusätzliche Ressourcen
Nachfolgend finden Sie einige hilfreiche Links zum Thema Entitäten und Erstellen von Power BI-Inhalten:

-   [Datenentitäten](..\data-entities\data-entities.md)
-   [Erstellen von Organisations-Inhaltspaketen](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Datenmodellierung mithilfe von Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Hinzufügen von Power BI-Kacheln zu Arbeitsbereichen](configure-power-bi-integration.md)
-   [Aufstellungssicherheit für Kostenrechnungsinhalt für Power B]](setup-security-cost-accounting-content-pack.md)




