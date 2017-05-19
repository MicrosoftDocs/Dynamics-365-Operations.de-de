---
title: "Vertriebs-und Rentabilitätsleistung Power BI Inhalt"
description: "In diesem Thema wird beschrieben, was im Dynamics 365 for Operations - Vertriebs-und Rentabilitätsleistung-Inhaltspaket für Microsoft Power BI enthalten ist. Es wird zudem beschrieben, wie das Dashboard und die Berichte, die im Inhaltspaket enthalten sind, verwendet werden und enthält Informationen zum Datenmodell und den Entitäten, die verwendet werden, um das Inhaltspaket zu erstellen."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 260674
ms.assetid: ab457f02-929e-4d34-b813-335be3092287
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 35d34f9a356f8a041f2abf0aa8d6c3a6d9ca4a46
ms.contentlocale: de-de
ms.lasthandoff: 04/25/2017


---

# <a name="sales-and-profitability-performance-power-bi-content"></a>Vertriebs-und Rentabilitätsleistung Power BI Inhalt

[!include[banner](../includes/banner.md)]


In diesem Thema wird beschrieben, was im Dynamics 365 for Operations - Vertriebs-und Rentabilitätsleistung-Inhaltspaket für Microsoft Power BI enthalten ist. Es wird zudem beschrieben, wie das Dashboard und die Berichte, die im Inhaltspaket enthalten sind, verwendet werden und enthält Informationen zum Datenmodell und den Entitäten, die verwendet werden, um das Inhaltspaket zu erstellen.

<a name="overview"></a>Überblick
--------

Dies Inhaltspaket wurde erstellt für Verkaufsleiter zum Überwachen die Vertriebsmetrik Umsatzerlöses, des Bruttogewinns und der Margen. Es verwendet Transaktionsdaten aus von Dynamics 365 for Operations und stellt eine Gesamtübesicht zu unternehmensweiten Umsatzahlen und eine Aufschlüsselung des Verkaufsergebnisses für Debitoren und Produkte zur Verfügung. Durch das Hervorheben von Umsatzerlösänderungen und Gewinnwachstum im Zeitverlauf, können Berichte verwendet werden, um Manager über die positiven und negativen Trends für einzelne Debitoren und Produkte hinzuweisen. Kategorie- und regionale Manager können Diagramme zu haben, mit denen Umsatzerlöse und Rentabilität verschiedener Produktkategorien und Debitorengruppen miteinander vergleichen, um schlechte und gute Elemente zu erlennen. Ein umfassender Bericht zu einzelnen Umsatzerlösen des Debitors mit Gewinnspanne bietet Account Managern eine Daten-unterstützte Basis an, um die Verkaufs- und Marketings-Aufwände mit dem Profil jedes Debitors abzustimmen. Das Vertriebs-und Rentabilitätsleistung-Inhaltspaket ermöglicht Verkaufsleiter die Verkaufsleistung zu analysieren:

-   Umsatzerlös, laufenden Jahres (nach Debitorengruppen- und Personendebitoren, Verkaufskategorien und Einzelprodukte und bestimmte geografische Region)
-   Umsatzerlösänderung, jährlich (nach Debitorenregionen und -Verkaufskategorien)

Rentabilität kann wie folgt analysiert werden:

-   Bruttogewinn und Gewinnspanne (nach Debitorengruppen und Produktverkaufskategorien)
-   Bruttogewinnänderung, jährlich
-   Debitorenrentabilität (nach Umsatz gegen Bruttogewinn)

## <a name="accessing-the-content-pack"></a>Zugreifen auf das Inhaltspaket
Der Vertriebs-und Rentabilitätsleistung-Inhaltspaket für Power BI wird als Implementierungsressource in Lifecycle Services (LCS) veröffentlicht und kann von Dynamics 365 for Operations zugegriffen werden. Weitere Informationen dazu, wie Power BI-Bericht erstellt werden, finden Sie unter [Power Bi Inhalt in LCS von Microsoft und Ihren Partnern](power-bi-content-microsoft-partners.md).
Hinweis: **KB4011327** ist eine Voraussetzung für diesen Power BI Inhalt Nachdem Sie sich bei Lifecycle Services angemeldet haben, können Sie hier auf KB zugreifen: <a href="https://fix.lcs.dynamics.com/issue/results/?q=kb4011327">https://fix.lcs.dynamics.com/issue/results/?q=kb4011327</a>.

## <a name="metrics-included-in-the-content-pack"></a>Metrik im Inhaltspaket
Der Inhaltspaket enthält einen Bericht, der einem Satz Metriken visuell dargestellt als Diagramme, Kacheln und Tabellen besteht. Die folgende Tabelle enthält eine Übersicht der im Visualisierungen im Inhaltspaket.

