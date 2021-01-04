---
title: Power BI-Inhalt der Ausgabenverwaltung
description: In diesem Thema wird beschrieben, was im Power BI-Inhaltspaket zur Ausgabenverwaltung enthalten ist.
author: RyanSand
manager: AnnBe
ms.date: 03/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: TrvExpenseWorkspace, ExpenseWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kfend
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 9391676beea6aac831648d5fa55eae5eba3f6397
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682796"
---
# <a name="expense-management-power-bi-content"></a>Power BI-Inhalt der Ausgabenverwaltung

[!include [banner](../includes/banner.md)]

In diesem Thema wird beschrieben, was im Power BI-Inhalt zur Ausgabenverwaltung enthalten ist. 

## <a name="overview"></a>Übersicht
Zwei  Power BI  Inhaltspakete sind für die Verwendung mit der Ausgabenverwaltung in Version 8.1 und höher verfügbar. 
- Es gibt eine persönlichen Dashboard, das für Mitarbeiter vorgesehen ist, um die Ausgabenberichte zu übermitteln. 

  Das Dashboard ist so gestaltet, dass wichtige Informationen für Personen zu übermittelten und noch nicht übermittelten Beträgen sowie der Verlauf und Einblicke in den Ausgabentransaktionsverlauf bereitgestellt werden. Das persönliche Dashboard ist eine Einzelseite, welche die wichtigsten Informationen für den Benutzer enthält.

- Es gibt ein Administratordashboard, das für Kreditorenkonten-Sachbearbeiter und Manager vorgesehen ist. Das Dashboard ist für die Nachverfolgung und die Berichterstattung von Gesamtmitarbeiterausgaben zugeschnitten. Es bietet entscheidende Ausgabenenmetrik wie noch nicht übermittelte Ausgaben, Kilometerleistung und durchschnittliche Spesenabrechnungsbeträge. Es verwendet Transaktionsdaten und bietet Aggregatansichten vom Ausgabenmanagement in sämtlichen Unternehmen. Es bietet auch eine Aufschlüsselung pro Mitarbeiter, mit der Option, Finanzdimensionen hinzuzufügen. Die Administratorausgaben-Analyseinhalt enthält: 
  - Eine Überblicksseite mit entscheidender Metrik über Ausgabenbeträge und Einblicke in Berichte, die als Entwurf vorhanden sind, in Bearbeitung sind oder abgeschlossen sind. 
  - Eine Mitarbeiterstatistikseite, um einzelne Details über einen Mitarbeiter nach Zeit, Kostentyp und Statistikgruppe zu überprüfen. 
  - Eine Mitarbeitervergleichsseite, um mehrere Mitarbeiter im Zeitverlauf zu vergleichen. 

Alle Beträge werden in der Unternehmenswährung angezeigt. Daten für alle Unternehmen werden angezeigt, aber Sie können nach Bedraf einen Unternehmensfilter hinzufügen. 

## <a name="accessing-the-power-bi-content"></a>Zugreifen auf den Power BI-Inhalt
Sie finden die Dateien Administrator Ausgaben Dashboard.pbix und Persönliche Ausgaben Dashboard.pbix Power BI Inhalt in der freigegebenen Anlagenbibliothek in Microsoft Dynamics Lifecycle Services (LCS). Weitere Informationen dazu, wie Sie den Inhalt herunterladen und in Ihrer Organisation implementieren, finden Sie unter [Power BI-Inhalt in LCS von Microsoft und Ihren Partnern](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/12/12/power-bi-content-from-microsoft-and-your-partners/).
Der Inhalt ist vom Ausgabenverwaltungsarbeitsbereich als eingebetteter Power BI Inhalt verfügbar. Jeder Ausgabeneneigentümer kann selbst auf persönliche Ausgaben zugreifen, während nur Kreditorenkonten-Sachbearbeiter und Manager Zugriff auf Administratorinhalte haben, um alle Ausgabenendaten anzuzeigen.

## <a name="refreshing-the-power-bi-content"></a>Aktualisieren des Power BI Inhalts
Der Inhalt Ausgabenverwaltungs Power BI benötigt die TrvBiExpenseMeasurement-Kennzahl und das BudgetActivityMeasure, um aus dem Entitäts-Shop aktualisiert zu werden. 

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Metriken, die im Power BI-Inhalt enthalten sind
Der Inhalt enthält einen Satz Berichtsseiten. Jede Seite enthält einen Satz Metriken, die als Diagramme, Kacheln und Tabellen visuell dargestellt werden. Die folgende Tabelle enthält eine Übersicht der Visualisierungen im Power BI Paket.

**Analyse persönlicher Ausgaben**

| Berichtsseiten | Darstellung                             |
|-------------|-------------------------------------------|
| Eigene Ausgaben | Betrag der Kilometerleistung                         |
|             | Spesenabrechnungen in Verarbeitung                |
|             | Nr. von noch nicht übermittelten Ausgaben               |
|             | Persönliche Ausgaben zum Bezahlen              |
|             | Noch nicht übermittelter Betrag                        |
|             | Übermittelter Betrag                          |
|             | Betrag für die Rückerstattung             |
|             | Ausgabenberichte mit Beträgen und Status   |
|             | Übermittelte aber nicht genehmigte Ausgabenberichte  |
|             | Ausgaben nach Kostentyp                     |
|             | Ausgaben nach Verkäufer                      |
|             | Ausgaben nach verarbeitete Ausgaben            |
|             | Ausgaben nahc Projekt                       |
|             | Gesamttransaktionsbetrag im Zeitverlauf        |

**Administratorausgabenanalyse**

| Berichtsseiten         | Darstellung                           |           
|---------------------|-----------------------------------------|
| Ausgabenüberblick    | Entwurfausgabenbetrag                   |
|                     | Anzahl der Ausgabenpositionen im Entwurf           |
|                     | Ausgabenpositionen im Entwurf                     |
|                     | Richtlinienverletzungen für Ausgabenabrechnung        |
|                     | Betrag ausstehend                      |
|                     | Übermittelte aber nicht genehmigte Ausgaben       |
|                     | Genehmigte Ausgaben                       |
|                     | Gesamter Spesenbetrag                    |
|                     | Zusammenfassung des Ausgabenberichts                |
|                     | Ausgaben nach Kostentyp                   |
|                     | Ausgaben nach Verkäufer                    |
|                     | Ausgaben nach Mitarbeiter                   |
|                     | Ausgaben vs. Projekt                     |
| Mitarbeitevergleich | Ausgabenbetrag                         |
|                     | Ausgabenbeträge im Zeitverlauf nach Mitarbeiter   |
| Mitarbeiterstatisik | Ausgabenbericht nach Kostentyp            |
|                     | Persönliche Spesen                       |
|                     | Ausgabenberichte nach Statistikgruppe     |
