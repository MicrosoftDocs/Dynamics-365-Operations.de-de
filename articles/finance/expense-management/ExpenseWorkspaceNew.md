---
title: Ausgabenberichte neu gestaltet
description: Dieses Thema enthält Informationen über die neu entworfene und neu gestaltete Erfahrung für Ausgabenberichte in Microsoft Dynamics 365 Finance. Die neue Erfahrung vereinfacht den Prozess der Ausgabenberichte und verkürzt die Zeit, die dafür erforderlich ist.
author: ryansandness
manager: AnnBe
ms.date: 06/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2019-6-30
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 8a8ad1ad84b8acaa54d8b03327157a930e562f59
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187658"
---
# <a name="expense-reports-reimagined"></a>Ausgabenberichte neu gestaltet

[!include[banner](../includes/banner.md)]

Die Ausgabenberichtseingabe wurde neu gestaltet, um den Prozess für die Erledigung des Ausgabenberichts zu vereinfachen und die Zeit, die dazu benötigt wird, zu reduzieren. Hier sind die wichtigsten Punkte der neuen Ausgabenenerfahrung:

- Ein neuer Spesenverwaltungsarbeitsbereich, über den Sie auf die Ausgabes Ihres Delegats zugreifen können.
- Ein neue Funktion, um Belege abzustimmen, um an Kopfzeilen angehängte Belege besser anzuzeigen und um den Prozess für das Anfügen von Belegen zu Ausgabenzeilen zu vereinfachen.
- Ein neuer schreibgeschützter Raster, mit dem Sie viele weitere Ausgabenzeilen und zusätzliche Datenspalten anzeigen können. Sie können nun alle aufgeschlüsselten und geteilten Positionen zusammen mit deren übergeordneten Ausgaben anzeigen.
- Ein vereinfachter Bereich zur Bearbeitung von Ausgaben.
- Neu gestaltete Fehler-, Warnungen- und Richtliniennachrichten sollen dabei helfen, dass Sie den richtigen Kontext haben, zu verstehen, was das Problem ist und wie es gelöst werden kann. Microsoft hat viele Nachrichten entfernt, die angezeigt wurden, bevor der Benutzer die Chance hatten, die Aufgaben abzuschließen und das Problem zu adressieren, wie beispielsweise unvollständige Einzelaufzählungsnachrichten.
- Eine neue Seite zur Angabe, welche Felder von der Organisation vorgegebenen werden, welche Felder optional sind und welche Felder nicht aufgezeichnet werden sollen. Diese Seite wird helfen, die Anzahl von Feldern zu reduzieren, die der Benutzer festlegen muss.
- Ein neues Erscheinungsbild für Ausgabenberichte, damit die Berichte nicht mehr aussehen, als ob sie für Buchhaltungspersonen entworfen wurden.

Um die neue Erfahrung zu aktivieren, verwenden Sie den Arbeitsbereich **Funktionsverwaltung**, um die Funktion **Neue Darstellung der Ausgabenberichte** zu aktivieren. Wenn Sie diese Funktion aktivieren, werden die folgenden Aktivitäten ausgeführt:

- Der vorhandene Ausgabenenarbeitsbereich wird durch den neuen Arbeitsbereich ersetzt.
- Ein neues Menüelement für Ausgabenenfeldsichtbarkeit wird hinzugefügt.
- Keine vorhandenen Menüoptionen für Ausgabenberichte (die bestehende Seite) oder Ausgabenberichtfelder werden entfernt.
- Abläufe und alle Genehmigungen führen Sie weiterhin zur bestehenden Ausgabenberichtsseite.

## <a name="getting-started-video-for-new-users"></a>Erste Schritte-Video für neue Benutzer

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE2Y7gO]

