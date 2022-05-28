---
title: Vergütung verarbeiten
description: Die Vergütungsverarbeitung ermöglicht Ihnen die Berechnung neuer Grundvergütungsbeträge für Mitarbeiter basierend auf Eigenkapitalanpassungen, Verdiensterhöhungsziele und Leistungsfähigkeit.
author: twheeloc
ms.date: 08/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: e4aa910d92c2905d54d96f656e1d3d1c36388636
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8693863"
---
# <a name="process-compensation"></a>Vergütung verarbeiten


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Die Vergütungsverarbeitung ermöglicht Ihnen die Berechnung neuer Grundvergütungsbeträge für Mitarbeiter basierend auf Eigenkapitalanpassungen, Verdiensterhöhungsziele und Leistungsfähigkeit. Dieses Thema beschreibt den grundlegenden Ablauf der Vergütungsverarbeitung für feste Vergütungspläne, ohne die Leistung eines Mitarbeiters zu faktorieren.

## <a name="plan-the-new-compensation-amounts-and-budgets"></a>Planen neuer Vergütungsbeträge und Budgets
Um Ihren Mitarbeitern eine Verdiensterhöhung zu geben, müssen Sie ein festes Erhöhungsbudget für jede Ihrer Abteilungen einrichten: **Vergütungsverwaltung** > **Links** > **Verdiensterhöhungsziele**. (Alternativ können Sie diese Seite über die Abteilung: **Organisation** > **Abteilungen** öffnen.) Sie können angeben, ob Mitarbeiter in einer bestimmten Gewerkschaft oder an einem bestimmten Standort eine andere prozentuale Erhöhung erhalten sollen. Die Felder **Budget** und **Währung** dienen zu Informationszwecken und können verwendet werden, um einen Währungsbetrag für das Budget zu notieren.

## <a name="set-up-the-compensation-process"></a>Vergütungsprozess einrichten
Auf der Seite **Vergütungsprozesse** können Sie die Parameter für die Vergütungsverarbeitung festlegen. Dies umfasst den Datumszeitraum, der für die Ermittlung der Vergütungsbeträge verwendet wird, und das Datum, an dem die neuen Vergütungsbeträge wirksam werden sollen.

Optional können Sie eine **feste Zahlung anteilig im Hinblick auf das Einstellungsdatum** aufnehmen, wenn einer Ihrer festen Vergütungspläne eine prozentuale Einstellungsregel verwendet. Für diese Pläne erhält jeder, der nach dem **Zyklusstart**-Datum und vor dem **Datum für die anteilige feste Vergütung eingestellt wurde**, 100 % der berechneten Zulage oder die allgemeine Erhöhung. Jeder, der nach dem Datum für die **anteilige feste Vergütung eingestellt wurde**, und vor dem **Zyklusenddatum**, erhält einen Anteil der berechneten Erhöhung basierend darauf, wie viele Tage des Gesamtzyklus er beschäftigt war. Wenn Ihr Zyklus beispielsweise vom 1. Januar bis 31. Dezember geht und es eine feste Zahlung anteilig ab dem Einstellungsdatum vom 1. April gibt, erhält ein Mitarbeiter, der im März eingestellt wird, die vollständige berechnete Erhöhung, während ein Mitarbeiter, der am 1. Juli eingestellt wird, etwa die hälfte der berechneten Erhöhung erhält.

Das **Stichtag**-Datum für das Prozessereignis wird nur für die Verarbeitung bestimmter variabler Vergütungspläne verwendet und wird hier nicht beschrieben. **Stichtag überprüfen** ist der Stichtag für Empfehlungen, sodass die neuen Vergütungsbeträge in den Datensatz des Mitarbeiters geladen werden können. Das Prüfdatum dient ausschließlich zu Informationszwecken.

Nachdem die Parameter des Prozessereignisses gespeichert wurden, können Sie auf die Schaltfläche **Einrichtung** klicken, um die Pläne auszuwählen, die bei der Ausführung des Prozesses berücksichtigt werden sollen, und anzugeben, welche festen Vergütungsaktivitäten für jeden Plan unternommen werden sollen.

Klicken Sie auf der Registerkarte **Pläne** auf die Schaltfläche **Hinzufügen**, um dem Prozessereignis einen Vergütungsplan hinzuzufügen. Die Spalten **Anderer Einfluss**, **Einflussfaktor** und **Einflussbeschreibung** werden nur für variable Vergütungspläne verwendet und werden in diesem Thema nicht beschrieben.

