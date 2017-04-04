---
title: "Vertriebs-und Rentabilitätsleistung Leistungsfähigkeit BIinhalt"
description: "In diesem Thema wird beschrieben, was im Dynamics 365 - zufriedenes Pack für Arbeitsgänge des Vertriebs und der Rentabilitätsleistung für Microsoft-Energie BI enthalten ist. Es erläutert, wie auf die Berichte, die im Paket enthalten inhaltliche sind und enthält Informationen zum Datenmodell und die Entitäten, die verwendet werden, um das Inhaltstext Pack zu erstellen."
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
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 3e6b48768bb8e69d46f1555d9300f3b878b01ff1
ms.lasthandoff: 03/31/2017


---

# <a name="sales-and-profitability-performance-power-bi-content"></a>Vertriebs-und Rentabilitätsleistung Leistungsfähigkeit BIinhalt

In diesem Thema wird beschrieben, was im Dynamics 365 - zufriedenes Pack für Arbeitsgänge des Vertriebs und der Rentabilitätsleistung für Microsoft-Energie BI enthalten ist. Es erläutert, wie auf die Berichte, die im Paket enthalten inhaltliche sind und enthält Informationen zum Datenmodell und die Entitäten, die verwendet werden, um das Inhaltstext Pack zu erstellen.

<a name="overview"></a>Überblick
--------

Dies Inhaltstext Pack wurde erstellt, sodass Verkaufsleiter schließlich die eigentliche Vertriebsmetrik des Umsatzerlöses, des Bruttogewinns und der Ränder überwachen. Es verwendet - Transaktionsdaten vornehmen des Vertriebs von Microsoft Dynamics 365 für Arbeitsgänge und stellt eine gesamte wertberichtigt unternehmensweiten Shoppersonals und eine Aufschlüsselung des Verkaufsergebnisses für Debitoren und Produkte zur Verfügung. Durch das Hervorheben, wird Umsatzerlös und im Gewinn-Wachstum im Zeitverlauf, Berichte verwendet werden kann, um Manager über die positiven und negativen Trends für einzelne Debitoren und Produkte hinzuweisen. Kategorie und Manager regionale suchen es sinnvoll, Diagramme zu haben, mit der Umsatzerlöse und Rentabilität verschiedener Produktkategorien von Debitorengruppen und miteinander vergleichen, um Trödler und auszusortieren Füllzeichen. Ein Bericht, der umfassender einzelnen Umsatzerlös des Debitors mit Gewinnspanne zeichnet, bietet Account Managern eine Daten-unterstützte Basis an, um die Verkaufs- und Marketings-Aufwände dem Profil jedes abzustimmen jeweiligen Debitors. Der Inhaltstext Pack Verkäufen und der Rentabilitätsleistung aktiviert Verkaufsleiter Verkaufsleistung, um von zu analysieren:

-   Umsatzerlös, des laufenden Jahres (nach Debitorengruppen-, und Personendebitoren Verkaufskategorien und Einzelprodukte und bestimmte geografische Region)
-   Umsatzerlösänderung, jährlich (nach Debitorenregionen und -Verkaufskategorien)

Rentabilität kann wie folgt analysiert werden:

-   Bruttogewinn und Gewinnspanne (Comma-Separated Debitorengruppen und Produktverkaufskategorien)
-   Bruttogewinnänderung jährlich,
-   Debitorenrentabilität (nach Umsatz für Bruttogewinn)

## <a name="accessing-the-content-pack"></a>Zugreifen des das Content Packs
Der Inhaltstext Pack Vertriebs-und Rentabilitätsleistung Leistungsfähigkeit BI wird als Implementierungsanlage in den Lebenszyklus-Dienstleistungen (LCS) veröffentlicht und kann von Microsoft Dynamics 365 für Arbeitsgänge zugegriffen werden. Weitere Informationen dazu, wie BIberichte Energie, finden Sie auf zugreift und startet [Leistung in BIinhalt Kreditbriefen von Microsoft und von den Partnern] (power-bi-content-microsoft-partners.md ).

## <a name="metrics-included-in-the-content-pack"></a>Metrik enthalten inhaltliche Pack im
Der Inhaltstext Pack enthält einen Bericht, der einem Satz Metriken visuell dargestellt als Diagramme, Kacheln und Tabellen besteht. Die folgende Tabelle enthält eine Übersicht der im Visualisierungen das Content Pack.

|                        |                                            |                                                         |
|------------------------|--------------------------------------------|---------------------------------------------------------|
| ** Berichtsseite **        | **Charts**                                 | ** Kacheln **                                               |
| Umsatz nach Kunden    | Top 10 Debitoren nach Umsatzerlös                | Gesamtumsatz                                           |
|                        | Gesamtumsatzerlös nach Debitorengruppe            | YOY-Umstatzsteigerung                                      |
|                        | Durchschnittskundeumsatzerlös nach Debitorengruppe | Bruttogewinn                                            |
|                        | Umsatzerlös und Bruttogewinn nach Debitorengruppe.   |                                                         |
| Umsatzerlösnebenprodukt     | Umsatzerlös und Bruttogewinn nach Verkaufskategorie.   | - Gesamt \# von Produkten                                    |
|                        | Produkte nach Umsatzerlös Top 10                 | Gesamtanzahl aktive und Prozentsatz der Summe Produkte |
|                        | Nach Verkaufskategorie Gesamtumsatzerlös            | Produkte, die Nummer 80% betragen Umsatzerlös           |
| Umsatzerlös nach Periode \*    | Umsatzerlös nach Monat                           | YOY-Umstatzsteigerung                                      |
|                        | Nachfolgende Umsatzerlösabweichung, YOY             | YOY-Umstatzsteigerung %                                    |
|                        | Gesamte Verkaufsmengenabweichung nach Debitorenregion    |                                                         |
| Umsatzerlös nach Lagerplatz    | Nach Ort Umsatzerlöse                      |                                                         |
|                        | YOY-Umstatzsteigerung %                       |                                                         |
|                        | Umsatzerlöse nach Regionen                    |                                                         |
| Debitorenrentabilität | Bruttogewinn für Zinsausgaben, nach Debitor   | Bruttogewinn, Bruttogewinn, YOY-Umstatzsteigerung          |
| Rentabilitätsanalyse | Umsatzerlös und Bruttogewinn nach Monat          |                                                         |
|                        | 15 Debitoren der Bruttogewinn nach oben           |                                                         |
|                        | Bruttogewinn nach Monat, YOY                 |                                                         |

