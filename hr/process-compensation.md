---
title: "Vergütung verarbeiten"
description: "Die Vergütungsverarbeitung ermöglicht Ihnen die Berechnung neuer Grundvergütungsbeträge für Mitarbeiter basierend auf Eigenkapitalanpassungen, Verdiensterhöhungsziele und Leistungsfähigkeit."
author: kherr
manager: AnnBe
ms.date: 07/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 6e30357b0bca8745b69bff19a55828b180c3b829
ms.contentlocale: de-de
ms.lasthandoff: 06/13/2017


---

# <a name="process-compensation"></a>Vergütung verarbeiten
Die Vergütungsverarbeitung ermöglicht Ihnen die Berechnung neuer Grundvergütungsbeträge für Mitarbeiter basierend auf Eigenkapitalanpassungen, Verdiensterhöhungsziele und Leistungsfähigkeit. Dieser Beitrag enthält Informationen zum grundlegenden Ablauf der Vergütungsverarbeitung für feste Vergütungspläne ohne Berücksichtigung der Leistung.

## <a name="plan-the-new-compensation-amounts-and-budgets"></a>Planen neuer Vergütungsbeträge und Budgets
Um Ihren Mitarbeiter eine Gehaltserhöhung zu bieten, müssen Sie ein Budget für feste Erhöhung für die einzelnen Abteilungen festlegen: Vergütungsverwaltung > Verknüpfungen > Verdiensterhöhungsziele. (Alternativ können Sie dieses Formular auch über die Abteilung öffnen: Organisation > Abteilungen.) Hier können Sie angeben, ob Mitarbeiter einer bestimmten Gewerkschaft oder an eines bestimmten Standorts einen anderen Erhöhungsbetrag erhalten sollen. Die Felder **Budget** und **Währung** dienen zu Informationszwecken und können verwendet werden, um einen Währungsbetrag für das Budget zu notieren.

## <a name="set-up-the-compensation-process"></a>Vergütungsprozess einrichten
Ein Prozessereignis ermöglicht Ihnen, die Parameter für die Vergütungsverarbeiten anzugeben. Dazu zählen die Datumsperiode zur Bewertung der Bestimmung der Vergütungsbeträge.  und das Datum, zu dem die neuen Vergütungsbeträge wirksam werden sollen.

Optional können Sie auch einen festen Lohn (anteilig) auf Basis des Einstellungsdatums einschließen, wenn einer der festen Vergütungspläne eine Einstellungsregel nach Prozent verwendet. Bei diesen Plänen erhält jeder, der nach dem Startdatum des Zyklus und vor dem Einstellungsdatum für festen Lohn (anteilig) eingestellt wurde 100 % der berechneten Vergütungserhöhung oder der allgemeinen Erhöhung. Jedermann, der nach dem Einstellungsdatum für den festen Lohn (anteilig) auf Basis des Einstellungsdatums und vor dem Zyklusenddatum eingestellt wurde, erhält einen Anteil der berechneten Erhöhung basierend auf der Anzahl der Tage, die er außerhalb der gesamten Zyklustage angestellt war. Wenn beispielsweise unser Zyklus vom 01. Januar bis zum 31. Dezember ausgeführt wird und das Einstellungsdatum für festen Lohn (anteilig) ist der 01. April, dann erhält ein Mitarbeiter, der im März eingestellt wurde, die volle berechnete Erhöhung, während ein Mitarbeiter, der am 01. Juli eingestellt wurde, ungefähr die Hälfe der berechneten Erhöhung erhält.

Das Prozessereignis **Zeitpunkt**-Datum wird nur für die Verarbeitung bestimmter variabler Vergütungspläne verwendet und wird von diesem Blogbeitrag nicht abgedeckt. **Stichtag überprüfen** ist der Stichtag für Empfehlungen, sodass die neuen Vergütungsbeträge in den Datensatz des Mitarbeiters geladen werden können. Das Prüfungsdatum dient nur zur Information.

Nachdem die Parameter des Prozessereignisses gespeichert wurden, können Sie auf die Schaltfläche **Einstellungen** klicken, um die Pläne anzuzeigen, die in diese Prozessausführung einzubeziehen sind und welche Aktivitäten bezüglich fester Vergütung für jeden Plan zu ergreifen sind.

Klicken Sie auf die Schaltfläche **Hinzufügen** in der oberen Registerkarte, um einem Vergütungsplan zum Prozessereignis hinzuzufügen. Die Spalten **Andere Hebelwirkung verwenden**, **Hebelwirkungsfaktor** Und **Hebelwirkung (Beschreibung)** werden nur für Pläne für variable Vergütung verwendet und in diesem Beitrag nicht weiter beschrieben.

