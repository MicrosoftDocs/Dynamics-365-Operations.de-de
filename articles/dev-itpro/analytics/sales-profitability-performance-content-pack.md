---
title: "Vertriebs-und Rentabilitätsleistungsinhalt für Power BI"
description: "In diesem Thema wird beschrieben, was im Umsatz- und Rentabilitätsleistung Power Bl Inhalt enthalten ist. Es wird erläutert, wie Sie auf die Power Bl-Berichte zugreifen und enthält Informationen zum Datenmodell und zu den Entitäten, die verwendet werden, um den Inhalt zu erstellen."
author: YuyuScheller
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 260674
ms.assetid: ab457f02-929e-4d34-b813-335be3092287
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 3692b9be0fb93e0e2de743775a54bb9c9dbf5809
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="sales-and-profitability-performance-power-bi-content"></a>Vertriebs-und Rentabilitätsleistungsinhalt für Power BI

[!include[banner](../includes/banner.md)]

In diesem Thema wird beschrieben, was im **Umsatz- und Rentabilitätsleistung** Microsoft Power Bl Inhalt enthalten ist. Es wird erläutert, wie Sie auf die Power Bl-Berichte zugreifen und enthält Informationen zum Datenmodell und zu den Entitäten, die verwendet werden, um den Inhalt zu erstellen.

## <a name="overview"></a>Überblick

Der **Vertrieb und Rentabilitätsleistung** Power BI Inhalt wurde erstellt, sodass Verkaufsleiter schließlich die eigentliche Vertriebsmetrik des Umsatzerlöses, des Bruttogewinns der Ränder und überwachen können. Es verwendet Transaktionsdaten und stellt eine Gesamtübersicht zu unternehmensweiten Umsatzahlen und eine Aufschlüsselung des Verkaufsergebnisses für Debitoren und Produkte zur Verfügung.

Berichte entsperren Änderungen im Umsatzerlös und im Gewinn-Wachstum im Zeitverlauf. Daher kann der Bericht dazu verwendet werden, um Manager über die positiven und negativen Ausgabentrends für einzelne Kunden und Produkten zu warnen. Darüber hinaus vergleichen die Diagramme den Umsatzerlös und die Rentabilität verschiedener Produktkategorien und Debitorengruppen von gegenseitig. Daher können Kategorie- und Regionalmanager gute und schlechte Produkte zu identifizieren. Schließlich zeichnet ein umfassender Bericht einen einzelnen Umsatzerlös des Debitors mit Gewinnspanne auf. Deshalb haben Kundenbetreuer eine Daten-unterstützte Basis, die dafür verwendet werden kann, die Verkaufs- und Marketing-Aufwände für jedes Debitorenprofil zu optimieren. 

Das **Umsatz- und Rentabilitätsleistung**-Inhaltspaket ermöglicht es Verkaufsleitern, die Verkaufsleistung wie folgt zu analysieren:

-   Umsatzerlös, laufenden Jahres (nach Debitorengruppen- und Personendebitoren, Verkaufskategorien und Einzelprodukte und bestimmte geografische Region)
-   Umsatzerlösänderung, jährlich (nach Debitorenregionen und -Verkaufskategorien)

Rentabilität kann auf folgende Arten analysiert werden:

-   Bruttogewinn und Gewinnspanne (nach Debitorengruppen und Produktverkaufskategorien)
-   Bruttogewinnänderung, jährlich
-   Debitorenrentabilität (nach Umsatz gegen Bruttogewinn)

## <a name="accessing-the-power-bi-content"></a>Zugreifen au Power BI Inhalt
Wenn Sie Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (Juli 2017) verwenden, wird der Power BI Inhalt **Vertrieb und Rentabilitätsleistung** auf der Seite **Vertrieb und Rentabilitätsleistung** (**Vertrieb und Marketing** > **Abfragen und Berichte** > **Vertriebsleistungsanalyse** > **Vertrieb und Rentabilitätsleistung**) angezeigt. 

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Metrik, die im Power BI Inhalt enthalten ist
Der Power BI Inhalt **Umsatz- und Rentabilitätsleistung** enthält einen Bericht, der aus einem Satz Metriken besteht. Diese Metrik werden als Diagramme, Kacheln und Tabellen visuell dargestellt. Die folgende Tabelle enthält eine Übersicht der Visualisierungen im Inhaltspaket.

| Berichtsseiten            | Diagramme                                     | Kacheln                                                   |
|------------------------|--------------------------------------------|---------------------------------------------------------|
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

## <a name="extending-the-power-bi-content"></a>Erweitern des Power BI-Inhalts
Wenn Sie die Inhaltspakete verwenden, die in Microsoft Dynamics Lifecycle Services (LCS) verfügbar sind, können Sie großartige Analysen für Person bereitstellen, die sich nicht in Microsoft Dynamics 365 anmelden. Sie können diese Inhaltspakete so ändern, dass sie andere Berichte oder grafische Elemente umfassen, und die Inhaltspakete dann für die Analyse auf Ihrem Power BI.com-Mandanten veröffentlichen.

