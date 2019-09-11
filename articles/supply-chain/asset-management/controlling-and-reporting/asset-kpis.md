---
title: Anlagen-KPIs
description: In diesem Thema werden Anlagen-KPIs in Asset Management erläutert.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 4fc32d337be1f71932555fcb062a8d05c9ca9bda
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918417"
---
# <a name="asset-kpis"></a>Anlagen-KPIs

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

In Asset Management können Sie verschiedene Key Performance Indicators (KPIs) für Anlagen und Anlagentypen berechnen. Sie können KPIs verwenden, um einen Überblick der Leistung von Anlagen in Bezug auf beispielsweise Uptime, Ausfallzeiten, Reparaturzeit und mittlere ausfallfreie Betriebszeit (MTBF) zu erhalten.

1. Klicken Sie auf **Anlagenverwaltung** > **Abfragen** > **Anlagen** > **Anlagen-KPIs**.

2. Wählen Sie im Dialogfeld **Anlagen-KPIs berechnen** die **Zeitskala** aus, die in der Berechnung verwendet werden soll, und eine Periode in den Feldern **Von Datum** und **Bis Datum**. 

3. Auf dem Inforegister **Einzuschließende Datensätze** können Sie bestimmte Anlagen und Anlagetypen auswählen, die in die Berechnung einbezogen werden sollen, falls erforderlich.

4. Klicken Sie auf **OK**, um die Berechnung zu starten.

5. Auf dem Inforegister **Übersicht** werden die Ergebnisse der Berechnung in der Rasteransicht angezeigt. Jede Anlage wird in einer separaten Position angezeigt.

6. Auf dem Inforegister **KPIs für ausgewählte Position** finden Sie Berechnungen für die Anlage, die auf dem Inforegister **Übersicht** ausgewählt wird. Die KPI-Werte werden in Bezug auf **Zeit**, **Verfügbarkeit**, **Arbeitsaufträge**, **Wartung**, **Fehler**, **Wartungsausfallzeit** und **Kosten** kategorisiert.

In der Tabelle unten finden Sie eine Beschreibung der Felder auf der Seite **Anlagen-KPIs**.

