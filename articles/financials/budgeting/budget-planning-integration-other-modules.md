---
title: Budgetplanungsintegration in andere Module
description: "Budgetpläne können aus mehreren unterschiedlichen Ressourcen generiert werden. Die grundlegenden Elemente für den periodischen Prozess sind die gleichen für alle Ressourcen."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 64443
ms.assetid: f9a94db5-906c-404a-9ca5-91528d67c490
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 311a5cbd3768d8ecc7e7430717369193e60c3e57
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---

# <a name="budget-planning-integration-with-other-modules"></a>Budgetplanungsintegration in andere Module

[!include[banner](../includes/banner.md)] Budgetpläne können aus mehreren unterschiedlichen Ressourcen generiert werden. Die grundlegenden Elemente für den periodischen Prozess sind die gleichen für alle Ressourcen. 



<a name="periodic-processes-for-generating-budget-plans"></a>Periodische Prozesse für das Generieren von Budgetplänen
----------------------------------------------

Budgetpläne können aus folgenden Ressourcen generiert werden:

-   Hauptbuchbuchungen
-   Feststehende Inhaltsteile
-   Planungspositionen
-   Projektplanungen
-   Beschaffungsplanungen
-   Bedarfsplanungen
-   Budgetregistereinträge
-   Andere Budgetpläne

Die grundlegenden Elemente für den periodischen Prozess sind die gleichen für alle Prozesse. Über Registerkarten können Sie die Quelle der Daten, die Zielattribute (Budgetplan) und Optionen zum A Prozesses im Hintergrund als Stapelverarbeitungsvorgang definieren. In späteren Abschnitten dieses Artikels werden Elemente beschrieben, die möglicherweise nicht in jedem Prozess ersichtlich sind.

### <a name="actions"></a>Aktionen

Für jeden Generierungsprozess sind drei Aktionen verfügbar:

-   **Neuen Budgetplan erstellen**-– Erstellt eines neuen Plan, der über die Attribute verfügt, die im Bereich **Vorgabe**  aktiviert sind. Diese Attribute müssen nicht eindeutig sein. Daher können zwei Pläne denselben Namen und andere Werte haben.
-   **Vorhandenes Budgetplanszenario ersetzen** – Löscht alle Daten im Zielbudgetplan im ausgewählten Budgetplanszenario und erstellt neue Positionen, die die ausgewählten Quelldaten verwenden.
-   **Vorhandenes Budgetplanszenario aktualisieren, neue Daten hinzufügen** – Aktualisiert vorhandene Positionen im Zielplan, damit diese mit den Quellpositionen übereinstimmen, und fügt auch neue Positionen für neue Daten hinzu. Der Abgleich basiert auf dem Sachkonto, dem Datum, der Budgetklasse und verschiedenen anderen Feldern. Wenn Sie zum Beispiel Budgetpläne aus den Prognosepositionen generieren, ist die Positionsnummer ein wichtiges Feld. Alle Positionen, die eine Positionsnummer haben, die mit der Quellpositionsnummer übereinstimmt, werden durch die neuen Positionen aus der Quelle ersetzt.

### <a name="source"></a>Grundlage

Bei allen Prozessen können die Registerkarte **Quelle** Daten filtern, indem die **Filter**-Schaltfläche verwendet wird. Standardmäßig werden bestimmte Felder dem Filter für jeden Prozess hinzugefügt. Beispielsweise sind für den Prozess **Budgetplan aus dem Hauptbuch generieren** die Kategorien **Sachkonto** und **Hauptkonto** verfügbar und erscheinen auf der Generierungsseite. Alle Felder, die Sie dem Filter hinzufügen, werden auch zur Seite hinzugefügt, zusammen mit beliebigen Kriterien, die Sie hinzufügen.

### <a name="target"></a>Ziel

Über die Option **Historisch** auf der Registerkarte **Vorgabe** können Sie die Daten aus den Quelldaten als Gültigkeitsdatum im Budgetplan verwenden. In der Regel muss das Gültigkeitsdatum innerhalb des Budgetzyklus des Plans liegen. Wenn Sie die Option **Historisch** auf **Ja** festlegen, wird das Datum (auch das Jahr) der Quelle verwendet, damit Sie ältere Daten als Grundlage für den Vergleich verwenden können. Sie können historische Daten im Budgetplan nicht ändern, und der Plan wird auf einen genehmigten Workflowstatus festgelegt. Allerdings können Sie den Status zurücksetzen, wenn andere Szenarien im Plan Änderungen erfordern.

