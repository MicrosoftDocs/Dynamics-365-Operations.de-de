---
title: Einkaufs- und Ausgabenanalyse Power BI-Inhalt
description: In diesem Thema wird beschrieben, was in den Inhalten der Einkaufs- und Ausgabenanalyse Power BI enthalten ist. Es wird beschrieben, wie auf die Berichte, die im Inhalt enthalten sind, zugegriffen wird und es werden Informationen zum Datenmodell und den Entitäten bereitgestellt, die zum Erstellen des Inhalts verwendet werden.
author: FrankDahl
manager: AnnBe
ms.date: 04/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: PurchaseSpendAnalysisPowerBI
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 571f443b02268cbee8fe787f25419e046ba99aeb
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182852"
---
# <a name="purchase-spend-analysis-power-bi-content"></a>Einkaufs- und Ausgabenanalyse Power BI-Inhalt

[!include [banner](../includes/banner.md)]

In diesem Thema wird beschrieben, was in den Inhalten der **Einkaufs- und Ausgabenanalyse** Microsoft Power BI enthalten ist. Es erläutert, wie Sie auf die Power BI-Berichte zugreifen und enthält Informationen zum Datenmodell und zu den Entitäten, die verwendet werden, um den Inhalt zu erstellen.

## <a name="overview"></a>Übersicht

Der **Einkaufs- und Ausgabenanalyse** Power BI-Inhalt wurde entworfen, um Einkaufsleiter und Manager zu unterstützen, die für Budgets verantwortlich sind und die Einkaufausgaben nachverfolgen. Manager können Einkaufsausgaben wie folgt analysieren:

- Einkauf des laufenden Jahres (nach Kreditorengruppen- und Personenkreditoren Beschaffungskategorie, und Einzelprodukte und Standort des Kreditors)
- Jährliche Einkaufänderung (nach Kreditorengruppe und Beschaffungskategorie)

Es verwendet Transaktionsdaten und stellt eine Gesamtübersicht zu unternehmensweiten Umsatzahlen und eine Aufschlüsselung des Einkaufsergebnisses für Debitoren und Produkte zur Verfügung. Berichte zeigen Änderungen im Einkauf, der im Zeitverlauf aufwendet. Daher kann der Bericht dazu verwendet werden, um Manager über die positiven und negativen Ausgabentrends für einzelne Kreditoren und Produkten zu warnen. Diagramme zeigen zusätzlich Einkaufsausgaben für unterschiedliche Beschaffungskategorien und Kreditorengruppen an. Deshalb können Kategorie- und Regional-Manager die Diagramme nutzen, um Änderungen im Ausgabenverhalten zu identifizieren.

## <a name="accessing-the-power-bi-content"></a>Zugreifen auf den Power BI-Inhalt
Der **Einkaufs- und Ausgabenanalyse** Power BI-Inhalt wird auf der **Einkaufsausgabenanalyse**-Seit angezeigt (**Beschaffung** \> **Abfragen und Berichte** \> **Einkaufleistungsanalyse** \> **Einkaufs- und Ausgabenanalyse**).

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Metriken, die im Power BI-Inhalt enthalten sind
Der **Einkaufs- und Ausgabenanalyse** Power BI-Inhalt enthält einen Bericht, der aus einem Satz Metriken besteht. Diese Metrik werden als Diagramme, Kacheln und Tabellen visuell dargestellt. 

Die folgenden Abschnitte bieten eine Übersicht über die Visualisierungen.

### <a name="purchase-by-vendor-report-page"></a>Berichtsseite „Einkauf nach Kreditor“
**Diagramme**
- Top 10 Kreditoren nach Einkauf (gestapeltes Balkendiagramm)
- Gesamte Bestellung nach Kreditorengruppe/Land/Name (Kreisdiagramm)
- Gesamte Einkauf nach Kreditorengruppe/Land/Name (Spaltendiagramm)
- Durchschnittlicher Einkauf nach Kreditorengruppe/Land/Name (Spaltendiagramm)

**Kacheln**
- Gesamter Einkauf
- YOY-Einkaufzunahme
- Kreditoren insgesamt
- Summe aktive Kreditoren

**Beispiel**
<img src="media/spend1.PNG" alt="Purchase by vendor">

### <a name="purchase-by-product-report-page"></a>Berichtsseite „Einkauf nach Produkt“

**Diagramme**
- Bestellung nach Beschaffungskategorie Produktnamen (Tortendiagramm)
- Gesamteinkauf nach Beschaffungskategorie Produktnamen (Tortendiagramm)
- Top 10 Produkte nach Einkauf (gestapeltes Balkendiagramm)

**Kacheln**
- Produkte gesamt</li>
- Gesamtanzahl der aktiven Produkte und Gesamtprozentsatz der Produkte
- Zahl der Produkte, die zu 80% Einkauf betragen

**Beispiel**


<img src="media/purchaseByProduct.PNG" alt="Purchase by Product">

