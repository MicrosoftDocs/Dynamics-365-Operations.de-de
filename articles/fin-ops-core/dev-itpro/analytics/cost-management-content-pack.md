---
title: Power BI-Inhalt zur Kostenverwaltung
description: In diesem Thema wird beschrieben, was im Power BI-Inhalt zur Kostenverwaltung enthalten ist.
author: ShylaThompson
manager: AnnBe
ms.date: 03/16/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 270314
ms.assetid: 9680d977-43c8-47a7-966d-2280ba21402a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6bd76fc771c370d8d769a97d3b33003f632717f2
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174189"
---
# <a name="cost-management-power-bi-content"></a>Power BI-Inhalt zur Kostenverwaltung

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Übersicht

Der Microsoft Power BI-Inhalt für **Kostenmanagement** ist für Bestandsbuchhalter oder Einzelpersonen in der Organisation bestimmt, die für den Status "Bestand" oder "Ressource in Bearbeitung (RIF)" zuständig oder daran interessiert sind oder die für die Analyse von standardmäßigen Kostenabweichungen zuständig oder daran interessiert sind.

> [!NOTE]
> Der Power BI-Inhalt zur **Kostenverwaltung**, der in diesem Thema beschrieben wird, gilt für Dynamics 365 Finance and Operations 8.0.
> 
> Das Power BI-Inhaltspaket zur **Kostenverwaltung**, das auf der AppSource-Site verfügbar ist, ist veraltet. Weitere Informationen zu dieser Veraltung finden Sie unter [Power BI-Inhaltspakete, die auf AppSource verfügbar sind](../migration-upgrade/deprecated-features.md#power-bi-content-packs-available-on-appsource).

Dieser Power BI-Inhalt bietet ein kategorisiertes Format, mit dessen Hilfe Sie die Leistung von Beständen überwachen können und visuell darstellen können, wie Kosten durch sie fließen. Sie können Verwaltungseinblicke erhalten, wie das Umsatzverhältnis, die Anzahl von Tagen, während der der Bestand verfügbar ist, die Genauigkeit sowie die „ABC-Klassifizierung” auf Ihrer bevorzugten aggregierten Ebene (Untenehmen, Artikel, Artikelgruppe oder Standort). Die verfügbar gemachten Informationen können auch als detaillierte Ergänzung der Finanzaufstellung verwendet werden.

Der Power BI-Inhalt wird auf Grundlage der aggregierten Messung **CostObjectStatementCacheMonthly** erstellt, wobei die Tabelle **CostObjectStatementCache** die primäre Datenquelle ist. Diese Tabelle wird durch das Datensatzcacheframework verwaltet. Standardmäßig wird die Tabelle alle Stunden 24 aktualisiert, aber Sie können die Aktualisierungshäufigkeit ändern oder manuelle Aktualisierungen in der Konfiguration des Datensatzcaches aktivieren. Manuelle Aktualisierungen können entweder im Arbeitsbereich **Kostenverwaltung** oder im Arbeitsbereich **Kostenanalyse** ausgeführt werden.

Nach jeder Aktualisierung der Tabelle **CostObjectStatementCache** muss die aggregierte Messung **CostObjectStatementCacheMonthly** aktualisiert werden, bevor Daten in den Power BI-Visualisierungen aktualisiert werden.

## <a name="accessing-the-power-bi-content"></a>Zugreifen auf den Power BI-Inhalt

Der Power BI-Inhalt zur **Kostenverwaltung** wird in den Arbeitsbereichen **Kostenverwaltung** und **Kostenanalyse** angezeigt.

Der Arbeitsbereich **Kostenverwaltung** enthält die folgenden Registerkarten:

- **Übersicht** – Auf dieser Registerkarte werden Anwendungsdaten angezeigt.
- **Bestandsbuchhaltung – Status** – Auf dieser Registerkarte wird Power BI-Inhalt angezeigt.
- **Fertigungsbuchhaltung – Status** – Auf dieser Registerkarte wird Power BI-Inhalt angezeigt.

Der Arbeitsbereich **Kostenanalyse** enthält die folgenden Registerkarten:

- **Übersicht** – Auf dieser Registerkarte werden Anwendungsdaten angezeigt.
- **Bestandsbuchhaltung – Analyse** – Auf dieser Registerkarte wird Power BI-Inhalt angezeigt.
- **Fertigungsbuchhaltung – Analyse** – Auf dieser Registerkarte wird Power BI-Inhalt angezeigt.
- **Standardkostenabweichungsanalyse** – Auf dieser Registerkarte wird Power BI-Inhalt angezeigt.

## <a name="report-pages-that-are-included-in-the-power-bi-content"></a>Berichtsseiten, die im Power BI-Inhalt enthalten sind

Der Power BI-Inhalt zur **Kostenverwaltung** enthält einen Satz von Berichtsseiten, die aus einem Satz von Metriken bestehen. Diese Metrik werden als Diagramme, Kacheln und Tabellen visuell dargestellt. 

Die folgende Tabelle bietet eine Übersicht der Visualisierungen im Power BI-Inhalt zur **Kostenverwaltung**.

### <a name="inventory-accounting-status"></a>Bestandsbuchhaltung – Status

| Berichtsseiten                               | Darstellung                                   |
|-------------------------------------------|-------------------------------------------------|
| Lager (Überblick)                        | Anfangssaldo                               |
|                                           | Nettoveränderung                                      |
|                                           | Nettoveränderung in %                                    |
|                                           | Endsaldo                                  |
|                                           | Lagergenauigkeit                              |
|                                           | Verhältniszahl für Lagerumschlag                        |
|                                           | Lagerbestandsverfügbarkeit in Tagen                          |
|                                           | Aktives Produkt in Periode                        |
|                                           | Aktive Kostenträger in Periode                   |
|                                           | Saldo nach Artikelgruppe                           |
|                                           | Saldo nach Standort                                 |
|                                           | Aufstellung nach Kategorie                           |
|                                           | Nettoveränderung nach Quartal                           |
| Bestandsübersicht nach Standort und Artikelgruppe | Lagerbestandsgenauigkeit nach Standort                      |
|                                           | Lagerumschlagverhältnis nach Standort                |
|                                           | Lagerbestandsendsaldo nach Standort                |
|                                           | Lagerbestandsgenauigkeit nach Artikelgruppe                |
|                                           | Lagerumschlagverhältnis nach Artikelgruppe          |
|                                           | Lagerbestandsendsaldo nach Standort und Artikelgruppe |
| Lageraufstellung                       | Lageraufstellung                             |
| Lagerbestandsaufstellung nach Standort               | Lagerbestandsaufstellung nach Standort                     |
| Lagerbestandsaufstellung nach Produkthierarchie  | Lageraufstellung                             |
| Lagerbestandsaufstellung nach Produkthierarchie  | Lagerbestandsaufstellung nach Standort                     |

### <a name="manufacturing-accounting-status"></a>Fertigungsbuchhaltung – Status

| Berichtsseiten                | Darstellung                       |
|----------------------------|-------------------------------------|
| RIF-Übersicht ab Jahresbeginn           | Anfangssaldo                   |
|                            | Nettoveränderung                          |
|                            | Nettoveränderung in %                        |
|                            | Endsaldo                      |
|                            | RIF-Umsatzverhältnis                  |
|                            | Tage RIF verfügbar                    |
|                            | Aktiver Kostenträger in Periode        |
|                            | Nettoveränderung nach Ressourcengruppe        |
|                            | Saldo nach Standort                     |
|                            | Aufstellung nach Kategorie               |
|                            | Nettoveränderung nach Quartal               |
| RIF-Aufstellung              | Anfangssaldo                   |
|                            | Endsaldo                      |
|                            | RIF-Aufstellung nach Kategorie           |
| RIF-Aufstellung nach Standort      | Anfangssaldo                   |
|                            | Endsaldo                      |
|                            | RIF-Aufstellung nach Kategorie und Standort  |
| RIF-Aufstellung nach Hierarchie | Anfangssaldo                   |
|                            | Endsaldo                      |
|                            | RIF-Aufstellung nach Kategoriehierarchie |

### <a name="inventory-accounting-analysis"></a>Bestandsbuchhaltung – Analyse

| Berichtsseiten        | Darstellung                                                                |
|--------------------|------------------------------------------------------------------------------|
| Bestandsdetails  | Top 10 Ressourcen nach Endsaldo                                           |
|                    | Top 10 Ressourcen nach Nettoerhöhung                                      |
|                    | Top 10 Ressourcen nach Nettoverringerung                                      |
|                    | Top 10 Ressourcen nach Bestandsumsatzverhältnis                                 |
|                    | Ressourcen nach Umsatzverhältnis bei niedrigem Lagerbestand und Endsaldo oberhalb des Schwellenwerts |
|                    | Top 10 Ressourcen nach niedriger Genauigkeit                                             |
| ABC-Klassifizierung | Bestand Endbetrag                                                     |
|                    | Verbrauchtes Material                                                            |
|                    | Verkauft (COGS)                                                                  |
| Bestandstrends   | Bestand Endbetrag                                                     |
|                    | Bestand Nettoänderung                                                         |
|                    | Verhältniszahl für Lagerumschlag                                                     |
|                    | Lagergenauigkeit                                                           |

### <a name="manufacturing-accounting-analysis"></a>Fertigungsbuchhaltung – Analyse

| Berichtsseiten | Darstellung      |
|-------------|--------------------|
| RIF-Trends  | RIF-Endsaldo |
|             | RIF-Nettoveränderung     |
|             | RIF-Umsatzverhältnis |

### <a name="std-cost-variance-analysis"></a>Standardkostenabweichungsanalyse

| Berichtsseiten                             | Darstellung                                        |
|-----------------------------------------|------------------------------------------------------|
| Einkaufspreisabweichung (Standardkosten) ab Jahresbeginn | Beschaffter Saldo                                     |
|                                         | Einkaufspreisabweichung                              |
|                                         | Einkaufspreis-Abweichungsverhältnis                        |
|                                         | Abweichung nach Artikelgruppe                               |
|                                         | Abweichung nach Standort                                     |
|                                         | Einkaufspreis nach Quartal                            |
|                                         | Einkaufspreis nach Quartal und Artikelgruppe             |
|                                         | Top 10 Ressourcen nach ungünstigem Einkaufspreisverhältnis |
|                                         | Top 10 Ressourcen nach günstigem Einkaufspreisverhältnis   |
| Produktionsabweichung (Standardkosten) ab Jahresbeginn     | Fertigungskosten                                    |
|                                         | Produktionsabweichung                                  |
|                                         | Produktionsabweichungsverhältnis                            |
|                                         | Abweichung nach Artikelgruppe                               |
|                                         | Abweichung nach Standort                                     |
|                                         | Produktionsabweichung nach Quartal                       |
|                                         | Produktionsabweichung nach Quartal und Abweichungstyp     |
|                                         | Top 10 Ressourcen nach ungünstiger Produktionsabweichung  |
|                                         | Top 10 Ressourcen nach günstiger Produktionsabweichung    |

## <a name="understanding-the-data-model-and-entities"></a>Das Datenmodells und die Entitäten verstehen

Daten aus der Anwendung werden verwendet, um die Berichtsseiten im Power BI-Inhalt zur **Kostenverwaltung** auszufüllen. Diese Daten werden als aggregierte Messungen dargestellt, die im Entitätsspeicher bereitgestellt werden, der eine Microsoft SQL Server-Datenbank ist, die für Analysen optimiert ist. Weitere Informationen finden Sie unter [Power BI-Integration mit Entitätsspeicher](power-bi-integration-entity-store.md).

Die wesentlichen aggregierten Messungen der folgenden Objekte werden als Grundlage des Power BI-Inhalts verwendet.

| Objekt                          | Zentrale aggregierte Messungen | Datenquelle für Finance and Operations | Feld               |
|---------------------------------|----------------------------|----------------------------------------|---------------------|
| CostObjectStatementCacheMonthly | Dauer                     | CostObjectStatementCache               | Dauer              |
| CostObjectStatementCacheMonthly | Leistung                   | CostObjectStatementCache               | Menge                 |
| CostInventoryAccountingKPIGoal  | AnnualInventoryTurn        | CostInventoryAccountingKPIGoal         | AnnualInventoryTurn |
| CostInventoryAccountingKPIGoal  | InventoryAccuracy          | CostInventoryAccountingKPIGoal         | InventoryAccuracy   |

Die folgende Tabelle zeigt die wesentlichen berechneten Messungen im Power BI-Inhalt an.

| Kennzahl                            | Herstellkostenkalkulation |
|------------------------------------|-------------|
| Anfangssaldo                  | Anfangssaldo = \[Endsaldo\]-\[Nettoveränderung\] |
| Anfangssaldomenge             | Anfangssaldomenge = \[Endsaldomenge\]-\[Nettoveränderungsmenge\] |
| Endsaldo                     | Endsaldo = (CALCULATE(SUM(\[Amount\]), FILTER(ALL(FiscalCalendar) ,FiscalCalendar\[MONTHSTARTDATE\] \<= MAX(FiscalCalendar\[MONTHSTARTDATE\])))) |
| Endsaldomenge                | Endsaldomenge = CALCULATE(SUM(\[QTY\], FILTER(ALL(FiscalCalendar),FiscalCalendar\[MONTHSTARTDATE\] \<= MAX(FiscalCalendar\[MONTHSTARTDATE\]))) |
| Nettoveränderung                         | Nettoänderung = SUM(\[AMOUNT\]) |
| Nettoveränderungsmenge                    | Nettoveränderungsmenge = SUM(\[QTY\]) |
| Lagerumschlagverhältnis nach Betrag | Lagerumschlagverhältnis nach Betrag = if(OR(\[Durchschnittlicher Bestandssaldo\] \<= 0, \[Verkaufter oder verbrauchter Bestand\]\> = 0), 0, ABS(\[Verkaufter oder verbrauchter Bestand\])/\[Durchschnittlicher Bestandssaldo\]) |
| Durchschnittlicher Lagerbestandsaldo          | Duchschnittlicher Bestandssaldo = ((\[Endsaldo\]  + \[Anfangssaldo\]) / 2) |
| Lagerbestandsverfügbarkeit in Tagen             | Lagerbestandsverfügbarkeit in Tagen = 365 / CostObjectStatementEntries\[Lagerumschlagsverhältnis nach Betrag\] |
| Lagergenauigkeit                 | Lagerbestandsgenauigkeit nach Betrag = IF(\[Endsaldo\]\< = 0, IF(OR(\[Gezählter Bestandsbetrag\] \<\> 0, \[Endsaldo\] \< 0), 0, 1), MAX(0, (\[Endsaldo\] - ABS(\[Gezählter Bestandsbetrag\]))\[Endsaldo\])) |

Die folgenden wesentlichen Dimensionen werden als Filter verwendet, um die aggregierten Messungen zu segmentieren, damit Sie eine stärkere Granularität sowie tiefere analytische Einblicke erlangen.


| Entität                                                  | Beispiele für Attribute                          |
|---------------------------------------------------------|-------------------------------------------------|
| Produkte                                                | Produktnummer, Produktname, Einheit, Artikelgruppen |
| Kategoriehierarchien (Zugewiesen zur Rolle „Kostenmanagement”) | Kategoriehierarchie, Kategorie-Ebene              |
| Juristische Personen                                          | Name der juristischen Person                              |
| Steuerkalender                                        | Steuerkalender, Jahr, Quartal, Periode, Monat   |
| Standort                                                    | ID, Name, Adresse, Bundesland, Land               |