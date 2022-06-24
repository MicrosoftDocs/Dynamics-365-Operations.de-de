---
title: Power BI-Inhalt zur Lagerortleistung
description: In diesem Artikel wird beschrieben, was im Warehouse Performance Power BI Inhalt enthalten ist.
author: Mirzaab
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWarehousePerformancePowerBI
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 272953
ms.assetid: 4e4d4323-78cf-4ffa-8d5a-05e856c33db6
ms.search.region: Global
ms.author: mirzaab
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: d43cef4970cdf180d0db39086220def56b08f280
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8851921"
---
# <a name="warehouse-performance-power-bi-content"></a>Power BI-Inhalt zur Lagerortleistung

[!include [banner](../includes/banner.md)]

In diesem Artikel wird beschrieben, was im **Warehouse Performance** Microsoft Power BI-Inhalt enthalten ist. Es erläutert, wie Sie auf die Power BI-Berichte zugreifen und enthält Informationen zum Datenmodell und zu den Entitäten, die verwendet werden, um den Inhalt zu erstellen.

## <a name="overview"></a>Übersicht

Der Power BI Inhalt **Lagerortleistung** wurde erstellt, damit Lagerort und Betriebsleiter wichtige eingehende und ausgehende Bestandmetriken überwachen können. Er verwendet Lagerortverwaltung, Produkt und andere Transaktionsdaten von Ihrem System und stellt eine gesamte Ansicht der Lagerortleistung und eine Aufschlüsselung für Kreditoren, Produktgruppen, Produkte und Standort und Lagerorte bereit.

Lagerortverwaltung kann den Power BI Inhalt **Lagerortleistung** verwenden, um die folgenden drei Bereiche zu messen:

- **Eingehende Leistung** – Misst, wie gut ein Lieferant gegenüber dem Kunden ist (das heißt, misst die Lieferleistung) und misst die Erfüllungsleistung, damit Sie Probleme, die Arbeitskräfte oder Artikel über einen Zeitraum berücksichtigen, identifizieren können. Es ist wichtig, dass Sie rechtzeitig wissen, ob Kreditoren rechtzeitig, früh oder zu spät liefern, damit Sie bestimmen können, wie die Leistung des Kunden die Gesamtleistung beeinflusst. Ein Kreditor, der außerhalb der vereinbarten Daten liefert, kann zusätzlichen Druck auf den Lagerort ausüben, weil unerwartete Arbeit entstehen kann und die Durchschnittliche Lagerzeit sich verändert.
- **Versandleistung** – Misst, ob Ihr Lagerort vollständig oder in Teilen an Debitoren versendet (das heißt, misst die Versand und Lieferleistung), sodass mögliche Probleme mit Produkten, Standorten oder Lagerorten erkannt werden können. Wenn Sie feststellen, dass der Versand in bestimmte Bereiche oder Städte zu spät erfolgt, müssen Sie möglicherweise mehr Aufmerksamkeit für Transporte oder Kundenbetreuung aufwenden.
- **Lagerplatzbestandsrichtigkeit** – Bestandsrichtigkeit ist eine wichtige interne Lagerort-Business Intelligence (BI). Es ist außerordentlich wichtig, dass Sie bestimmen, wie genau Sie im Allgemeinen zählen. Es ist allerdings auch wichtig, dass Sie bestimmen, wie genau Sie Artikel an den richtigen Lagerplätzen speichern und dass Sie Abweichungsdaten markieren, damit Sie eine Position für Artikel oder eine eingeleitete gesamte Inventur für bestimmte Artikel suchen können. (Aktuell wird die neue elementbasierte Inventurfunktion als Hotfix geliefert.) Wenn Sie diesen Power BI Inhalt verwenden, um die Korrektheit der verfügbaren Lagerbestanddaten pro Standort zu bestimmen, können Sie auch Diebstähle in Ihren Geschäften identifizieren. Sie können außerdem bestimmen, ob Lagerplätze verfügbare Mengen haben, die von den Enterprise Ressourcenplanungsdaten (ERP) abweichen. Diese Lagerplätze sind möglicherweise zu groß, oder sie können möglicherweise nicht gezählt werden. Alternativ könnten einige physische Positionen ungültig sein, damit ist es schwierig, einen einzelnen Artikeltyp in Einklang mit verfügbaren Daten zu halten.