Speichern Sie den Datensatz, und klicken Sie anschließend auf die Schaltfläche **Hinzufügen** in der unteren Registerkarte, um Aktivitäten bezüglich fester Vergütung für den ausgewählten Plan hinzuzufügen. Verwenden Sie die Option zum Aktivieren einer Empfehlung, wenn Sie einen anderen Betrag eingeben möchten, der nicht mit der berechneten Durchschnittserhöhung übereinstimmt. Wenn Sie eine Aktivität basierend auf dem Ergebnis der vorherigen Aktivität berechnen möchten, um mehrere Vergütungsaktivitäten zu verknüpfen, dann markieren Sie die Option „Vorheriges Ergebnis verwenden“. Aktivitäten fester Vergütung sind Typen einer Vergütungslogik, denen Sie beschreibende Namen zuweisen können. Für Klassen- und Bereichspläne können Sie nur Aktivitäten bezüglich fester Vergütung der folgenden Typen zuweisen:

| Typ der Aktivität für feste Vergütung | Funktionen                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Eigenkapital                        | Eigenkapitalaktivitäten vergleichen den Lohnsatz des Mitarbeiters ab dem Enddatum des Zyklus mit dem niedrigsten Referenzpunkt für die Ebene, die im Einzelvorgang des Mitarbeiters angegeben ist. Wenn der Lohnsatz des Mitarbeiters geringer ist als der Mindestbetrag des Referenzpunkt, wird die Erhöhung, die erforderlich ist, damit der Mitarbeiter den Mindestbetrag erreicht, berechnet.                                                                                |
| Verdienst                         | Verdienstaktivitäten berechnen eine Erhöhung basierend auf dem Lohnsatz des Mitarbeiters ab dem Zyklusenddatum und den Erhöhungssatz (in Prozent) aus dem Budget für feste Erhöhung für die Abteilung, Gewerkschaft und den Standort des Mitarbeiters.                                                                                                                                                                                         |
| Allgemein                       | Allgemeine Aktivitäten berechnen eine Erhöhung auf Basis eines Prozentsatzes oder weisen dem Mitarbeiter einen Pauschalbetrag zu. Diese wird auf Grundlage der Einstellungen für „Feste Vergütung“ auf der Registerkarte „Allgemeines“ bestimmt.                                                                                                                                                                                                                        |
| Beförderung                     | Beförderungsaktivitäten stellen Ihnen einen benannten Platz zur Verfügung, an dem Sie die Erhöhung zuweisen können. Stellen Sie deshalb sicher, dass Sie die Option für **Empfehlung aktivieren** ausgewählt haben, damit Sie Empfehlungen für Mitarbeiter eingeben können, die Aktionen erhalten.  Bei Mitarbeitern ohne eine empfohlene Erhöhung wird keine Aktionsaktivität zu den Datensätzen für eine feste Vergütung hinzugefügt.                                                                       |
| Änderung einer anderen Ebene            | Im vorherigen Beispiel ist Zurückstufung der Name für unsere Aktivität bezüglich fester Vergütung. Der Typ ist „Änderung einer anderen Ebene“. Dadurch wird eine Durchschnittserhöhung von 0 (Nulländerung) generiert, sodass sie einen Empfehlungsbetrag eingeben können, um den Lohnsatz des Mitarbeiters anzupassen. (Stellen Sie sicher, die Option für **Empfehlung aktivieren** aktiviert ist.) Bei Mitarbeitern ohne Empfehlung ist diese Aktivität nicht zu den Datensätzen für feste Vergütung hinzugefügt. |

Sie können nur Aktivitäten bezüglich fester Vergütung vom Typ „Schritt“ zu einem Schrittplan hinzufügen.

| Typ der Aktivität für feste Vergütung | Funktionen                                                                                                                                                                                           |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Schritt                           | Geben Sie auf der Registerkarte „Allgemeines“, ob diese Schrittaktivität die Mitarbeiter 0, 1 oder zwei 2 Stufen voranbringen soll.                                                                                  |
|                                | **0 Schritte** – Der Mitarbeiter erhält den Lohnsatz für seinen aktuellen Schritt.                                                                                                                      |
|                                | **1 Schritt** – Das System prüft, ob der Mitarbeiter bereits am letzten Referenzpunkt seiner Ebene angekommen ist.                                                                                             |
|                                | **2 Schritte** –-Das System befördert den Mitarbeiter auf seiner Ebene zwei Schritte nach oben. Das System beförderte möglicherweise den Mitarbeiter nur einen oder keinen Schritt, wenn der letzte Referenzpunkt der Ebene erreicht ist. |

