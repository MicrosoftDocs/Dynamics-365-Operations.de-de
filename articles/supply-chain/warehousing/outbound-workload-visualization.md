---
title: Ausgehende Workloadvisualisierung
description: Dieses Thema enthält Informationen über die Visualisierung der ausgehenden Arbeitsauslastung. Mit dieser Funktionalität können Lagerort-Manager und Vorgesetzte benutzerdefinierte Diagramme zur Arbeitsauslastung erstellen, mit denen der Fortschritt der aktuellen Arbeit und die verbleibende Menge überwacht werden kann. Lagerortverwaltungen können mehrere Ansichten erstellen und bei Bedarf eine automatische Aktualisierung festlegen.
author: Mirzaab
ms.date: 08/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-08-28
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: acfde5961f481f5d939f0c6388b80edfd65ee339
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6351416"
---
# <a name="outbound-workload-visualization"></a>Ausgehende Workloadvisualisierung

[!include [banner](../includes/banner.md)]

Erweiterte Funktionalitäten, die über die Seite **Visualisierung der Arbeitsauslastung im Ausgang** zugänglich sind, ermöglichen es Lagerleitern und Vorgesetzten, benutzerdefinierte Diagramme der Arbeitsauslastung zu erstellen, die zur Überwachung des Fortschritts der aktuellen Arbeit und der verbleibenden Menge verwendet werden können. Lagerortverwaltungen können mehrere Ansichten erstellen und bei Bedarf eine automatische Aktualisierung festlegen. Visualisierungen der ausgehenden Arbeitsauslastung eignen sich für die Anzeige auf den Seiten zur Lagerort-Leistung.

Diese Funktionalität kann verwendet werden, um den Fortschritt von Entnahmearbeiten zu verfolgen. Die Funktion ist mit der Arbeitsverwaltung integriert, und wenn die Arbeitsverwaltung festgelegt ist, können die Visualisierungen der ausgehenden Arbeitsauslastung eine Berechnung der Anzahl der Stunden anzeigen, die für die angezeigte (gefilterte) Entnahmearbeit verbleiben.

## <a name="turn-on-the-outbound-workload-visualization-feature"></a>Einschalten der Funktion zur Visualisierung der ausgehenden Arbeitsauslastung

Bevor Sie diese Funktion nutzen können, muss sie auf Ihrem System aktiviert werden. Admins können die Einstellungen [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) verwenden, um den Status der Funktion zu prüfen und sie einzuschalten. Im Arbeitsbereich **Funktionsverwaltung** ist die Funktion wie folgt aufgeführt:

- **Module:** *Lagerortverwaltung*
- **Name der Funktion:** *Visualisierung der ausgehenden Arbeitsauslastung*

## <a name="set-up-outbound-workload-visualizations"></a>Visualisierungen der ausgehenden Arbeitsauslastung festlegen

Um Ihre Visualisierungen festzulegen, erstellen Sie eine Sammlung von Filtern (Ansichten) und gestalten jeden Filter so, dass er eine andere Art von Analyse anzeigt. Sie verwenden die Seite **Filter konfigurieren**, um die Filter zu entwerfen.

Um eine Visualisierung der ausgehenden Arbeitsauslastung festzulegen, gehen Sie wie folgt vor.

1. Gehen Sie auf **Lagerortverwaltung \> Lagerort-Überwachungsberichte \> Visualisierung der ausgehenden Arbeitsauslastung**.

    Die Seite **Visualisierung der ausgehenden Arbeitsauslastung** erscheint. Nachdem Sie einige Filter erstellt haben, wird diese Seite Ihre Visualisierung anzeigen. Sie können so viele Filter erstellen, wie Sie wollen. Alle Filter, die Sie erstellen, werden unter Ihrem Benutzerkonto gespeichert, sodass Sie sie später verwenden können. Mit anderen Worten: Jeder Benutzer hat seinen eigenen Satz von Filtern, die er erstellt hat. Diese Filter werden nicht mit anderen Benutzern geteilt.

1. Wählen Sie auf der Seite **Visualisierung der ausgehenden Arbeitsauslastung** im Aktivitätsbereich auf der Registerkarte **Filter** die Option **Filter konfigurieren**.
1. Wählen Sie auf der Seite **Filter konfigurieren** im Aktivitätsbereich **Neu**, um einen Filter hinzuzufügen, und legen Sie dann die folgenden Felder dafür fest:

    - **X-Achsen-Gruppentabelle** - Wählen Sie die Tabelle, die das Feld enthält, das zum Gruppieren der X-Achsen-Werte verwendet werden soll.
    - **X-Achsengruppenfeld** - Wählen Sie aus den Feldern der Tabelle, die Sie im Feld **X-Achsengruppentabelle** ausgewählt haben, das Feld aus, das zum Gruppieren der X-Achsenwerte verwendet werden soll.
    - **X-Achsenwert-Tabelle** - Wählen Sie die Tabelle, die das Feld enthält, das für die weitere Analyse der Gruppen verwendet werden soll.
    - **X-Achsenwertfeld** - Wählen Sie aus den Feldern der Tabelle, die Sie im Feld **X-Achsenwerttabelle** ausgewählt haben, das Feld aus, das die Werte liefert, die für jede Gruppe analysiert werden sollen.
    - **Automatisch aktualisieren** - Wählen Sie, ob die Visualisierung automatisch aktualisiert werden soll.
    - **Auffrischungsintervall (Minuten)** - Geben Sie die Anzahl der Minuten zwischen den automatischen Auffrischungen ein.
    - **Anzeigestufe** - Wählen Sie, ob das Diagramm offene Zeilen oder die Anzahl offener Kopfzeilen anzeigen soll.
    - **Typ der Entnahme** - Wenn Sie das Feld **Anzeigeebene** auf _Offene Zeilen_ festlegen, wählen Sie, ob die Zählung der offenen Zeilen im Diagramm anfängliche Entnahmen, gestaffelte Entnahmen oder sowohl anfängliche Entnahmen als auch gestaffelte Entnahmen enthalten soll.
    - **Standort** - Wählen Sie den Standort, für den das Diagramm geladen werden soll.
    - **Lagerort** - Wählen Sie den Lagerort aus, für den das Diagramm geladen werden soll.
    - **Einzubeziehende Tage** - Geben Sie die Anzahl der Tage in der Vergangenheit ein, für die das Diagramm erstellt werden soll.
    - **Arbeitsauftragstyp** - Wählen Sie die Typen der ausgehenden Arbeitsaufträge, nach denen gefiltert werden soll.

    ![Seite Filter konfigurieren.](media/work-viz-filters-1.png "Seite Filter konfigurieren")