## <a name="accessing-the-power-bi-content-pack"></a>Zugreifen auf das Power BI-Inhaltspaket
Die **Lagerhausleistung** Power BI-Inhalt wird in der **Lagerhausleistung** angezeigt (**Lagerhausverwaltung** \> **Abfragen und Berichte** \> **Produktionsleistungsanalyse** \> **Lagerhausfluss**).

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Metriken, die im Power BI-Inhalt enthalten sind
Die **Lagerortleistung** Power BI Inhalt enthält einen Bericht. Dieser Bericht enthält einen Satz Metriken, die als Diagramme, Kacheln und Tabellen visuell dargestellt werden. Die folgende Tabelle enthält eine Übersicht der Visualisierungen im Power BI-Inhalt zu **Lagerhausleistung**.

| Berichtsseiten                 | Diagramme                                   | Beschreibung |
|-----------------------------|------------------------------------------|-------------|
| Eingehende Leistung         | Summe Lager                          | Die Anzahl von Arbeitspositionen, die in einer bestimmten Zeit verarbeitet werden. |
| Eingehende Leistung         | Durchschnittliche Lagerzeit                    | Die durchschnittliche Zeit, in Stunden, für alle Bestellpositionen, die verarbeitet werden, von der Registrierung der Artikel bis zum zuletzt verarbeiteten Artikels. |
| Eingehende Leistung         | Vorzeitig empfangen                           | Die Anzahl der Bestellpositionen, die frühzeitig eingehen. |
| Eingehende Leistung         | Rechtzeitig empfangen                         | Die Anzahl der Bestellpositionen, die rechtzeitig eingehen. |
| Eingehende Leistung         | Verspätet empfangen                            | Die Anzahl der Bestellpositionen, die spät eingehen. |
| Eingehende Leistung         | Rechtzeitig durch Lieferant                        | Eine Ansicht des Prozentsatzes der Bestellpositionen, die von einem Kreditor oder einer Kreditorengruppe früh, verspätet und rechtzeitig empfangen werden. |
| Eingehende Leistung         | Rampe um durchschnittlichen Bestand zu lagern (Stunden) | Der durchschnittliche Bestand zum Lagern in Stunden im Zeitverlauf. |
| Eingehende Leistung         | Durchschnittliche Einlagerung durch Arbeitskraft               | Die durchschnittliche Zeit, in Stunden, die eine Arbeitskraft gebraucht hat, um Bestellpositionen für die Einlagerung zu verarbeiten. |
| Eingehende Leistung         | Durchschnitt der Einlagerungsstunden nach Kreditor          | Die durchschnittliche Einlagerungszeit in Stunden durch den Lieferant oder die Lieferantengruppe. |
| Eingehende Leistung         | Durchschnitt der Einlagerungsstunden nach Produkt         | Die durchschnittliche Einlagerungszeit in Stunden nach Artikel oder Artikelgruppe. |
| Lagerortbestandgenauigkeit | Gesamtzahl                              | Die Anzahl von Arbeitspositionen, die in einer bestimmten Zeit verarbeitet werden. |
| Lagerortbestandgenauigkeit | Abweichungssatz                         | Der gesamte Abweichungssatz als Prozentsatz aller Positionen, die für eine Periode bewertet werden. |
| Lagerortbestandgenauigkeit | Anzahl ohne Abweichung                | Von der Gesamtanzahl von Inventurarbeitspositionen, die verarbeitet wurden, die Anzahl der Positionen, die ohne jegliche Abweichung verarbeitet werden. |
| Lagerortbestandgenauigkeit | Artikel im Zeitverlauf gezählt                  | Der Prozentsatz von Artikeln, die mit und ohne Abweichung im Zeitverlauf gezählt werden. |
| Lagerortbestandgenauigkeit | Größer als Artikelmengeabweichung % | Eine Tabellenansicht von Inventurpositionen, die Abweichungen haben, die einen angegebenen Prozentsatz überschreitet. Die Tabelle enthält Informationen über Artikel, durchschnittlicher Abweichung der Lagerplätze, Inventurarbeitspositionen, die berechnet werden, Nummern-Inventurpositionen, die Abweichungen für den Speicherort haben, durchschnittlichen Menge, die berechnet wird, voraussichtliche Gesamtmenge, die berechnet wird, und tatsächliche Artikelmenge, die berechnet wird. |
| Lagerortbestandgenauigkeit | Artikelzählung nach Arbeitskraft                     | Die Inventurleistung der Arbeitskräfte. Leistung wird als Prozentsatz der Inventurarbeitspositionen mit und ohne Abweichungen ausgedrückt. |
| Lagergenauigkeit nachverfolgen | Artikelanzahl nach Standort/Lagerort           | Inventurleistung abhängig von verarbeiteten Inventurarbeitspositionen nach Standort und Lagerort, die Abweichungen enthalten und ausschließen. |
| Lagerortbestandgenauigkeit | Abweichungssatznebenprodukt              | Der Abweichungssatz für einen Inventurauftrag der Leistung. Der Zinssatz wird als Prozentsatz der Inventurarbeitspositionen verarbeitet und nach Artikel oder nach Artikelgruppe ausgedrückt. |
| Versandleistung        | Positionen versendet                            | Die Gesamtanzahl der Lieferpositionen, die über eine bestimmte Zeitperiode versendet werden. |
| Versandleistung        | Vorzeitig                                    | Der Prozentsatz von Lieferpositionen, die frühzeitig versendet werden. |
| Versandleistung        | Termingerecht                                  | Der Prozentsatz von Lieferpositionen, die vereinbarungsgemäß versendet werden. |
| Versandleistung        | Verspätet                                     | Der Prozentsatz von Lieferpositionen, die zu spät versendet werden. |
| Versandleistung        | Lieferungen im Zeitverlauf                      | Der Prozentsatz von Lieferpositionen, die pünktlich, früh oder zu spät über eine bestimmte Zeitperiode versendet werden. Eine Trendlinie zeigt den Trend für Positionen an, die pünktlich versendet werden. |
| Versandleistung        | Spät versendet nach Ort                     | Eine Zuordnungsvisualisierung von Orten und Bereiche, die von Lieferungen zu spät betroffen sind. |
| Versandleistung        | Versand nach Produkt                       | Der Prozentsatz, der frühzeitig rechtzeitig oder zu spät versandt wurde, nach Artikel oder Artikelgrupp, |
| Versandleistung        | Geliefert an Debitoren                      | Der Prozentsatz, der frühzeitig rechtzeitig oder zu spät versandt wurde, nach Artikel oder Artikelgrupp, |
| Versandleistung        | Nach Standort/Lagerort Versendet              | Der Prozentsatz, der frühzeitig rechtzeitig oder zu spät versandt wurde, nach Artikel oder Artikelgrupp, |