Das Feld **Gesamtsumme nach** oben auf der Seite bestimmt auch das Datum, das verwendet wird. In diesem Feld werden die Summen zusammengezählt, und optional wird das Gültigkeitsdatum auf den ersten Tag des Geschäftsjahrs oder des Finanzzeitraums festgelegt. 

Viele der Felder der Registerkarte **Vorgabe** werden bearbeitbar oder schreibgeschützt, abhängig von der Aktivität, die Sie auswählen. Wenn Sie vom Erstellen eines neuen Budgetplans zum Aktualisieren eines vorhandenen Plans wechseln, ist das Feld **Budgetplanname** nicht verfügbar und die Felder, die dem Auswählen eines vorhandenen Plans zugeordnet sind, sind verfügbar. Auf den Registerkarten **Vorgabe** und **Quelle** ist das Feld **Sachkonto**  nie verfügbar, da der Wert vom ausgewählten Budgetplanungsprozess bestimmt wird. 

Im Feld **Budgetklasse** können Sie die Haushaltsplanpositionen entweder als Ausgabenbuchungen oder Umsatzerlösbuchungen festlegen. Normalerweise sind Umsatzerlösbuchungen Habenbeträge auf einem Sachkonto und werden daher als negative Beträge gespeichert. In der Regel werden diese Buchungen auch als negative Beträge im Budgetplan angezeigt. Indem Sie die Budgetklasse jedoch als Feld im Planlayout hinzufügen, können Sie festlegen, dass der Umsatzerlös als positive Beträge angezeigt wird.

### <a name="generation-rules"></a>Erstellungsregeln

Drei Felder enthalten zusätzliche Funktionen: **Faktor-**, **Minimum-** und **Rundung-****Regel**. 

Der Wert im Feld **Faktor** wird durch den Quellbetrag multipliziert, um den Betrag im Budgetplan festzulegen. Sie können dann Anpassungen vornehmen, wenn Sie die Budgetplanpositionen erstellen. Sie können beispielsweise **1,03** für eine 3-Prozent-Zunahme eingeben. Der Faktor muss ein positive Zahl sein. 

Im Feld **Minimum** können Sie den Schwellenbetrag zum Erstellen einer Budgetplanposition festlegen. Wenn der Quellbetrag kleiner als diese Nummer ist, wird die Budgetplanposition nicht erstellt. Ein Wert von **0.00** ermöglicht alle Beträge, begrenzt Zeilen jedoch nicht auf positive Beträge. (Keine Wertbegrenzungszeilen für positive Beträge). Negative Beträge sind immer enthalten und enthalten normalerweise Habenbuchungen.)

Im Feld **Rundungsregel** können Sie die Genauigkeit der Budgetplanpositionen festlegen, die erstellt werden. Sie können Beträge auf die nächsten 1,00, 10,00, 100,00 usw. der Währung runden.

## <a name="notes-for-specific-processes"></a>Hinweise für bestimmte Prozesse
### <a name="generate-budget-plan-from-general-ledger"></a>Budgetplan aus dem Hauptbuch generieren

Wenn Sie einen Budgetplan aus den Hauptbuchdaten erstellen, müssen Sie das Feld **Gesamtsumme nach** auf **Geschäftsjahr** festlegen, wenn die Option **Historisch** auf **Nein** festgelegt ist. Die Zeiträume und Daten in der Quelle entsprechen möglicherweise nicht die Zeiträumen in den Datumsangaben im Ziel. Da der Prozess keine zuverlässige Methode hat, diese Werte zuordnen, müssen Sie den Prozess auf den ersten des Jahres einschränken. 

Im Ziel ist das Feld **Budgetklasse** entweder auf **Ausgaben** oder **Umsatzerlös** festgelegt. Diese Einstellung wird verwendet, um das Attribut **Budgettyp** für Positionen auszuwählen, die erstellt werden, wenn das Hauptkonto in einer Position nicht von Typ **Umsatzerlös** oder **Ausgaben** ist.

### <a name="generate-budget-plan-from-fixed-assets"></a>Budgetplan aus Anlagen generieren