Speichern Sie den Datensatz und klicken Sie dann auf der Registerkarte **Aktivitäten** auf die Schaltfläche **Hinzufügen**, um dem ausgewählten Plan feste Vergütungsaktivitäten hinzuzufügen. Verwenden Sie die Option **Empfehlung aktivieren**, um einen anderen Betrag einzugeben, als die berechnete Richtlinienerhöhung für die Aktivität. Um eine Aktion zu berechnen, die auf dem Ergebnis der vorherigen Aktion basiert und so mehrere Ausgleichsaktionen zu verknüpfen, markieren Sie die Option **Vorheriges Ergebnis verwenden**. Feste Vergütungsaktionen sind Arten von Vergütungslogiken, denen Sie beschreibende Namen geben können. Für **Branche** und **Band** Pläne können Sie nur feste Vergütungsaktionen hinzufügen, die zu den folgenden Typen gehören:

| Typ der Aktivität für feste Vergütung | Funktionen                  |
|-------------------------------|-------------------------------------------------------------------------|
| Eigenkapital                        | Eigenkapitalaktivitäten vergleichen den Lohnsatz des Mitarbeiters ab dem Enddatum des Zyklus mit dem niedrigsten Referenzpunkt für die Ebene, die im Einzelvorgang des Mitarbeiters angegeben ist. Wenn der Lohnsatz eines Mitarbeiters niedriger als der niedrigste Referenzpunkt ist, wird die Erhöhung berechnet, die notwendig ist, um den Mitarbeiter auf den Mindestpunkt in dem Bereich zu bringen.                                                                                |
| Verdienst                         | Vergütungsaktivitäten berechnen eine Erhöhung basierend auf dem Lohnsatz des Mitarbeiters zum Enddatum des Zyklus, ebenso wie nach der prozentualen Erhöhung, wie im Budget für die feste Erhöhung für die Abteilung des Mitarbeiters, die Gewerkschaft und den Standort vorgegeben.                                                                                                                                                                                         |
| Allgemein                       | Allgemeine Aktivitäten berechnen eine Erhöhung basierend auf einem Prozentwert oder geben den Mitarbeitern einen Pauschalbetrag. Dieser wird basierend auf den Einstellungen für **Feste Vergütung** auf der Registerkarte **Allgemein** bestimmt.                                                                                                                                                                                                                        |
| Beförderung                     | Beförderungsaktionen bieten Ihnen einen benannten Ort, an dem Sie Erhöhungen vergeben können. Markieren Sie die Option **Empfehlung aktivieren**, um eine Empfehlung für Mitarbeiter einzugeben, die befördert werden.  Mitarbeitern ohne empfohlene Erhöhung wird die die **Beförderung**-Aktivität nicht zu ihren Datensätzen für die feste Vergütung hinzugefügt.                                                                       |
| Änderung einer anderen Ebene            | Im obigen Beispiel hat unsere **Feste Vergütung**-Aktion den Namen **Zurückstufung** mit dem Typ **Änderung einer anderen Ebene**. Dadurch wird eine Durchschnittserhöhung von 0 (Nulländerung) generiert, sodass sie einen Empfehlungsbetrag eingeben können, um den Lohnsatz des Mitarbeiters anzupassen. (Wählen Sie die Option **Empfehlung aktivieren** aus). Mitarbeitern ohne Empfehlung wird diese Aktivität nicht zu ihren Datensätzen für die feste Vergütung hinzugefügt. |

Sie können nur **Feste Vergütung**-Aktivitäten mit einem Schrittplan hinzufügen.

| Typ der Aktivität für feste Vergütung | Funktionen                |
|--------------------------------|------------------------------|
| Schritt                           | Geben Sie auf der Registerkarte **Allgemein** an, ob diese Schrittaktivität die Mitarbeiter 0, 1 oder zwei 2 Stufen voranbringen soll.                                                                                  |
|                                | **0 Schritte** – Der Mitarbeiter erhält den Lohnsatz für seinen aktuellen Schritt.                                                                                                                      |
|                                | **1 Schritt** – Das System prüft, ob der Mitarbeiter bereits am letzten Referenzpunkt seiner Ebene angekommen ist.                                                                                             |
|                                | **2 Stufen** - Der Mitarbeiter rückt zwei Stufen auf seiner aktuellen Ebene vor. Der Mitarbeiter kann nur eine oder null Stufen aufsteigen, wenn er den letzten Referenzpunkt für seine Stufe erreicht. |