1. Schließen Sie die Seite **Filter konfigurieren**, um zur Seite **Visualisierungen der ausgehenden Arbeitsauslastung** zurückzukehren.

    Die Seite **Visualisierungen der ausgehenden Arbeitsauslastung** zeigt jetzt Daten an, die auf Ihren neuen Filtereinstellungen basieren. Ihr neuer Filter ist jetzt verfügbar und wird im Feld **Filter** ausgewählt. Die folgenden Felder sind am oberen Rand des Diagramms verfügbar:

    - **Filter** - Dieses Feld enthält alle Filter, die Sie bisher erstellt haben. Wählen Sie einen Filter aus, um seine Daten im Diagramm anzuzeigen.
    - **Zuletzt aktualisiert** - Dieses Feld zeigt das Datum und die Uhrzeit an, zu der die Informationen im Diagramm zuletzt aktualisiert wurden.
    - **Geschätzte/Ist-Zeit** - Wenn in Ihrem System Arbeitsstandards festgelegt sind, legen Sie diese Option auf *Ja* fest, um die kumulierten geschätzten Kommissionierzeiten oben in jeder Spalte des Diagramms anzuzeigen. Wenn Sie keine Arbeitsstandards verwenden, ist diese Option nicht verfügbar.

    ![Beispielvisualisierung.](media/work-viz-chart.png "Beispiel-Visualisierung")

1. Wählen Sie einen beliebigen Balken im Diagramm aus, um die zugehörigen Details zur Arbeitszeile anzuzeigen.

    ![Arbeitspositionsdetails.](media/work-viz-work-details.png "Arbeitspositionsdetails")

## <a name="example-outbound-workload-visualization-for-zones"></a>Beispiel: Visualisierung der ausgehenden Arbeitsauslastung für Zonen

Für dieses Beispiel möchten Sie eine Visualisierung festlegen, die Arbeitszeilen für jede Zone und den Status jeder Arbeitszeile (_Offen_, _Geschlossen_ oder _Abgebrochen_) anzeigt. In diesem Fall können Sie einen Filter festlegen, der die folgenden Einstellungen hat:

- **Filtername** - Geben Sie einen Namen für diesen Filter ein (z. B. _Zone vs. Arbeitsstatus_).
- **Beschreibung** - Geben Sie eine kurze Beschreibung für diesen Filter ein (z. B. _Zone vs. Arbeitsstatus_).
- **X-Achse Gruppentabelle** - Wählen Sie _Lagerplätze._
- **X-Achsengruppe** - Wählen Sie _Zonen-ID_.
- **X-Achsenwert-Tabelle** - Wählen Sie _Arbeit_, da Sie die Arbeit pro Zone anzeigen möchten.
- **X-Achsen-Wertefeld** - Wählen Sie _Arbeitsstatus_, weil Sie den Arbeitsstatus anzeigen wollen.
- **Automatisch aktualisieren** - Wählen Sie, ob die Visualisierung automatisch aktualisiert werden soll.
- **Typ der Entnahme** - Wählen Sie _Erstentnahmen und gestaffelte Entnahmen_, weil Sie sowohl Erstentnahmen als auch Entnahmen von gestaffelten Lagerplätzen einbeziehen wollen. Mit anderen Worten: Sie wollen im Wesentlichen alle Zeilen mit Entnahmearbeiten einbeziehen, die Sie haben.
- **Anzeigeebene** - Wählen Sie _Zeilen öffnen_, weil Sie die Informationen pro Zeile und nicht pro Arbeitskopf anzeigen wollen.

Die folgende Abbildung zeigt ein Beispiel für das resultierende Diagramm.

![Visualisierung von Zone vs. Arbeitsstatus.](media/work-viz-chart.png "Visualisierung von Zone vs. Arbeitsstatus")

Dieses Diagramm zeigt zwei Zonen mit den Namen **FLOOR** und **BULK**, sowie eine Zone mit dem Namen **Blank**. Die Zone **Leer** repräsentiert alle Arbeitszeilen, die nicht Mitglied einer Zone sind. Das Diagramm zeigt immer alle nicht zugehörigen gefilterten Daten als **Leerzeichen** an, um eine möglichst gute Sichtbarkeit zu gewährleisten. In der Zone **FLOOR** zeigt das Diagramm drei geschlossene Zeilen und vier offene Zeilen. In der Zone **BULK** zeigt das Diagramm vier geschlossene Linien, eine offene Linie und 24 gelöschte Linien. Schließlich zeigt das Diagramm acht geschlossene Zeilen, die zu keiner Zone gehören und daher als **Leer** aufgeführt sind.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]