Sie finden den **Umsatz- und Rentabilitätsleistung**-Power BI-Inhalt in der freigegebenen Anlagenbibliothek in LCS. Weitere Informationen dazu, wie Sie Power BI-Inhalte herunterladen und in Ihrer Organisation implementieren, finden Sie unter [Power BI-Inhalt in LCS von Microsoft und Ihren Partnern](power-bi-content-microsoft-partners.md). Um eine Vorführung anzusehen, die zeigt, wie der Power BI-Inhalt impementiert wird, zeigen Sie den Office Mix [Power BI-Inhalt von Microsoft und Ihren Partnern in Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) an.

Stellen Sie sicher, dass Sie den **Umsatz- und Rentabilitätsleistung**-Inhalt herunterladen, der der von Ihnen verwendeten Dynamics 365-Version entspricht.

> [!NOTE]
> Wenn Sie Microsoft Dynamics 365 for Operations, Version 1611, verwenden, ist KB 4011327 eine Voraussetzung für diesen Power BI-Inhalt. Nachdem Sie sich bei LCS angemeldet haben, können Sie unter https://fix.lcs.dynamics.com/issue/results/?q=kb4011327 auf KB zugreifen.

## <a name="understanding-the-data-model-and-entities"></a>Das Datenmodells und die Entitäten verstehen
Die folgenden Daten werden verwendet, um den Bericht im Power BI-Inhalt **Umsatz- und Rentabilitätsleistung** auszufüllen. Diese Daten werden als gesamte Messungen dargestellt, die im Entitätsshop bereitgestellt werden. Der Entitätsshop ist eine Microsoft SQL Server-Datenbank, die zwecks Analyse optimiert ist. Weitere Informationen finden Sie in der [Übersicht Power BI Integration mit Entitätsspeicher](power-bi-integration-entity-store.md). 

Die gesamten Messungen in diesem Inhaltspaket sind die Teilmenge der gesamten Messungen, die im Verkaufscube in Microsoft Dynamics AX 2012 und Microsoft Dynamics AX 2012 R3 verfügbar waren. Um die Cube-Messungen im Entitätsspeicher bereitzustellen, müssen Sie diese bereitstellbar machen. Weitere Informationen finden Sie unter [Power BI integration with Entity Store in Dynamics](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/). 

Die folgenden aggregierten Messungen der Rechnungspositionsentität werden als Grundlage des Inhaltspakets verwendet.

| Entität        | Zentrale aggregierte Messungen                   | Datenquelle für Dynamics 365                    | Feld                                        | Beschreibung                                   |
|---------------|----------------------------------------------|-------------------------------------------------|----------------------------------------------|----------------------------------------------|
| Rechnungspositionen | Umsatzerlös                                      | CustInvoiceTrans                                | SUM(LineAmountMST)                           | Der Betrag in der Buchhaltungswährung.            |
|               | Wareneinsatz                           | InventTrans                                     | SUM(CostAmountPosted + CostAmountAdjustment) | Die Summe der Kosten und die Anpassungen.    |
|               | Betrag der Provisionsposition - Buchhaltungswährung | CustInvoiceTrans                                | SUM(CommissAmountMST)                        | Kommissionsbetrag in der Buchungswährung. |

Die folgende Tabelle zeigt, wie die zentralen aggregierten Messungen verwendet werden, um mehrere berechnete Kennzahlen der Rechnungspositionsentität im Dataset des Inhalts zu erstellen.

| Kennzahl           | Herstellkostenkalkulation                                                                                      |
|-------------------|--------------------------------------------------------------------------------------------------|
| Bruttogewinn      | SUM(Umsatz – COGS – Provision – Mehrwertsteuer (in Rechnungsposition enthalten))          |
| Bruttogewinn      | SUM(Gross profit / (Revenue - Sales tax (in Rechnungsposition enthalten)))             |
| Umsatzerlös letztes des | Revenue last year = CALCULATE(SUM('Invoice lines'\[Revenue\]), SAMEPERIODLASTYEAR(Dates\[Date\]) |

Die folgenden wichtigen Dimensionen im Verkaufscube werden als Filter verwendet, um die aggregierten Messungen zu teilen, um eine größere Granularität zu erreichen und tiefere und analytische Einblicke bereitzustellen.

| Entität           | Beispiele für Attribute                               |
|------------------|------------------------------------------------------|
| Debitoren        | Kundengruppen, Kundenregionen, Adresse, Branche |
| Produkte         | Produktnummer, Produktname, Artikelgruppenname       |
| Verkaufskategorien | Verkaufskategorienamen                                 |
| Juristische Personen   | Name der juristischen Person                                   |
| Daten            | Daten                                                |

Standardmäßig zeigt das Inhaltspaket Daten während des laufenden Kalenderjahrs an. Allerdings können Sie den im Berichtsfilterabschnitt Datumsfilter ändern. Sie können das den Unternehmensfilter auch ändern.

