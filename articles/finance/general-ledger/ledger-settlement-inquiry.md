---
title: Abfrage für Sachkontoausgleich
description: In diesem Artikel wird das Anfragefenster für die Ledger-Abrechnung beschrieben
author: kweekley
ms.date: 12/15/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerClosingSheet
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 33ae49d9503c0a83bda7e0093ab6ef69fb4aef0a
ms.sourcegitcommit: 9f3a60a583da21382a14f32ce146fc9ce03f2a09
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/15/2022
ms.locfileid: "9853127"
---
# <a name="ledger-settlement-inquiry"></a>Abfrage für Sachkontoausgleich

[!include [banner](../includes/banner.md)]

In diesem Artikel wird das Fenster **Abfrage des Sachkontoausgleichs** beschrieben, das verwendet werden kann, um abgerechnete, nicht abgerechnete oder sowohl abgerechnete als auch nicht abgerechnete Sachkontobuchungen für einen Abrechnungszeitraum anzuzeigen.

## <a name="view-ledger-settlement-transactions"></a>Hauptbuchabwicklungstransaktionen anzeigen
1.  Wechseln Sie zu **Hauptbuch > Abfragen und Berichte > Abfrage für Sachkontoausgleich**.
2.  Verwenden Sie die Felder **Von Datum** und **Bis Datum** oder das **Datumsintervall** Feld, um einen Datumsbereich anzugeben. Bei der Probebilanz muss der Datumsbereich innerhalb eines einzigen Geschäftsjahres liegen.
3.  Wählen Sie im Feld **Hauptkonten** ein oder mehrere Hauptkonten aus, für die Sie die Hauptbuchtransaktionen anzeigen möchten. Die Dropdown-Liste zeigt nur Hauptkonten an, die auf der Seite **Hauptbuchparameter** für die Hauptbuchabrechnung eingerichtet wurden.
4.  Verwenden Sie das Feld **Finanzdimensionssatz**, um die Finanzdimensionen im Raster anzuzeigen. Da das Hauptkonto erforderlich ist, wird der Feldwert **Hauptkonto** immer als erste Spalte angezeigt, selbst wenn Sie einen Finanzdimensionssatz auswählen, der das Hauptkonto nicht enthält Konto.
5.  Wählen Sie im Feld **Status** die Option:
-   **Alle**, um sowohl abgerechnete als auch nicht abgerechnete Transaktionen anzuzeigen
-   **Nicht abgewickelt**, um nur nicht abgerechnete Transaktionen anzuzeigen 
-   **Abgewickelt**, um nur abgerechnete Transaktionen anzuzeigen
6.  Wählen Sie **Transaktionen anzeigen**. Hauptbuchbuchungen werden basierend auf den von Ihnen eingegebenen Kriterien im Raster angezeigt. Sie können die Ergebnisse der Abfrage an Microsoft Excel zur weiteren Analyse exportieren. Wählen oder halten (oder mit der rechten Maustaste) auf das Raster.

### <a name="column-details"></a>Spaltendetails
Das Raster auf der Seite **Hauptbuchabrechnungsabfrage** enthält die folgenden Spalten:
-   **Hauptkonto** – Dieses Feld ist erforderlich und wird immer angezeigt.
-   **Finanzdimensionen** – Finanzdimensionen werden basierend auf dem ausgewählten Finanzdimensionssatz angezeigt.
-   **Buchungsdatum** – Das Buchungsdatum der Sachbuchtransaktion.
-   **Ursprüngliches Transaktionsdatum** – Wenn der Jahresabschluss durchgeführt wurde und der Hauptbuchausgleich so eingerichtet ist, dass Details für ein Hauptkonto beibehalten werden, werden die offenen Transaktionen im Detail als Eröffnungssaldo übernommen. Das ursprüngliche Buchungsdatum der Sachkontobuchung wird im Feld **Ursprüngliches Buchungsdatum** gepflegt.
-   **Transaktionsalter** – Der Wert ist 0 (Null) für alle abgerechneten Transaktionen. Bei nicht abgewickelten Transaktionen wird der Wert als Anzahl der Tage entweder vom ursprünglichen Transaktionsdatum oder vom Transaktionsdatum bis zum Datum der Ausführung der Anfrage berechnet.
Beispielsweise hat eine Hauptbuchtransaktion das Transaktionsdatum 1. Januar 2022 (1.1.2022) und ein ursprüngliches Transaktionsdatum den 30. Dezember 2021 (30.12.2021). Wenn die Abfrage am 2. Januar 2022 (1.2.2022) für das Geschäftsjahr 2022 ausgeführt wird, ist der **Transaktionsalterswert** 4. Dieser Wert wird als Anzahl der Tage zwischen dem ursprünglichen Transaktionsdatum (30.12.2021) und dem 02.01.2022 berechnet.

Wenn kein ursprüngliches Transaktionsdatum vorhanden ist, wird stattdessen das Transaktionsdatum verwendet.
-   **(Sonstige Transaktionsinformationen)** – Zusätzliche Spalten zeigen Informationen wie die Belegnummer, die Beschreibung sowie Soll- und Habenbeträge in allen drei Währungen (Transaktion, Buchhaltung und Reporting).
-   **Status** – Dieser Wert ist entweder **Abgerechnet** oder **Nicht abgerechnet**.
-   **Abwicklungs-ID** – Die eindeutige ID, die den abgewickelten Transaktionen zugewiesen ist.

[![Abfrage für Sachkontoausgleichseite](./media/Inquiry1.png)](./media/Inquiry1.png)

 
Summen können unter dem Raster angezeigt werden.
1.  Wählen Sie die Auslassungspunkte (…) rechts vom Raster und dann **Fußzeile anzeigen** aus.
2.  Wählen Sie aus oder halten Sie (mit der rechten Maustaste klicken) in jede Betragszeile und wählen Sie dann **Nach dieser Zeile gruppieren**, um die Gesamtwerte anzuzeigen. Die Summen werden in der Fußzeile angezeigt. Wenn die Abfrage so gefiltert wird, dass nur offene Transaktionen angezeigt werden, können Sie die Summen verwenden, um die Beträge mit der Probebilanz abzugleichen.