## <a name="run-the-compensation-process"></a>Ausführen des Vergütungsprozesses
Nachdem das Prozessereignis mit den erforderlichen Datumsfeldern, Plänen und Aktivitäten eingerichtet wurde, klicken Sie auf **Prozess ausführen** auf der Seite **Prozessereignis**. Dadurch wird das Dialogfeld **Vergütungsverarbeitungsereignisse ausführen**. Klicken Sie auf die Option **Ergebnisse der Verarbeitung anzeigen**, um zu sehen, wie die Vergütungsbeträge für jeden Mitarbeiter berechnet wurden. **OK** führt den Vergütungsprozess für alle Mitarbeiter aus, die in den ausgewählten Vergütungsplänen ab Zyklusendedatum enthalten sind.

## <a name="view-the-process-results"></a>Prozessergebnisse anzeigen
Um die Prozessergebnisse anzuzeigen, öffnen Sie die Seite **Prozessergebnisse**. Jedes Mal, wenn ein Prozessereignis ausgeführt wird, wird ein neues Vergütungsereignis erstellt. Auf diese Weise können Sie Probeläufe durchführen, Anpassungen vornehmen und das Vergütungsereignis mehrere Male ausführen, um verschiedene Auswirkungen auf die Mitarbeitervergütung anzuzeigen.

Die Seite **Prozessergebnisse** enthält Informationen über die Prozessausführung, einschließlich dem Zeitpunkt, wann die Ausführung stattgefunden hat, dem Benutzer, der den Prozess ausgeführt hat, und ob während der Prozessausführung Fehler aufgetreten sind. Wählen Sie die Option **Gesperrt** aus, um die Schaltfläche **Vergütung laden** zu deaktivieren und zu verhindern, das jemand die Vergütungsereignisse in die Mitarbeiterdatensätze lädt. Durch Klicken auf die Schaltfläche für **Mitarbeiterergebnisse** wird die Liste der Mitarbeiter angezeigt, die in der Ausführung enthalten sind.

Die Option **Mitarbeiterergebnisse** zeigt Informationen über den eigentlichen Prozess an, ebenso wie für im Prozess durchgeführte Vergütungsaktivitäten. Der Abschnitt **Feste Vergütung** enthält einen Datensatz für alle im Prozessereignis für den Vergütungsplan enthaltenen Aktivitäten. Die Spalten **Aktuelle Richtlinie** und **Empfehlung** zeigen weitere Informationen für die im Abschnitt **Feste Vergütung** ausgewählte Aktivität. Wenn **Empfehlungen aktivieren** für die Aktivität gekennzeichnet wurde, können die Felder **Empfehlung** bearbeitet werden. Dadurch können Sie manuell die Beträge für Mitarbeiter anpassen. Beachten Sie, dass wenn Sie **Vorheriges Ergebnis verwenden** für die Aktivität für das Prozessereignis gekennzeichnet haben, die Beträge für alle davon abhängigen Aktivitäten manuell aktualisiert werden müssen.

Wenn die Vergütungsbeträge für einen Mitarbeiter überprüft wurden und alle Anpassungen an die empfohlenen Werte durchgeführt wurden, können Sie den **Status** in der **Mitarbeiterereignis**-Position ändern, um anzuegeben, ob das Ereignis genehmigt wurde oder ignoriert werden soll. Optional können Sie alle Änderungen löschen, die an der Empfehlung für den Mitarbeiter vorgenommen wurden, indem Sie auf die Schaltfläche **Neu berechnen** klicken. Dadurch erhält das vorhandene Mitarbeiterereignis den Status "Ignorieren" und es wird ein neues Mitarbeiterereignis mit neu berechneten Werten erstellt.

## <a name="loading-approved-compensation-changes"></a>Laden genehmigter Vergütungsänderungen
Wenn für ein oder mehrere Mitarbeiterereignisse der Status in **Genehmigt** geändert wurde, können sie in die festen Vergütungsdatensätze des Mitarbeiters geladen werden. Dies kann erfolgen, indem jedes Mitarbeiterereignis einzeln ausgewählt wird und auf der Seite **Mitarbeiterergebnisse** auf die Schaltfläche **Mitarbeitervergütung laden** geklickt wird, oder indem auf der Seite **Ergebnisse bearbeiten** auf die Schaltfläche **Vergütung laden** geklickt wird, um alle genehmigten Mitarbeiterereignisse gleichzeitig zu laden.

Durch Klicken auf **OK** im Dialogfeld **Vergütung laden** werden Vergütungsaktivitätspositionen ungleich Null zur Seite **Feste Mitarbeitervergütung** hinzugefügt.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