Die [Ausgabenfunktion in Dynamics 365 for Finance and Operations](https://youtu.be/Ocy-MsTvEE0) Videodatei (oben angezeigt) ist in der [Finance and Operations-Wiedergabeliste](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) enthalten, die auf YouTube verfügbar ist.

## <a name="new-features"></a>Neue Features

| Neue Funktion | Beschreibung |
|---|----|
| Ausgabenenfeldsichtbarkeit | Auf einer neuen Einstellungsseite können Sie angeben, welche Felder für eine Organisation deaktiviert werden sollen, welche Felder erforderlich sein sollen und welche Felder nur empfehlenswert sind. |
| Pflichtfelder | Mit der neuen einfachen Konfiguration können Sie einige Pflichtfelder erstellen, ohne dass Sie den Richtlinienrahmen verwenden müssen. |
| Optionale Felder | Eine zweite Seite für optionale Felder wird hinzugefügt. Dadurch haben Mitarbeiter nicht das Gefühl, dass sie die Felder festlegen müssen, aber auf die Felder kann dennoch einfach zugegriffen werden. |
| Nicht angefügte Belege hinzufügen | Die Möglichkeit, nicht angehängte Belege einem Ausgabenbericht hinzuzufügen, ist nun im Arbeitsbereich und im Ausgabenbericht besser sichtbar. |
| Verbesserte Nachrichten | Es gibt eine bessere Sichtbarkeit in Ausgabenpositionen, die Warnungen oder Fehler enthalten. |
| Verringerung der Nachrichten in der Meldungsleiste| Die Anzahl der Infolog-Meldungen wurde verringert, und es wurde versucht, doppelte Nachrichten zu verhindern, die in zu vielen Fällen auftraten. |
| Gruppierte häufige Aktionen | Die Schnittstelle wurde mit dem Hinzufügen neuer Aktivitätsschaltfläche für die meisten allgemeinen Zeilen spezfisichen Aktivitäten, dem Hinzufügen einer neuen Ellipsen-Schaltfläche (...)für Kopfzeilen und weitere weniger häufige Aktivitäten bereinigt. |
| Neuer Arbeitsbereich, um die Sichtbarkeit zu erhöhen | Einen neuen Arbeitsbereich vereinheitlicht Funktionen und Links, damit der Benutzer zu unterschiedlichen Bereichen navigieren kann. |
| Bestehende Ausgaben und Belege während der Ausgabenerstellung hinzufügen | Wenn Sie Ausgabenberichte erstellen, können Sie alle oder ausgewählte Ausgaben und Belege hinzufügen. |
| Wechselkurrechner | Ein Wechselkursrechner wurde hinzugefügt, damit Sie den Wechselkurs für Ausgaben mit unterschiedlichen Wechselkurstransaktionen berechnen können. |
| Speichern und Hinzufügen neuer Ausgabenpositionen | Die Schaltflächen **Speichern** und **Neu** sind verfügbar, wenn neue Ausgaben eingegeben werden, damit Sie die Ausgabenpositionen schnell eingeben können. |
| Bessere Sichtbarkeit in die aufgeschlüsselten und geteilten Positionen | Aufgeschlüsselte und geteilte Positionen werden direkt der Ausgabenliste hinzugefügt, um die Sichtbarkeit zu erhöhen es Ihnen zu ermöglichen, einfach zu bestimmen, ob Richtlinienfehler oder andere Fehler vorhanden sind. |
| Belege während de Aufstellung anzeigen | Belege können während der Aufstellung angezeigt werden. |

Die erste Version fokussierte sich auf die Ausgabeneneintragsszenarien. Jedes Ausgabenberichtsprüfungs- oder Genehmigungsszenario nutzt weiterhin die bestehende Ausgabeneneintragsseite.

Die folgenden Funktionen sind auf der bestehenden Seite aber nicht auf der neuen Seite vorhanden. Diese Funktionen werden in den kommenden Aktualisierungen eingeführt:

- Genehmigungen
- Kreditorkontengenehmigungen und die Möglichkeit, die Buchhaltung zu bearbeiten
- Mehrere Eingabepunkte
- Integratin der Reiseanforderung
- Datenentität für Ausgabenenfeldsichtbarkeit
- Eintrag für Tagessatzausgaben
- Der Workflow auf Positionsebene.
- Zwischengenehmigersupport
- Erweiterte Aufschlüsselung
