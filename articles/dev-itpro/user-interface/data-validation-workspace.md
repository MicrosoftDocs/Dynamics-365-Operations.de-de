---
title: "Datenüberprüfungsarbeitsbereich"
description: "Mit dem Arbeitsbereich für die Prüfliste für Datenüberprüfung können Sie Datenprüfungsvorgänge in Unternehmen, Bereichen und bei Personen erfassen. Die Checkliste kann während einer neuen Implementierung, nach einer Aktualisierung oder nach einer Migration verwendet werden."
author: bking
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: DataValidationWorkspace
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.assetid: 
ms.search.region: Global
ms.author: bking
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: daded9d8ef48456cbd3f97a7bae5fa75885ce9d1
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="data-validation-workspace"></a>Datenüberprüfungsarbeitsbereich

[!include[banner](../includes/banner.md)]


Dieses Thema enthält eine Übersicht über den **Arbeitsbereich für die Prüfliste für Datenprüfung** und der zugeordneten Konfiguration.

## <a name="data-validation-checklist-workspace"></a>Arbeitsbereich für die Prüfliste für Datenüberprüfung

Mit dem **Arbeitsbereich für die Prüfliste für Datenüberprüfung** können Sie Datenprüfungsvorgänge in Unternehmen, Bereichen und bei Personen erfassen. Die Checkliste kann während einer neuen Implementierung, nach einer Aktualisierung oder nach einer Migration verwendet werden. Abhängig von Ihrer Ansicht auf den Arbeitsbereich **Prüfliste für Datenüberprüfung**, sehen Sie entweder alle Aufgaben und Status für eine Datenprüfungsprojekt oder nur die Aufgaben, die Ihnen zugewiesen sind.

Sie müssen ein Datenprüfungsprojekt am oberen Rand des Arbeitsbereichs auswählen. Alle Daten, die im Arbeitsbereich angezeigt werden, werden dann nach dem ausgewählten Datenprüfungsprojekt gefiltert.

### <a name="summary-tiles"></a>Zusammenfassungskacheln

Die **Zusammenfassung** Kacheln enthalten eine Übersicht über den Prozess, und helfen, den Datenüberprüfungsprozess zu überwachen. Sie können alle verbleibenden Aufgaben, abgeschlossene Aufgaben, aktuelle Aufgaben und nicht gestartete Aufgaben für den Prozess sehen. Diese Informationen sind für alle Unternehmen, die im ausgewählten Datenprüfungsprojekt enthalten sind.

### <a name="tasks-and-status-section"></a>Aufgaben- und Statusbereich

Im Abschnitt **Aufgaben und Status** wird der Status des Gesamtdatenprüfungsprojekts auf unterschiedliche Weise angezeigt: Status nach juristischer Person, nach Bereich und nach Aufgabenliste. Sie können den Filter auch auswählen, um den Status für ein bestimmtes Unternehmen anzuzeigen. Jede Statusregisterkarte bietet eine Aufschlüsselung nach Prozentsatz, der abgeschlossen wurde und nach Aufgaben, die noch verbleiben.

Die letzten Registerkarte ist für die detaillierte Aufgabenliste. Diese Liste zeigt die vollständige Aufgabenliste an.
Sie können die Aufgabenliste auf verschiedene Weise filtern. Klicken Sie auf **Bearbeiten einer Aufgabe**, um den Status einer Aufgabe zu ändern oder eine Aufgabe zuweisen. Klicken Sie auf **Anhänge**, um die Anhänge für eine Aufgabe anzuzeigen.

Der Aufgabenname ist ein Link zur Seite Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition oder einer anderen Webseite, auf der ein Benutzer die Arbeit abschließen muss. Sie können diesen Hyperlink festlegen, indem Sie das Feld **Menüelementname** verwenden, wenn Sie im Formular **Datenüberprüfungsprojekt konfigurieren** eine Aufgabe bearbeiten oder erstellen.

Sie können Dateien, Hinweise, Bilder und URLs zu einer Aufgabe zuordnen, indem Sie die Aktivität **Zuordnungen** verwenden. Sie können beispielsweise eine Berichtdatei anhängen, die für eine Aufgabe gedruckt wurde. Ein Symbol wird in der Spalte **Anlag** für die Aufgabe angezeigt, wenn eine Anlage vorhanden ist.

Die Option **Abgeschlossen von** wird automatisch mit dem Namen einer Arbeitskraft ausgefüllt, die die Aufgabe abgeschlossen hat, nachdem die Aufgabe abgeschlossenen ist. Wenn eine Aufgabe markiert wird, die als abgeschlossen markiert wird, wird das Feld **Datum abgeschlossen** automatisch mit dem aktuellen Datum und der Systemzeit aktualisiert.

### <a name="configure-data-validation-project-page"></a>Datenüberprüfungsprojektseite

Bevor Sie den Arbeitsbereich **Prüfliste für Datenprüfung** verwenden können, müssen Sie den Prozess konfigurieren, indem Sie die Seite **Datenprüfungsprojekt konfigurieren** verwenden. (Klicken Sie auf **Arbeitsbereiche** \> **Prüfungsliste für Datenprüfung** \> **Datenprüfungsprojekt konfigurieren**).

### <a name="task-areas"></a>Aufgabenbereiche

Sie verwenden Aufgabenbereiche, um Datenprüfungsaufgaben in logische Bereiche der Eigentümerschaft innerhalb der Organisation zu gruppieren. Beispielsweise können Kreditoren, Debitoren oder das Hauptbuch als Aufgabenbereiche verwendet werden.

Die Menüoption **Menüelementname** wird dem Aufgabenarbeitseinsatz zugeordnet und kann verwendet werden, um in direktem Bezug zur zugeordneten Seite über den Aufgabenlink im Arbeitsbereich zu wechseln. Beispielsweise kann eine Datenprüfungsaufgabe zur Ausführung des Berichts **Kreditorenkontenfälligkeit** mit der Seite **Kreditorenkontenfälligkeitsbericht** verknüpft werden.