dieser \* Umsatzerlös und letzten Jahr und Wachstum nach Verkaufskategorie.

## <a name="understanding-the-data-model-and-entities"></a>Das Datenmodells und die Entitäten verstehen
Dynamics 365 für Arbeitsgangsdaten wird verwendet, um den Bericht im das Content Pack Verkäufen und der Rentabilitätsleistung aufzufüllen. Dieser wird als vollständige Messungen dargestellt, die im Entitätsshop bereitgestellt werden, der eine Microsoft SQL-Datenbank ist, die zwecks Analyse optimiert ist. Lesen Sie sich über dies im Blog [Power BI-Integration mit Entitäts-Shop in Dynamics]( https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/). Die gesamten Messungen in diesem das Content Pack sind die Teilmenge der gesamten Messungen, die im Vertriebs-Cuben in Dynamics AX 2012 und im AX 2012 R3 verfügbar waren. Zur Phase die gesamten Messungen des Cubes im Entitätsshop müssen Sie diese zur Bereitstellung geeignet ist. Weitere Informationen finden Sie unter in den Phasenaggregatsmessungen Vorgehensweise in den Entitätsshop im Blog [Power BI-Integration mit Entitäts-Shop in Dynamics] (https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/). Die folgenden Schlüsselaggregatsmessungen der Rechnungspositionsentität werden als Grundlage des das Content Packs verwendet.

|               |                                              |                                                 |                                              |                                          |
|---------------|----------------------------------------------|-------------------------------------------------|----------------------------------------------|------------------------------------------|
| **Entity**    | ** Gesamt Messungen des Schlüssels **               | ** Datenquelle für Dynamics 365 für Arbeitsgänge ** | **Field**                                    | **Description**                          |
| Rechnungspositionen | Umsatzerlös                                      | CustInvoiceTrans                                | SUMME (LineAmountMST)                           | Betrag in Buchhaltungswährung            |
|               | Wareneinsatz                           | InventTrans                                     | SUMME (CostAmountPosted + CostAmountAdjustment) | Einstandspreis + Anpassung                 |
|               | Betrag der Provisionsposition - Buchhaltungswährung | CustInvoiceTrans                                | SUMME (CommissAmountMST)                        | Provisionsbetrag in der Buchhaltungswährung |

Die folgende Tabelle zeigt die Tastenfunktionen gesamten Messungen der Rechnungspositionsentität angezeigt, die verwendet werden, um mehrere berechnete Kennzahlen das Content im Dataset des Packs zu erstellen.

|                   |                                                                                                  |
|-------------------|--------------------------------------------------------------------------------------------------|
| **Measure**       | ** Berechnet wie **                                                                                |
| Bruttogewinn      | SUMME – Umsatzerlös (COGS – Provision – Mehrwertsteuer einbezogen (im Debitorenrechnungspositions Minderbetrag))          |
| Bruttogewinn      | SUMME (Bruttogewinn/(Umsatzerlös - Mehrwertsteuer einbezogen (im Debitorenrechnungspositions Mehrbetrag)))             |
| Umsatzerlösletztes des | Umsatzerlösletztes des BERECHNEN = (SUMME ('Rechnung lines'entity_PLACEHOLDER \ [Umsatzerlös \], SAMEPERIODLASTYEAR Datumsangaben\[\](\[\] |

Die folgenden wichtigen Dimensionen in Vertriebscube ** ** werden als Filter verwendet, um die gesamten Messungen ein Crossdocking, um größere Granularität und analytische tiefere Einblicke zu erreichen.

|                  |                                                      |
|------------------|------------------------------------------------------|
| **Entity**       | ** Beispiele für Attribute **                           |
| Debitoren        | Debitorengruppen, Debitorenregionen, Adresse, Industrie |
| Produkte         | Produktnummer, Produktname, Artikelgruppenname       |
| Verkaufskategorien | Verkaufskategorienamen                                 |
| Juristische Personen   | Namen der juristischen Person                                   |
| Daten            | Daten                                                |

Standardmäßig zeigt das Inhaltstext Pack Daten während des laufenden Kalenderjahr angezeigt, aber Sie können den Berichtsfilterabschnitt den Datumsfilter öffnen und ändern. Sie können den Unternehmensfilter auch ändern.

## <a name="additional-resources"></a>Zusätzliche Ressourcen
Nachfolgend finden Sie einige hilfreiche Links zum Thema Entitäten und Erstellen von Power BI-Inhalten:

-   [Datenentitäten](..\data-entities\data-entities.md)
-   [Erstellen von Organisations-Inhaltspaketen](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Datenmodellierung mithilfe von Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Hinzufügen von Power BI-Kacheln zu Arbeitsbereichen](configure-power-bi-integration.md)