Der Prozess **Budgetplan aus Anlagen generieren**  ist keine Option für das Aggregieren nach Zeitraum oder Tag. Es gibt auch keine Option für das Festlegen des Plans als historisch. Sie können dieses periodische Verarbeitung verwenden, um geplante Buchungen für Anlagen in der Budgetplanung einzubeziehen.

### <a name="generate-budget-plan-from-forecast-positions"></a>Budgetplan aus Planpositionen generieren

Der Prozess **Budgetplan aus Planpositionen generieren** weist die Quellplanungsposition zur Budgetplanposition zu. Sie können die Position anzeigen, indem Sie entweder die Planungsposition als Zeile im Budgetplanlayout hinzufügen oder die Abfrage **Budgetplanpositionen** verwenden. Wenn Sie nicht möchten, dass die Prognoseposition zu den Budgetplanpositionen zugewiesen werden, legen Sie die Option **Position in Budgetplanposition einbeziehen** auf **Nein** fest.

Positionen werden im Budgetplan nach Sachkonto und Position zusammengefasst. Allerdings können Sie die Positionsnummer ausschließen, damit nur Positionen nach Sachkonto zusammengefasst werden. Legen Sie auf der Registerkarte **Vorgabe** die Option **Position in Budgetplanposition einbeziehen** auf **Nein** fest.

Im Feld **Vollzeitäquivalent-Szenario für Budgetplan** können Sie ein Szenario auswählen, um die Anzahl von Vollzeitentsprechungen (FTEs) in den Budgetplan einzubeziehen. Das Feld ist für Szenarien des Mengentyps beschränkt, die im Layout des Zielbudgetplans enthalten sind. Wenn Sie ein FTE-Szenario auswählen, müssen Sie auch ein FTE-Hauptkonto auswählen. Dieses Konto wird verwendet, um die Positionen des Mengen der Budgetplanpositionen zu erstellen. 

Der Budgetplanungsprozess und das Budgetplanszenario, die in der Quelle ausgewählt werden, legen den Budgetplanungsprozess und das Budgetplanszenario im Zielszenario. Da diese Attribute den Planungspositionen zugewiesen werden, müssen mit dem Budgetplan übereinstimmen. Daher können diese Attribute nicht im Ziel geändert werden.

### <a name="generate-budget-plan-from-project-forecasts"></a>Budgetplan aus Projektplanungen generieren

Der Prozess **Budgetplan aus Projektplanungen generieren** genau wie der Prozess **Budgetplan aus Planpositionen generieren** haben eine Option, Projektmengen (Stunden, Ausgaben und Artikel) in ein Mengenszenario einzubeziehen. Die zwei Prozess haben auch ähnliche Filter für die Spalten im Budgetplanlayout. 

Auf der Registerkarte **Quelle** bestimmen drei Optionen im Abschnitt **Auszug einbeziehen**, welche Haushaltsplanpositionen erstellt werden. Diese Optionen sind die gleichen wie die Optionen, die verfügbar sind, wenn Sie Budgetregistereinträge direkt von Projektplanungen erstellen. Legen Sie die Option **Gewinn und Verlust** auf **Ja** fest, um Positionen für Kosten und Umsatzerlöse zu erstellen. Legen Sie die Option **RIF** auf **Ja** fest, um Ressource in Fertigungen-Einträge zu erstellen. Legen Sie die Option **Lohnzuweisung** auf **Ja** fest, um Positionen für die Lohngegenkonten für Stundenbuchungen zu erstellen. 

