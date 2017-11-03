---
title: Kostenrechnungsanalyse Power BI Inhalt
description: "In diesem Thema wird beschrieben, was im Buchhaltungsanalyse Power Bl enthalten ist. Es wird erläutert, wie Sie auf die Power Bl-Berichte zugreifen und enthält Informationen zum Datenmodell und zu den Entitäten, die verwendet werden, um den Inhalt zu erstellen."
author: AndersGirke
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 270274
ms.assetid: b74549df-35d5-4f2f-b3c7-405b0d38ea78
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: b49cfe39732a450e4723419c50d8bcc3d64b7ec9
ms.openlocfilehash: f596f84463f46fc37b14b77bd335b9ed8a62eea9
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---

# <a name="cost-accounting-analysis-power-bi-content"></a>Kostenrechnungsanalyse Power BI Inhalt

[!include[banner](../includes/banner.md)]

In diesem Thema wird beschrieben, was im **Buchhaltungsanalyse** Microsoft Power Bl-Inhalt enthalten ist. Es wird erläutert, wie Sie auf die Power Bl-Berichte zugreifen und enthält Informationen zum Datenmodell und zu den Entitäten, die verwendet werden, um den Inhalt zu erstellen.

## <a name="overview"></a>Überblick

Der **Kostenrechnungsanalyse**-Power BI-Inhalt dient den Kostencontrollern oder all jenen, die für die Ausführung der Kostensteuerung in einer Organisation verantwortlich sind. Er umfasst die Schlüsselindikatoren, wie Kosten, Größe und Verrechnungssatz von Istkosten, Budgetkost und flexible Budgetkosten. Er verwendet Buchungsdaten aus dem **Kostenrechnungs**-Modul und stellt eine gesamte Ansicht von Kosten für die gesamte Organisation in einer Berichtswährung bereit. Manager können die Daten nach Kostenträger filtern, um die Kostensteuerung der Organisationseinheiten vorzunehmen, selbst wenn die Organisation mehrere juristische Personen hat. 

Da der **Kostenrechnungsanalyse**-Inhalt Abweichungen zwischen den Istkosten und den budgetierten Kosten hervorhebt, können Manager über die positiven und negativen Trends für ihre Einsatzkräfte informiert werden. Manager können zu den Kostenfaktorhierarchien oder den einzelnen Kostenfaktoren Detailinformationen anzeigen. Auf diese Weise können Manager einen detaillierten Einblick erhalten, wie Kostenabweichungen aufgetreten sind, und anschließend wirksame Maßnahmen ausführen. 

Der **Kostenrechnungsanalyse**-Inhalt ermöglicht es Buchhaltern, Kosten zu analysieren, um zu sehen, wie Kosten die Kostenträger der gesamten Organisation durchlaufen. 

Weitere Informationen zur Kostenrechnung finden Sie unter [Startseite Kostenrechnung](../../financials/cost-accounting/cost-accounting-home-page.md). 

Durch das Festlegen der  Zugriffsebenensicherheit in der Kostenrechnung und durch die Kombination mit Zeilenebenensicherheit in Power BI können Sie allen Kostenträgereigentümern Zugriff auf den **Kostenrechnungsanalyse** Power BI Inhalt geben. Alle Daten in den Visualisierungen werden anschließend auf Basis der Zugriffsebene gefiltert, die in der Kostenrechnung gesteuert wird. Weitere Informationen zur Zugriffsebenensicherheit und zur Sicherheit auf Zeilenebene finden Sie unter [Sicherheit für Kostenbuchhaltung für Power BI einrichten](setup-security-cost-accounting-content-pack.md)..

## <a name="accessing-the-power-bi-content"></a>Zugreifen au Power BI Inhalt
Sie finden die  **Kostenbuchhaltungsanalyse** Power BI Inhalt in der Bibliothek für freigegebene Anlagen in Microsoft Dynamics Lifecycle Services (LCS). Weitere Informationen dazu, wie Sie Power BI-Inhalte herunterladen und in Ihrer Organisation implementieren, finden Sie unter [Power BI-Inhalt in LCS von Microsoft und Ihren Partnern](power-bi-content-microsoft-partners.md). Um eine Vorführung anzusehen, die zeigt, wie der Power BI-Inhalt impementiert wird, zeigen Sie den Office Mix [Power BI-Inhalt von Microsoft und Ihren Partnern in Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) an.

Stellen Sie sicher, dass Sie den **Kostenrechnungsanalyse**-Inhalt herunterladen, der der von Ihnen verwendeten Microsoft Dynamics 365-Version entspricht.

> [!NOTE]
> KB 4011327 ist eine Voraussetzung für diesen Power BI-Inhalt Nachdem Sie sich bei LCS angemeldet haben, können Sie unter <https://fix.lcs.dynamics.com/issue/results/?q=kb4011327> auf die KB zugreifen.

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
Die folgenden Daten werden verwendet, um die Berichtsseiten im Power BI-Inhalt **Kostenrechnungsanalyse** auszufüllen. Diese Daten werden als gesamte Messungen dargestellt, die im Entitätsshop bereitgestellt werden. Der Entitätsshop ist eine Microsoft SQL Server-Datenbank, die zwecks Analyse optimiert ist. Weitere Informationen finden Sie in der [Übersicht Power BI Integration mit Entitätsspeicher](power-bi-integration-entity-store.md). 

Die folgenden aggregierten Messungen werden als Grundlage des Inhaltspakets verwendet.

| Entität                  | Zentrale aggregierte Messungen | Datenquelle für Dynamics 365      | Feld     | Beschreibung                                        |
|-------------------------|---------------------------|-----------------------------------|-----------|----------------------------------------------------|
| Kostenrechnungseinträge | SUM (Betrag)               | CAMDATAAggregatedCostEntry        | Betrag    | Der Betrag in der Kostenbuchhaltungs-Sachkontowährung. |
| Statistische Einträge     | SUM(Größe)            | CAMDATAAggregatedStatisctialEntry | Größe |                                                    |

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