|                        |                                            |                                                         |
|------------------------|--------------------------------------------|---------------------------------------------------------|
| **Berichtsseiten**        | **Diagramme**                                 | **Kacheln**                                               |
| Umsatz nach Debitor    | Beste 10 Debitoren nach Umsatz                | Gesamtumsatz                                           |
|                        | Gesamtumsatzerlös nach Debitorengruppe            | YOY-Umstatzsteigerung                                      |
|                        | Durchschnittskundeumsatzerlös nach Debitorengruppe | Bruttogewinn                                            |
|                        | Umsatzerlös und Bruttogewinn nach Debitorengruppe.   |                                                         |
| Umsatz nach Produkt     | Umsatzerlös und Bruttogewinn nach Verkaufskategorie.   | Produkte \# gesamt                                    |
|                        | Beste 10 Produkte nach Umsatz                 | Gesamtanzahl der aktiven Produkte und Gesamtprozentsatz |
|                        | Gesamtumsatzerlös nach Verkaufskategorie            | Zahl der Produkte, die zu 80% Umsatzerlös betragen           |
| Umsatz nach Zeitraum\*    | Umsatz nach Monat                           | YOY-Umstatzsteigerung                                      |
|                        | Nachfolgende Abweichung bei Umsatze, YOY             | YOY-Umstatzsteigerung %                                    |
|                        | Gesamte Verkaufsmengenabweichung nach Debitorenregion    |                                                         |
| Umsatz nach Lagerplatz    | Umsatzerlöse nach Ort                      |                                                         |
|                        | YOY-Umstatzsteigerung %                       |                                                         |
|                        | Umsatz nach Regionen                    |                                                         |
| Debitorenrentabilität | Bruttogewinn versus Umsatz nach Debitor   | Bruttogewinn, Bruttoerlös, YOY-Umstatzsteigerung          |
| Rentabilitätsanalyse | Umsatzerlös und Bruttogewinn nach Monat          |                                                         |
|                        | Top 15 Debitoren nach Bruttogewinn           |                                                         |
|                        | Bruttogewinn nach Monat, YOY                 |                                                         |

\* Umsatzerlös dieser und letzten Jahr und Wachstum nach Verkaufskategorie.

## <a name="understanding-the-data-model-and-entities"></a>Das Datenmodells und die Entitäten verstehen
Dynamics 365 for Operations-Daten werden für die Berichte im Vertriebs-und Rentabilitätsleistung-Inhaltspaket verwendet. Diese Daten werden als gesamte Messungen dargestellt, die im Entitätsshop bereitgestellt werden, der eine Microsoft SQL-Datenbank ist, die zwecks Analyse optimiert ist. Lesen Sie mehr im Blog [Power BI integration with Entity Store in Dynamics](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/). Die gesamten Messungen in diesem Inhaltspaket sind die Teilmenge der gesamten Messungen, die im Sales Cube in Dynamics AX 2012 und AX 2012 R3 verfügbar waren. Um die Cube-Messungen im Entitätspeicher bereitzustellen, müssen Sie diese bereitstellbar machen. Weitere Informationen finden Sie unter [Power BI integration with Entity Store in Dynamics](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/). Die folgenden aggregierten Messungen der Rechnungspositionsentität werden als Grundlage des Inhaltspakets verwendet.

|               |                                              |                                                 |                                              |                                          |
|---------------|----------------------------------------------|-------------------------------------------------|----------------------------------------------|------------------------------------------|
| **Entität**    | **Zentrale aggregierte Messungen**               | **Datenquelle für Dynamics 365 for Operations** | **Feld**                                    | **Beschreibung**                          |
| Rechnungspositionen | Umsatzerlös                                      | CustInvoiceTrans                                | SUM(LineAmountMST)                           | Betrag in Buchhaltungswährung            |
|               | Wareneinsatz                           | InventTrans                                     | SUM(CostAmountPosted + CostAmountAdjustment) | Cost amount + adjustment                 |
|               | Betrag der Provisionsposition - Buchhaltungswährung | CustInvoiceTrans                                | SUM(CommissAmountMST)                        | Betrag der Provision in Buchhaltungswährung |

Die folgende Tabelle zeigt, wie die zentralen aggregierten Messungen verwendet werden, um mehrere berechnete Kennzahlen der Rechnungspositionsentität im Dataset des Inhalts zu erstellen.

|                   |                                                                                                  |
|-------------------|--------------------------------------------------------------------------------------------------|
| **Kennzahl**       | **Berechnet als**                                                                                |
| Bruttogewinn      | SUM(Umsatz – COGS – Provision – Mehrwertsteuer (in Rechnungsposition enthalten))          |
| Bruttogewinn      | SUM(Gross profit / (Revenue - Sales tax (in Rechnungsposition enthalten)))             |
| Umsatzerlös letztes des | Revenue last year = CALCULATE(SUM('Invoice lines'\[Revenue\]), SAMEPERIODLASTYEAR(Dates\[Date\]) |

Die folgenden wichtigen Dimensionen im **Sales-Cube** werden als Filter verwendet, um die aggregierte Messungen zu teilen, um eine größere Granularität zu erreichen und tiefere und analytische Einblicke bereitzustellen.

|                  |                                                      |
|------------------|------------------------------------------------------|
| **Entität**       | **Beispiele für Attribute**                           |
| Debitoren        | Customer groups, Customer regions, Address, Industry |
| Produkte         | Produktnummer, Produktname, Artikelgruppenname       |
| Verkaufskategorien | Verkaufskategorienamen                                 |
| Juristische Personen   | Name der juristischen Person                                   |
| Daten            | Daten                                                |

Standardmäßig zeigt das Inhaltspaket Daten während des laufenden Kalenderjahr an. Aber Sie können den Berichtsfilterabschnitt den Datumsfilter öffnen und ändern. Sie können das den Unternehmensfilter auch ändern.

## <a name="additional-resources"></a>Zusätzliche Ressourcen
Nachfolgend finden Sie einige hilfreiche Links zum Thema Entitäten und Erstellen von Power BI-Inhalten:

-   [Datenentitäten](..\data-entities\data-entities.md)
-   [Erstellen von Organisations-Inhaltspaketen](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Datenmodellierung mithilfe von Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Hinzufügen von Power BI-Kacheln zu Arbeitsbereichen](configure-power-bi-integration.md)