### <a name="purchase-by-period-report-page"></a>Berichtsseite „Einkauf nach Zeitraum“
Diese Seite zeigt Einkäufe dieser und des letzten Jahres und den Wachstum nach Beschaffungskategorie.

**Diagramme** 
- Einkauf nach Monat/Tag (Spaltendiagramm)
- Kumulative Abweichung des Einkaufs YOY (Wasserfalldiagramm)
- Gesamte Zunahme des Einkaufs YOY (Spaltendiagramm)
- Beschaffungsauszug (Matrix)

**Kacheln**
- YOY-Einkaufzunahme
- YOY-Einkaufzunahme %

**Beispiel**
<img src="media/purchaseByPeriod.PNG" alt="Purchase by Period">

### <a name="purchase-by-vendor-location-report-page"></a>Berichtsseite „Einkauf nach Kreditorstandort“

**Diagramme**
- Einkauf nach Ort
- YOY-Einkaufzunahme %
- Einkauf nach Land

**Beispiel**
<img src="media/purchByVendorLocation.PNG" alt="Purchase by Vendor Location">

### <a name="purchase-spend-analysis-by-time-report-page"></a>Berichtsseite „Einkaufausgabenanalyse nach Zeit“

**Diagramme** 
- Einkauf aktuelles Jahr nach Monat/Tag (Liniendiagramm)
- Einkauf aktuelles und letztes Jahr (Linien und Spaltendiagramm)

**Beispiel**
<img src="media/PurchByTIme.PNG" alt="Purchase by Time">

### <a name="purchase-spend-analysis-by-vendor-report-page"></a>Berichtsseite „Einkaufausgabenanalyse nach Kreditor“

**Diagramme** 
- Top 10 % der Bestellung (Trichter)
- Top 10-Kreditoren mit erhöhtem Ausgaben YOY
- Top 10-Kreditoren mit verringerten Ausgaben YOY

**Beispiel** 
<img src="media/PurchSpendAnalysisByVendor.PNG" alt="Purchase spend by vendor">


## <a name="data-model-and-entities"></a>Datenmodell und Entitäten
Die folgenden Daten werden verwendet, um die Berichtsseiten im Power BI-Inhalt im **Einkaufs- und Ausgabenanalyse** Power BI-Inhalt auszufüllen. Diese Daten werden als gesamte Messungen dargestellt, die im Entitätsshop bereitgestellt werden. Der Entitätsshop ist eine Microsoft SQL Server-Datenbank, die für die Analyse optimiert ist. Weitere Informationen finden Sie in der [Übersicht Power BI-Integration mit Entitätsspeicher](power-bi-integration-entity-store.md).

Die aggregierenden Messungen in diesem Inhalt sind die Teilmenge der aggregierenden Messungen, die im Purchase Cube in Microsoft Dynamics AX 2012 und Microsoft Dynamics AX 2012 R3 verfügbar waren. Um die Cube-Messungen im Entitätsspeicher bereitzustellen, müssen Sie diese bereitstellbar machen. Weitere Informationen finden Sie im Verfahren für die Bereitstellung aggregierender Messungen im Entitäts-Shop unter [Übersicht über die Power BI-Integration mit Entität-Shop](power-bi-integration-entity-store.md). Die folgenden aggregierten Messungen der Rechnungspositionsentität werden als Grundlage des Inhaltspakets verwendet.

| Entität        | Zentrale aggregierte Messungen | Datenquelle                                 | Feld              | Beschreibung                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| Rechnungspositionen | Einkauf                   | VendInvoiceTrans                            | SUM(LineAmountMST) | Der Betrag in der Buchhaltungswährung. |

Die folgende Tabelle zeigt die wichtigen Messungen im Inhalt, die aus der Rechnungspositionsentität berechnet werden.

| Kennzahl               | Herstellkostenkalkulation                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| Einkauf aktuelles Jahr | Einkauf aktuelles Jahr = SUM('Invoice lines'\[Purchase\])                                            |
| Einkauf letztes Jahr    | Einkauf letztes Jahr = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\])) |
| YOY-Einkaufzunahme   | YOY-Einkaufzunahme = \[Purchase current year\] – \[Purchase last year\]                            |

Die folgenden wichtigen Dimensionen im Inhaltspaket werden als Filter verwendet, um die aggregierten Messungen zu teilen, um eine größere Granularität zu erreichen und tiefere und analytische Einblicke bereitzustellen.

| Entität                 | Beispiele für Attribute                                |
|------------------------|-------------------------------------------------------|
| Lieferanten                | Kreditorengruppen-, Kreditorregionen oder Land, Kreditorname |
| Produkte               | Produktnummer, Produktname, Artikelgruppenname        |
| Beschaffungskategorien | Beschaffungskategorie, Beschaffungskategorienamen      |
| Juristische Personen         | Name der juristischen Person                                     |
| Daten                  | Daten, Jahresausgleich                                    |

Standardmäßig zeigt das Inhaltspaket Daten während des laufenden Kalenderjahrs an. Allerdings können Sie den im Berichtsfilterabschnitt Datumsfilter ändern. Sie können das den Unternehmensfilter auch ändern.
