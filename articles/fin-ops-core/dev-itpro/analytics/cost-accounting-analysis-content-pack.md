---
title: Inhalt zur Kostenrechnungsanalyse – Power BI-Inhalt
description: In diesem Artikel wird beschrieben, was im Power BI-Inhalt zur Kostenrechnungsanalyse enthalten ist.
author: AndersGirke
ms.date: 10/02/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 270274
ms.assetid: b74549df-35d5-4f2f-b3c7-405b0d38ea78
ms.openlocfilehash: 7339d0abf8d087ca8fcc8f46dc91a5e78ec0f325
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269724"
---
# <a name="cost-accounting-analysis-power-bi-content"></a>Inhalt zur Kostenrechnungsanalyse – Power BI-Inhalt

[!include [banner](../includes/banner.md)]

In diesem Artikel wird beschrieben, was im Microsoft Power BI-Inhalt zur **Kostenrechnungsanalyse** enthalten ist. Es erläutert, wie Sie auf die Power BI-Berichte zugreifen, und enthält Informationen zum Datenmodell und zu den Entitäten, die verwendet wurden, um den Inhalt zu erstellen.

## <a name="overview"></a>Übersicht

Der Power BI-Inhalt zur **Kostenrechnungsanalyse** dient Kostencontrollern oder all jenen, die für die Ausführung der Kostensteuerung in einer Organisation verantwortlich sind. Er umfasst die Schlüsselindikatoren, wie Kosten, Größe und Verrechnungssatz von Istkosten, Budgetkost und flexible Budgetkosten. Er verwendet Buchungsdaten aus dem **Kostenrechnungs**-Modul und stellt eine gesamte Ansicht von Kosten für die gesamte Organisation in einer Berichtswährung bereit. Manager können die Daten nach Kostenträger filtern, um die Kostensteuerung der Organisationseinheiten vorzunehmen, selbst wenn die Organisation mehrere juristische Personen hat.

Da der **Kostenrechnungsanalyse**-Inhalt Abweichungen zwischen den Istkosten und den budgetierten Kosten hervorhebt, können Manager über die positiven und negativen Trends für ihre Einsatzkräfte informiert werden. Manager können zu den Kostenfaktorhierarchien oder den einzelnen Kostenfaktoren Detailinformationen anzeigen. Auf diese Weise können Manager einen detaillierten Einblick erhalten, wie Kostenabweichungen aufgetreten sind, und anschließend wirksame Maßnahmen ausführen.

Der **Kostenrechnungsanalyse**-Inhalt ermöglicht es Buchhaltern, Kosten zu analysieren, um zu sehen, wie Kosten die Kostenträger der gesamten Organisation durchlaufen.

Weitere Informationen zur Kostenrechnung finden Sie unter [Startseite Kostenrechnung](../../../finance/cost-accounting/cost-accounting-home-page.md).

Durch das Festlegen der Zugriffsebenensicherheit in der Kostenrechnung und durch die Kombination mit Zeilenebenensicherheit in Power BI können Sie allen Kostenträgereigentümern Zugriff auf den Power BI-Inhalt zur **Kostenrechnungsanalyse** geben. Alle Daten in den Visualisierungen werden anschließend auf Basis der Zugriffsebene gefiltert, die in der Kostenrechnung gesteuert wird. Weitere Informationen zur Zugriffsebenensicherheit und zur Sicherheit auf Zeilenebene finden Sie unter [Sicherheit für den Power BI-Inhalt der Kostenrechnungsanalyse einrichten](setup-security-cost-accounting-content-pack.md).

## <a name="accessing-the-power-bi-content"></a>Zugreifen auf den Power BI-Inhalt
Sie finden den Power BI-Inhalt zur **Kostenbuchhaltungsanalyse** in der Bibliothek für freigegebene Anlagen in Microsoft Dynamics Lifecycle Services (LCS). Weitere Informationen dazu, wie Sie den Inhalt herunterladen und in Ihrer Organisation implementieren, finden Sie unter [Power BI-Inhalt in LCS von Microsoft und Ihren Partnern](/archive/blogs/dynamicsaxbi/power-bi-content-from-microsoft-and-your-partners).

Stellen Sie sicher, dass Sie den **Kostenrechnungsanalyse**-Inhalt herunterladen, der der von Ihnen verwendeten Microsoft Dynamics 365-Version entspricht.

> [!NOTE]
> KB 4011327 ist eine Voraussetzung für diesen Power BI-Inhalt Nach der Anmeldung an LCS können Sie hier unter <https://fix.lcs.dynamics.com/issue/results/?q=kb4011327> auf die KB zugreifen.

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Metriken, die im Power BI-Inhalt enthalten sind
Der Inhalt enthält einen Satz Berichtsseiten. Jede Seite enthält einen Satz Metriken, die als Diagramme, Kacheln und Tabellen visuell dargestellt werden. Die folgende Tabelle enthält eine Übersicht der Visualisierungen im Power BI-Inhalt zur **Kostenrechnungsanalyse**.

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
Die folgenden Daten werden verwendet, um die Berichtsseiten im Power BI-Inhalt zur **Kostenrechnungsanalyse** auszufüllen. Diese Daten werden als gesamte Messungen dargestellt, die im Entitätsshop bereitgestellt werden. Der Entitätsshop ist eine Microsoft SQL Server-Datenbank, die für die Analyse optimiert ist. Weitere Informationen finden Sie unter [Power BI Integration mit Entity Store](power-bi-integration-entity-store.md).

Die folgenden aggregierten Messungen werden als Grundlage des Inhaltspakets verwendet.

| Entität                  | Zentrale aggregierte Messungen | Datenquelle für Dynamics 365      | Feld     | Beschreibung                                        |
|-------------------------|---------------------------|-----------------------------------|-----------|----------------------------------------------------|
| Kostenrechnungseinträge | SUM (Betrag)               | CAMDATAAggregatedCostEntry        | Betrag    | Der Betrag in der Kostenbuchhaltungs-Sachkontowährung. |
| Statistische Einträge     | SUM(Größe)            | CAMDATAAggregatedStatisctialEntry | Größe |                                                    |

Die folgende Tabelle zeigt, wie die zentralen aggregierten Messungen verwendet werden, um mehrere berechnete Kennzahlen im Dataset des Inhalts zu erstellen.

| Kennzahl                                       | Wie die festgelegte Kennzahl berechnet wird                                                                                          |
|-----------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| Istkosten                                   | BERECHNEN Sie ("Kostenrechnungeinträge'\[Messung\], Transaktionsversion\[ISSOURCEVERSIONBUDGET\_VALUE\] = 0)            |
| Budgetkosten                                   | BERECHNEN Sie ("Kostenrechnungeinträge'\[Messung\], Transaktionsversion\[ISSOURCEVERSIONBUDGET\_VALUE\] = 1)            |
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