Es gibt kein Feld **Budgetklasse**, da die Budgetklasse (**Ausgaben** oder **Umsatzerlös** von der Quelle bestimmt wird. 

Sie können Projektbudgets als Quelle nutzen, indem Sie das Planzahlenmodell auswählen, das die Projektbudgetbeträge enthält. Bedenken Sie, dass Projektbudgets Projektplanungseinträge erstellen, während diese genehmigt werden.

Um nur Kosten oder Umsatzerlöse für Budgetplanpositionen auszuwählen, verwenden Sie den Filter, um **Budgetaktualisierungen: Betragsart = Kosten** auszuwählen. Um nur einen Typ der Planung auszuwählen, verwenden Sie den Filter, um **Budgetaktualisierungen: Buchungsart = *xxx*** auszuwählen. 

Es kann nur ein Planzahlenmodell verwendet werden, um ein Budgetplanszenario zu generieren. Wenn Sie den Prozess für ein Planzahlenmodell ausführen und dann eine Aktualisierung ausführen und versuchen, ein anderes Modell anzugeben, wird das erste Modell überschrieben, wenn das gleiche Projekt und die gleichen Sachkonten gelten. Wenn Sie ein Budgetplanszenario aus mehr als einem Planzahlenmodell generieren möchten, generieren Sie in verschiedene Budgetplanszenarien, und verwenden Sie Zuteilungsoptionen, um sie in einem anderen Szenario zu addieren. 

Der Prozess **Budgetplan aus Projektplanungen generieren** weist auch das Quellprojekt zur Budgetplanposition zu.

### <a name="generate-budget-plan-from-supply-forecast"></a>Budgetplan aus Beschaffungsplanung generieren

Die Quellfilteroptionen im Prozess **Budgetplan aus Beschaffungsplanung generieren** wurden nach Optionen in der Funktion **Einkaufsbudget in Sachkonto übertragen** aufgrund der Ähnlichkeiten zwischen dem Prozess und der Funktion modelliert.

### <a name="generate-budget-plan-from-demand-forecast"></a>Budgetplan aus Bedarfsplanung generieren

Für den Prozess **Budgetplan aus Bedarfsplanung generieren** können Sie die Option **Auftrag** auf **Ja** festlegen, um Umsatzerlöspositionen im Budgetplan zu generieren, den **Verbrauch** auf **Ja** setzen, um Ausgabenpositionen zu erstellen, oder beide Optionen auf **Ja** festlegen.

### <a name="generate-budget-plan-from-budget-register-entries"></a>Budgetplan aus Budgetregistereinträgen erstellen

Für den Prozess **Budgetplan aus Budgetregistereinträgen erstellen** muss die Quelle ein Teilmodell, einen Budgetcode und eine Positionsnummer angeben. Das bedeutet, dass Sie Budgetplanpositionen nur für einen Budgetregistereintrag gleichzeitig erstellen können. Sie können zusätzliche Einträge im gleichen Budgetplan nutzen, indem Sie die Prozess nacheinander für jeden Quelleintrag ausführen.

### <a name="generate-budget-plan-from-budget-plan"></a>Budgetplan aus Budgetplan generieren

Für den Prozess **Budgetplan aus Budgetplan generieren** ermöglicht ein zusätzlicher Satz an Optionen auf der Registerkarte **Vorgabe**, neue Finanzdimensionen zuzuteilen. Wenn eine Finanzdimension ausgewählt ist, wird dieser Wert für alle Budgetplanpositionen verwendet. Daher können Sie einen Budgetplan als Grundlage für andere Budgetpläne verwenden, Sie können aber auch beispielsweise eine andere Abteilung oder Kostenstelle zu den neuen Budgetplänen zuweisen.

## <a name="looking-back-from-the-budget-plan"></a>Zurückgehen vom Datum des Budgetplans
### <a name="budget-plans-by-dimension-set-inquiry"></a>Budgetpläne nach Dimensionssätzen – Abfrage

Die Abfrage **Budgetpläne nach Dimensionssätzen** umfasst mehrere Optionen, über die Sie eine Abfrage ausführen lassen können, um die Quelle der Budgetplandaten zu identifizieren. 

Wählen Sie eine Position aus, und klicken Sie auf die Schaltfläche **Budgetplanpositionen**, um die Abfrage **Budgetplanpositionen** auszuführen. Die Ergebnisse werden für die Dimensionswerte der ausgewählten Position gefiltert. Sie können dann zusätzliche Parameter anwenden. 

Verwenden Sie die Schaltflächen **Beschaffungsplanung** und **Bedarfsplanung**, um diese Abfragen auszuführen. In beiden Fällen sucht die Abfrage nach Planungspositionen, die die Budgetplanpositionen erstellt haben könnten. 

Zusätzliche Berichte, die verfügbar sind, sind zum Beispiel **Planpositionen nach Budgetplan**. Dieser Bericht ist insbesondere dann hilfreich, wenn Sie feststellen möchten, ob eine Position korrekt zu den Budgetplänen zugewiesen wurde.