| Feld                   | Beschreibung                                                                                                                                                                                                                                                                                           |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Anlage                   | Anlagenkennung.                                                                                                                                                                                                                                                                                             |
| Gesamtzeit              | Die gesamte Zeit, die im Kalender eingestellt ist, der in der Berechnung verwendet wird. Wenn die Anlage zu einer Ressource zugeordnet wird, wird der zugehörige Ressourcenkalender verwendet. Wenn die Anlage nicht zu einer Ressource zugeordnet ist, wird der Kalender, der im Feld **Standardkalender** unter **Anlagenverwaltungsparameter** ausgewählt ist, verwendet. |
| Betriebszeit                  | Die Gesamtzeit minus Ausfallzeiten.                                                                                                                                                                                                                                                                            |
| Ausfallzeit                | Erfassungen von Wartungsausfallzeiten für die Anlage in der ausgewählten Periode.                                                                                                                                                                                                                              |
| Reparaturzeit             | Gesamtanzahl der Arbeitsstunden, die bei Reparaturarbeitsaufträgen verbraucht wurden.                                                                                                                                                                                                                                            |
| Verfügbarkeit %          | Betriebszeit geteilt durch Gesamtzeit, multipliziert mit 100.                                                                                                                                                                                                                                                   |
| Anzahl der Fehler        | Anzahl der Fehlerursachen, die für Fehlersymptome für die Anlage in der ausgewählten Periode erfasst wurden.                                                                                                                                                                                                             |
| MTBF                    | Mittlere ausfallfreie Betriebszeit (Mean Time Between Failure). Die Gesamtzeit geteilt durch die Anzahl der Fehler, die für die Anlage in der ausgewählten Periode erfasst wurden. Wenn die Fehleranzahl Null ist, wird MTBF auf die Gesamtzeit festgelegt.                                                                                                                   |
| Fehlerrate               | 1 dividiert durch MTBF.                                                                                                                                                                                                                                                                                    |
| MRT                     | Mittlere Reparaturzeit (Mean Repair Time). Die Reparaturzeit geteilt durch die Anzahl der Fehler, die für die Anlage in der ausgewählten Periode erfasst wurden. Wenn die Fehleranzahl Null ist, wird MRT auf die Reparaturzeit festgelegt.                                                                                                                           |
| Anzahl der Stopps         | Anzahl der Wartungsausfallzeiterfassungen, die für eine Anlage erstellt wurden.                                                                                                                                                                                                                                     |
| MTBS                    | Mittlere Zeit zwischen Stopps (Mean Time Between Stops). Die Gesamtzeit geteilt durch die Wartungsausfallzeiterfassungen. Wenn die Anzahl der Wartungsausfallzeiterfassungen für die ausgewählte Periode Null ist, wird der MTBS-Wert auf die Gesamtzeit festgelegt.                                                                                      |
| Vorbeugend – Kosten         | Die Kosten, die für die Anlage in Bezug auf den Kostentyp „Vorbeugend“ in der ausgewählten Periode gebucht wurden. Kostentypen werden in Arbeitsauftragstypen eingerichtet.                                                                                                                                                                       |
| Korrektiv – Kosten         | Die Kosten, die für die Anlage in Bezug auf den Kostentyp „Korrektiv“ in der ausgewählten Periode gebucht wurden. Kostentypen werden in Arbeitsauftragstypen eingerichtet.                                                                                                                                                                       |
| Wiederbeschaffungswert       | Der Wert, der für die Anlage als die Wiederbeschaffungskosten definiert wurde.                                                                                                                                                                                                                                                  |
| Anlagentyp             | Kennung des Anlagentyps, der für die Anlage ausgewählt wurde.                                                                                                                                                                                                                                             |
| Hersteller           | Kennung des Herstellers, der für die Anlage ausgewählt wurde.                                                                                                                                                                                                                                                 |
| Modell                   | Kennung des Herstellermodells, das für die Anlage ausgewählt wurde.                                                                                                                                                                                                                                           |
| Anfangsdatum               | Startdatum der KPI-Kalkulation. Wenn die Anlage nach dem Startdatum erstellt wurde, das für die Berechnung ausgewählt wurde, wird das Startdatum der Anlage in diesem Feld angezeigt.                                                                                                                                  |
| Enddatum                 | Enddatum der KPI-Kalkulation. Wenn die Anlage vor dem Enddatum, das für die Berechnung ausgewählt wurde, als inaktiv erfasst wurde, wird das Datum, ab dem die Anlage nicht mehr aktiv war, in diesem Feld angezeigt.                                                                                               |
| Zeitraum              | Während der Berechnung der KPIs wählen Sie eine zu verwendende Zeitskala aus: Stunden, Tage oder Wochen.                                                                                                                                                                                                            |
| Verfügbarkeit            | Betriebszeit geteilt durch Gesamtzeit.                                                                                                                                                                                                                                                                         |
| Arbeitsaufträge             | Die Gesamtanzahl von Arbeitsaufträgen, die in der KPI-Kalkulation berücksichtigt wurden.                                                                                                                                                                                                                                          |
| Arbeitsauftragszeit         | Gesamtanzahl der Arbeitsstunden, die bei Arbeitsaufträgen verbraucht wurden.                                                                                                                                                                                                                                               |
| Primäre Arbeitsaufträge     | Die Anzahl von primären Arbeitsaufträgen, die in der KPI-Kalkulation berücksichtigt wurden.                                                                                                                                                                                                                                        |
| Sekundäre Arbeitsaufträge   | Die Anzahl von sekundären Arbeitsaufträgen, die in der KPI-Kalkulation berücksichtigt wurden.                                                                                                                                                                                                                                      |
| Wartungsarbeitsaufträge | Die Anzahl von Wartungsarbeitsaufträgen, die in der KPI-Kalkulation berücksichtigt wurden. Ein Wartungsarbeitsauftrag ist ein Arbeitsauftrag ohne zugehörige Fehlerursachen.                                                                                                                                                             |
| Wartungszeit        | Gesamtanzahl der Arbeitsstunden, die bei Wartungsarbeitsaufträgen verbraucht wurden.                                                                                                                                                                                                                                       |
| Reparaturarbeitsaufträge      | Die Anzahl von Reparaturarbeitsaufträgen, die in der KPI-Kalkulation berücksichtigt wurden. Ein Reparaturarbeitsauftrag ist ein Arbeitsauftrag mit einer zugehörigen Fehlerursache.                                                                                                                                                                        |
| Zuverlässigkeit %           | Berechnung auf Basis der erwarteten exponentiellen Entwicklung in den Fehlererfassungen für eine Anlage, was bedeutet, dass die Anlage im Zeitverlauf aufgrund Abnutzung weniger zuverlässig wird. Die Berechnung dieses KPIs basiert auf MTBF und der Gesamtzeit.                                                            |
| MTPS                    | Mittlere Zeit der Produktionsstopps (Mean Time Production Stops). Die Wartungsausfallzeit geteilt durch die Anzahl der Wartungsausfallzeiterfassungen. Wenn die Anzahl der Wartungsausfallzeiterfassungen für die ausgewählte Periode Null ist, wird der MTPS-Wert auf Null festgelegt.                                                                               |
| Gesamtkosten              | Gesamtkosten, die für die Anlage in der ausgewählten Periode gebucht wurden.                                                                                                                                                                                                                                              |
| Investitionskosten         | Die Kosten, die für die Anlage in Bezug auf den Kostentyp „Investition“ in der ausgewählten Periode gebucht wurden. Kostentypen werden in Arbeitsauftragstypen eingerichtet.                                                                                                                                                                       |

Die folgende Abbildung zeigt ein Bildschirmabbild einer KPI-Berechnung für vier Anlagen.

![Abbildung 1](media/11-controlling-and-reporting.png)

- Sie können mehrere Anlagen in **Alle Anlagen** auswählen und dann auf die Schaltfläche **Anlagen-KPIs** auf der Registerkarte **Allgemein** klicken. Klicken Sie dann im Dialogfeld **Anlagen-KPIs berechnen** auf **OK**, um KPIs für die ausgewählten Anlagen zu berechnen.  
- Ergebnisse einer KPI-Berechnung können [Wartungsausfallzeiterfassungen](../work-orders/maintenance-downtime.md) enthalten, je nach Einstellungen und Verwendung von Wartungsausfallzeitursachencodes. 