## <a name="run-the-compensation-process"></a>Ausführen des Vergütungsprozesses
Nachdem das Prozessereignis mit den erforderlichen Datumsfeldern, Plänen und Aktivitäten eingerichtet wurde, klicken Sie auf **Prozess ausführen** auf der Prozessereignisseite. Dadurch wird das Dialogfeld für das Ausführen von Vergütungsprozessereignissen geöffnet. Innerhalb dieses Dialogfelds können Sie auf die Option **Ergebnisse der Verarbeitung anzeigen** klicken, um zu sehen, wie die Vergütungsbeträge für jeden Mitarbeiter berechnet wurden. **OK** führt den Vergütungsprozess für alle Mitarbeiter aus, die in den ausgewählten Vergütungsplänen ab Zyklusendedatum enthalten sind.

## <a name="view-the-process-results"></a>Prozessergebnisse anzeigen
Um die Prozessergebnisse anzuzeigen, öffnen Sie die Seite **Prozessergebnisse**. Jedes Mal, wenn ein Prozessereignis ausgeführt wird, wird ein neues Vergütungsereignis erstellt. Auf diese Weise können Sie Probeläufe durchführen, Anpassungen vornehmen und das Vergütungsereignis mehrere Male ausführen, um verschiedene Auswirkungen auf die Mitarbeitervergütung anzuzeigen.

Die Seite für Prozessergebnisse enthält Informationen über den Prozesslauf, einschließlich Datum der Ausführung, Mitarbeiter, der den Prozess ausgeführt hat und ob es Fehler bei der Prozessausführung gab. Sie können auch die Option **Gesperrt** markieren, um die Schaltfläche **Vergütung laden** zu deaktivieren und zu verhindern, das jemand die Vergütungsereignisse in die Mitarbeiterdatensätze lädt. Durch Klicken auf die Schaltfläche für **Mitarbeiterergebnisse** wird die Liste der Mitarbeiter angezeigt, die in der Ausführung enthalten sind.

Der Mitarbeiterergebnisse zeigen Informationen zum Prozess selbst sowie zu Vergütungsaktivitäten an, die im Prozess ausgeführt wurden. Der Abschnitt für feste Vergütung enthält Datensätze für die einzelnen Aktivitäten, die im Prozessereignis für den Vergütungsplan enthalten sind. Die Spalten für aktuelle Richtlinien und Empfehlungen zeigen weitere Informationen für die Aktivität an, die im Abschnitt „Feste Vergütung“ ausgewählt sind. Wurde für die Aktivität die Option zum Aktivieren von Empfehlungen gewählt, sind die Felder „Empfehlung“ editierbar. Dadurch können Sie manuell die Beträge für Mitarbeiter anpassen. Hinweis: Wenn Sie „Vorheriges Ergebnis verwenden“ für die Aktivität zum Prozessereignis aktiviert haben, müssen Sie die Beträge für alle abhängigen Aktivitäten manuell aktualisieren.

Sobald die Vergütungsbeträge für einen Mitarbeiter überprüft und Anpassungen an den empfohlenen Werten vorgenommen wurden, können Sie den **Status** der **Mitarbeiterereignis**-Position ändern, um anzugeben, ob das Ereignis genehmigt wurde oder ignoriert werden soll. Optional können Sie alle Änderungen löschen, die an der Empfehlung für den Mitarbeiter vorgenommen wurden, indem Sie auf die Schaltfläche **Neu berechnen** klicken. Dadurch erhält das vorhandene Mitarbeiterereignis den Status "Ignorieren" und es wird ein neues Mitarbeiterereignis mit neu berechneten Werten erstellt.

## <a name="loading-approved-compensation-changes"></a>Laden genehmigter Vergütungsänderungen
Sobald der Status von einem oder mehren Mitarbeiterereignissen zu „Genehmigt“ aktualisiert wurde, können sie in den Datensätzen für feste Vergütung der Mitarbeiter geladen werden. Dies geschieht entweder durch die Auswahl (nacheinander) der einzelnen Mitarbeiterereignisse und klicken auf die Schaltfläche „Mitarbeitervergütung laden“ auf der Seite „Mitarbeiterergebnisse“ oder durch klicken auf **Vergütung laden** auf der Seite „Prozessergebnisse“, um alle genehmigten Mitarbeiterereignisse auf einmal zu laden.

Durch Klicken auf **OK** im Dialogfeld **Vergütung laden** werden Vergütungsaktivitätspositionen ungleich Null zur Seite **Feste Mitarbeitervergütung** hinzugefügt.