## <a name="understanding-the-data-model-and-calculations"></a>Das Datenmodells und Berechnungen verstehen
Die folgenden Daten werden verwendet, um die Berichtsseiten im Power BI-Inhalt **Lagerortleistung** auszufüllen. Diese Daten werden als gesamte Messungen dargestellt, die im Entitätsshop bereitgestellt werden. Der Entitätsshop ist eine Microsoft SQL Server-Datenbank, die für die Analyse optimiert ist. Weitere Informationen finden Sie unter [Power BI Integration mit Entity Store](power-bi-integration-entity-store.md).

Die folgenden aggregierten Messungen werden als Grundlage des Inhaltspakets verwendet.

| Berichtsseiten                 | Diagramme                                   | Tabellen                                | Berechnungsbeschreibungen |
|-----------------------------|------------------------------------------|---------------------------------------|--------------------------|
| Leistungsinformationen         | Summe einlagern                          | WHSWorkLine                           | Die Anzahl von Arbeitspositionen, in denen der Arbeitstyp **gesetzt** ist. |
| Leistungsinformationen         | Durchschnittliche Lagerzeit                    | WHSWorkLine                           | Die Summe der Arbeitspositionen der maximalen Zeit, geteilt durch die Anzahl der Arbeitspositionen der maximalen Zeit, wenn die Arbeitspositionen die maximale Differenz zwischen dem Arbeiten erstellten Datum und dem abgeschlossenen Datum ist. |
| Eingehende Leistung         | Vorzeitig empfangen                           | WHSWorkLine                           | Die Anzahl von Arbeitspositionen, in denen die Arbeit das Erstellungsdatum erstellt, licht nach dem verwendeten Lieferdatum. Wenn das bestätigte Versanddatum nicht festgelegt ist, verwenden sie das angeforderte Lieferdatum. |
| Leistungsinformationen         | Rechtzeitig empfangen                         | WHSWorkLine                           | Die Anzahl von Arbeitspositionen, in denen die Arbeit das Erstellungsdatum erstellt, ist gleich wie das verwendete Lieferdatum. Wenn das bestätigte Versanddatum nicht festgelegt ist, verwenden sie das angeforderte Lieferdatum. |
| Eingehende Leistung         | Verspätet empfangen                            | WHSWorkLine                           | Die Anzahl von Arbeitspositionen, in denen die Arbeit das Erstellungsdatum erstellt, liegt nach dem verwendeten Lieferdatum. Wenn das bestätigte Versanddatum nicht festgelegt ist, verwenden sie das angeforderte Lieferdatum. |
| Eingehende Leistung         | Rechtzeitig durch Lieferant                        | WHSWorkLine                           | Früh erhalten, rechtzeitig erhalten und verspätet erhalten (siehe Beschreibungen oben in dieser Tabelle). |
| Eingehende Leistung         | Rampe um durchschnittlichen Bestand zu lagern (Stunden)   | WHSWorkLine                           | Enthält die durchschnittliche Zeit (siehe Beschreibung weiter oben in dieser Tabelle). |
| Eingehende Leistung         | Durchschnittliche Einlagerung durch Arbeitskraft               | WHSWorkLine                           | Enthält die durchschnittliche Zeit (siehe Beschreibung weiter oben in dieser Tabelle). |
| Eingehende Leistung         | Durchschnitt der Einlagerungsstunden nach Kreditor          | WHSWorkLine                           | Enthält die durchschnittliche Zeit (siehe Beschreibung weiter oben in dieser Tabelle). |
| Eingehende Leistung         | Durchschnitt der Einlagerungsstunden nach Produkt         | WHSWorkLine                           | Enthält die durchschnittliche Zeit (siehe Beschreibung weiter oben in dieser Tabelle). |
| Lagerortbestandgenauigkeit | Gesamtzahl                              | WHSWorkLineCycleCount                 | Inventur, wenn die absolute Abweichungsmenge gleich oder größer als 0 (null )ist. |
| Lagerortbestandgenauigkeit | Abweichungssatz                         | WHSWorkLineCycleCount                 | Inventur, die Abweichungen haben, geteilt durch die Gesamtanzahl. Eine Inventur hat Abweichungen, wenn die absolute Inventurmenge mehr als 0 (null ) beträgt. |
| Lagerortbestandgenauigkeit | Anzahl ohne Abweichung                | WHSWorkLineCycleCount                 | Inventur, wenn die absolute Abweichungsmenge gleich oder größer als 0 (null )ist. |
| Lagerortbestandgenauigkeit | Anzahl mit Abweichung                   | WHSWorkLineCycleCount                 | Inventur, wenn die absolute Abweichungsmenge gleich 0 (null )ist. |
| Lagerortbestandgenauigkeit | Artikel im Zeitverlauf gezählt                  | WHSWorkLineCycleCount                 | Anzahl ohne Abweichung und Anzahl mit Abweichung (vgl. Beschreibungen weiter oben in dieser Tabelle). |
| Lagerortbestandgenauigkeit | Größer als Artikelmengeabweichung % | WHSWorkLineCycleCount                 | Die durchschnittliche Abweichung ist die absolute Abweichungsmenge, die durch die erwartete Menge verteilt wird, wobei die absolute Abweichungsmenge mehr als 0 (null )ist. Die durchschnittliche Abweichung ist die absolute Abweichungsmenge, die durch die erwartete Menge verteilt wird, wobei die absolute Abweichungsmenge mehr als 0 (null )ist. Zählen Sie mit Abweichungen, Gesamtanzahl, erwartete Menge und gezählte Menge, in der die gesamte Menge nach Artikel und Lagerplatz gruppiert ist (siehe Beschreibungen oben in dieser Tabelle). |
| Lagerortbestandgenauigkeit | Artikelzählung nach Arbeitskraft                     | WHSWorkLineCycleCount                 | Anzahl ohne Abweichung und Anzahl mit Abweichung (siehe Beschreibungen weiter oben in dieser Tabelle). |
| Lagerortbestandgenauigkeit | Artikelanzahl nach Standort/Lagerort           | WHSWorkLineCycleCount                 | Anzahl ohne Abweichung und Anzahl mit Abweichung (siehe Beschreibungen weiter oben in dieser Tabelle). |
| Lagerortbestandgenauigkeit | Abweichungssatznebenprodukt              | WHSWorkLineCycleCount                 | Abweichungssatz (siehe Beschreibung weiter oben in dieser Tabelle). |
| Versandleistung        | Positionen versendet                            | SalesLine               | Die Anzahl der Auftragspositionen, in denen Auftragspositionen geliefert werden. |
| Versandleistung        | Vorzeitig                                    | CustPackingSlipOnTimeStatus           | Verkaufspositionen, wo der Versanddatumstatus **1 (früher)** ist. Früh bedeutet, dass das Versanddatum des Lieferscheins früher als das bestätigte Lieferdatum der Verkaufsposition ist. Wenn das bestätigte Versanddatum nicht festgelegt ist, verwenden sie das angeforderte Lieferdatum. |
| Versandleistung        | Termingerecht                                  | CustPackingSlipOnTimeStatus           | Verkaufspositionen, wo der Versanddatumstatus **2 (Rechtzeitig)** ist. Rechtzeitig bedeutet, dass das Versanddatum des Lieferscheins dem bestätigten Lieferdatum der Verkaufsposition entspricht. Wenn das bestätigte Versanddatum nicht festgelegt ist, verwenden sie das angeforderte Lieferdatum. |
| Versandleistung        | Verspätet                                     | CustPackingSlipOnTimeStatus           | Verkaufspositionen, wo der Versanddatumstatus **3 (spät)** ist. Spät bedeutet, dass das Versanddatum des Lieferscheins früher als das bestätigte Lieferdatum der Verkaufsposition ist. Wenn das bestätigte Versanddatum nicht festgelegt ist, verwenden sie das angeforderte Lieferdatum. |
| Versandleistung        | Lieferungen im Zeitverlauf                      | SalesLine CustPackingSlipOnTimeStatus | Aufträge, die vollständig geliefert werden, wenn die gesamte Menge der Verkaufsposition, zuzüglich früh, rechtzeitig, spät versendet wurde, und den Beschreibungen (siehe oben in dieser Tabelle). |
| Versandleistung        | Spät versendet nach Ort                     | CustPackingSlipOnTimeStatus           | Spät (siehe Beschreibung weiter oben in dieser Tabelle). |
| Versandleistung        | Versand nach Produkt                       | CustPackingSlipOnTimeStatus           | Früh, rechtzeitig und verspätet erhalten (siehe Beschreibungen oben in dieser Tabelle). |
| Versandleistung        | Geliefert an Debitoren                      | CustPackingSlipOnTimeStatus           | Früh, rechtzeitig und verspätet erhalten (siehe Beschreibungen oben in dieser Tabelle). |
| Versandleistung        | Nach Standort/Lagerort Versendet              | CustPackingSlipOnTimeStatus           | Früh, rechtzeitig und verspätet erhalten (siehe Beschreibungen oben in dieser Tabelle). |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]