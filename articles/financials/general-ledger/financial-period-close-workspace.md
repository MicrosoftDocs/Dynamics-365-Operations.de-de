---
title: Finanzperiodenabschluss-Arbeitsbereich
description: Dieser Artikel enthält eine Übersicht über den Finanzperiodenabschlussarbeitsbereiche und der zugeordneten Konfiguration.
author: ShylaThompson
manager: AnnBe
ms.date: 11/29/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerPeriodCloseProjectWorkspace
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 13791
ms.assetid: 6ee51758-639b-448e-9cb2-56cf1d804273
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e9c3c7f00d0a0e4379547edc5199f4a9a6727f3c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1548576"
---
# <a name="financial-period-close-workspace"></a>Finanzperiodenabschluss-Arbeitsbereich

[!include [banner](../includes/banner.md)]

Dieser Artikel enthält eine Übersicht über den Finanzperiodenabschlussarbeitsbereiche und der zugeordneten Konfiguration.

Finanzperiodenabschluss-Arbeitsbereich

Mit dem Arbeitsbereich **Abschluss Finanzperiode** können Sie Ihre Finanzabschlussprozessein Unternehmen, Bereichen und Personen erfassen. Abhängig von Ihrer Ansicht auf den Arbeitsbereich **Abschluss Finanzperiode** sehen Sie entweder alle Aufgaben und Status für eine Abschlussplanung oder nur die Aufgaben, die Ihnen zugewiesen sind. 

Sie müssen einen Abschlusszeitplan am oberen Rand des Arbeitsbereichs auswählen. Alle Daten, die im Arbeitsbereich angezeigt werden, werden dann nach dem ausgewählten Abschlusszeitplan gefiltert.

### <a name="summary-tiles"></a>Zusammenfassungskacheln

Die **Zusammenfassung** Kacheln geben eine Übersicht über den Prozess und der Indikator hilft, dass Sie den Schließvorgang verfolgen können. Sie können die Aufgaben sehen, die überfällig sind, die  für verbleibenden und finden die Aufgaben, die am heutigen Tag fällig sind, jedoch aufgrund der Abhängigkeiten gesperrt wurden und alle verbleibenden Aufgaben für den Prozess. Diese Informationen sind für alle Unternehmen, die im ausgewählten Abschlusszeitplan enthalten sind.

### <a name="tasks-and-status-section"></a>Aufgaben- und Statusbereich

Im Bereich **Aufgaben und Statu** wird der Status des Gesamtabschlusszeitplans auf verschiedene Arten aufgeteilt: Status nach Unternehmen, Status nach Bereich und Status nach Personen, die zuständig ist. Sie können den Status für alle Aufgaben im abschließenden Zeitplan ansehen, nur die momentanen Aufgaben oder die Aufgaben die überfällig sind, indem Sie den Filter oben an der Kartenliste ändern. Sie können den Unternehmensfilter auch auswählen, um den Status für ein bestimmtes Unternehmen anzuzeigen. Jede Statusregisterkarte gibt Aufschlüsselung nach Prozentsatz, der abgeschlossen wurde und nach Aufgaben, die noch verbleiben. Klicken Sie auf die Karte oder auf die Aktivität **Details ansehen**, um die detaillierte Aufgabenliste durch die ausgewählte Karte zu filtern. 

Die letzten Registerkarte ist für die detaillierte Aufgabenliste. Diese Liste zeigt die vollständige Aufgabenliste und kann so gefiltert werden, dass sie nur die Aufgaben anzeigt, die Sie interessieren. Sie können die Aufgabenliste auf verschiedene Weise filtern. Beispielsweise können Sie nach Aufgabenfälligkeitsdatum, verbundenen Unternehmen und zugeordnete Bereiche filtern. Sie können auch auswählen, ob abgeschlossene Aufgaben in der Aufgabenliste ein- oder ausgeblendet werden sollen. 

Zwei Indikatoren werden für Aufgaben verwendet:

-   Ein Ausrufezeichensymbol gibt an, dass die Aufgabe überfällig ist. Bei Aufgaben, die überfällig sind, ist das Fälligkeitsdatum auch rot hervorgehoben.
-   Ein Vorhängeschlosssymbol gibt an, dass die Aufgabe von anderen Aufgaben abhängig ist, die noch nicht abgeschlossen sind. Eine Aufgabe, die durch Abhängigkeiten gesperrt wird, kann nicht als abgeschlossen markiert werden. Zudem können Abhängigkeiten für eine Aufgabe festgelegt werden, indem Sie die Aktivität **Abhängigkeit  festlegen** auswählen.

Der Aufgabenname ist ein Link zur Seite Microsoft Dynamics 365 for Operations oder einer anderen Webseite, auf der ein Benutzer die Arbeit abschließen muss. Sie können diesen Link festlegen, indem Sie das Feld **Aufgabenlink** verwenden, wenn Sie eine Aufgabe bearbeiten oder erstellen. 

Sie können Dateien, Hinweise, Bilder und URLs zu einer Aufgabe zuordnen, indem Sie die Aktivität **Zuordnungen** verwenden. So können Sie beispielsweise die Erfassungsnummern angeben, die als Teil einer Aufgabe verwendet werden, Kommentare zu einer bestimmten Aufgabe hinzufügen oder eine Berichtsdatei anhängen, die für eine Aufgabe gedruckt wurde. Ein Symbol wird in der Spalte **Anlag** für die Aufgabe angezeigt, wenn eine Anlage vorhanden ist. 

Die Option **Aufgabe abgeschlossen** muss manuell aktiviert werden, nachdem die Aufgabe abgeschlossen ist. Wenn eine Aufgabe markiert wird, die als abgeschlossen markiert wird, wird das Feld **Datum abgeschlossen** automatisch mit dem aktuellen Datum und der Systemzeit aktualisiert. Abhängigkeitsindikatoren werden ebenfalls bei Bedarf aktualisiert.

## <a name="all-financial-period-close-tasks-list-page"></a>Listenseite für alle Aufgaben für den Finanzperiodenabschluss
Sie können alle Aufgaben der laufenden und der vorherigen Periode auf der Seite **Alle Aufgaben der Finanzperiode schließe**, anzeigen. Diese Listenseite eignet zur historischen Analyse Ihres Abschlussprozess, da sie die Informationen zum geplanten Fälligkeitsdatum, dem tatsächlichen Abschlussdatum und die Person beinhaltet, die die Aufgabe abgeschlossen hat. Nun können Sie die Informationen auf dieser Listenseite zum Melden und Überwachen der Zwecke einfach nach Microsoft Excel exportieren.

## <a name="financial-period-close-configuration-page"></a>Seite der Finanzperiodenabschluss-Konfiguration
Bevor Sie den Arbeitsbereich **Finanzperiodenabschluss** verwenden können, müssen Sie den Prozess in Microsoft Dynamics 365 for Finance and Operations mithilfe der Seite **Finanzperiodenabschlusskonfiguration** konfigurieren. (Klicken Sie auf **Hauptbuch** &gt; **Periode schließen** &gt; **Finanzperiodenkonfiguration abschließe**.)

### <a name="resources"></a>Ressourcen

In der Registerkarte **Ressource** definieren Sie die Person, die am Abschlussprozess beteiligt sind. Alle Mitarbeiter, die für eine abschließenden Aufgabe zuständig sind, müssen zunächst hier zugeordnet werden. Sie müssen auch die  Ansicht des Mitarbeiters des Arbeitsbereichs definieren. Die folgenden Optionen sind verfügbar:

-   **Nur zugewiesene Aufgaben** - Der Benutzer sieht nur die Aufgaben, die ihm zugewiesen werden.
-   **Alle Aufgaben und Status** - Der Benutzer sieht alle Abschlussaufgaben und den Status des Gesamtprozesses.

Benutzer, die nur dazu berechtigt sind, ihre zugewiesenen Aufgaben anzuzeigen, können der Aufgabenliste keine Aufgaben hinzufügen, Aufgaben bearbeiten oder Aufgaben aus der Aufgabenliste entfernen.

### <a name="task-areas"></a>Aufgabenbereiche

Sie verwenden Aufgabenbereiche, um die Abschlussaufgaben in logische Bereiche der Eigentümerschaft innerhalb der Organisation zu gruppieren. Beispielsweise können Kreditoren, Debitoren oder das Hauptbuch als Aufgabenbereiche verwendet werden.

### <a name="calendars"></a>Kalender

Sie erstellen und bearbeiten Abschlusskalender mithilfe der Registerkarte Kalender. Auf dieser Registerkarte definieren Sie die Arbeitstage für Abschlussprozesse und Sie können außerdem die Abschlussaufgaben planen.  Hier können Sie einen neuen Kalender erstellen und die Arbeitstage angeben, die für die Aufgabenplanung verwendet werden.  Es empfiehlt sich, ein Kalender für eine lange Zeitspanne wie ein Jahr oder mehrere Jahre zu erstellen, da sie nach der Erstellung bearbeitet werden können.  Nachdem Sie die Kalender erstellt haben, klicken Sie auf die Schaltfläche "Bearbeiten", um den Kalender für bestimmte Tage, wie etwa Feiertage, zu aktualisieren.  Schließen von Aufgaben werden an den Tagen geplant, wenn der Steuerwert auf "Offen" festgelegt ist.  Wenn Abschlussaufgaben nicht an einem bestimmten Tag geplant werden sollen, sollte der Tage den Kontrollwert "Gesperrt" aufweisen.

### <a name="templates"></a>Vorlagen

Sie verwenden Sie eine Vorlage für den Finanzabschluss, um Aufgaben zu definieren, die Teil des Abschlussprozesses sind. Eine Abschlussaufgabe ist ein regelmäßiger Arbeitseinsatz, der einer Person zugewiesen wird als Teil des Abschlussprozesses. In der Vorlage müssen Sie ein relatives Fälligkeitsdatum für jede Abschlussaufgabe definieren. Das Fälligkeitsdatum ist die relative Anzahl von Tagen vor oder nach dem Enddatum der definierten Periode, in der die Aufgabe fällig ist. Eine Fälligkeitszeit wird auch an jede Aufgabe zugeordnet. Die Fälligkeitszeit wird festgelegt, indem den Kontext der Zeitzone verwendet und in die Zeitzone für jeden Benutzer umgewandelt wird. 

Sie können eine Aufgabe in der Vorlage einem oder mehreren Unternehmen, in denen diese Aufgabe gilt. Wenn eine andere Person zugewiesen wird, um diesen Arbeitseinsatz in jedem Unternehmen ausführen, finden Sie es möglicherweise hilfreich, mehrere Aufgaben für den gleichen Arbeitseinsatz zu erstellen. Erstellen Sie eine Aufgabe für jedes Unternehmen. 

Die Menüoptiib **Aufgabenlink** wird dem Aufgabenarbeitseinsatz zugeordnet und kann verwendet werden, um in direktem Bezug zur zugeordneten Seite über den Aufgabenlink im Arbeitsbereich zu wechseln. Beispielsweise kann eine Abschlussaufgabe, die den Währungsbewertungsprozess für Kreditorenkonten ausführen soll, mit der zugeordneten Seite **Neubewertung der Fremdwährung** in Microsoft Dynamics 365 for Finance and Operations verknüpft werden. Sie können auch eine externe URL verknüpfen. 

> [!TIP]
> Wenn Sie einen bestimmten Management Reporter-Bericht mit einer Finanzperiodenabschlussaufgabe verknüpfen möchten, können Sie die Berichts-URL verwenden. Um auf die Berichts-URL zuzugreifen, öffnen Sie den Bericht im Berichts-Designer, und klicken Sie auf  **Datei** &gt; **Bericht anzeigen** , um den Bericht in einem Webbrowser zu öffnen. Sie können die URL dann in die Adressleiste des Browsers kopieren und in das Feld **Aufgabenlink**-**URL** einfügen. 

Sie können Aufgabenabhängigkeiten in der Vorlage definieren. Wenn festgelegt wurde, dass eine Aufgabe von einem oder mehreren Aufgaben abhängig ist, kann diese Aufgabe nicht als abgeschlossen markiert werden, bis alle Abhängigkeiten abgeschlossen wurden. 

Zudem besteht die Möglichkeit zum Erstellen mehrerer Belegvorlagen. Sie können anschließend die verschiedenen Vorlagen verwenden, um die Schließvorgänge für verschiedene Periodentypen zu erfassen, wie Ende des Monats oder Ende Jahr oder um verschiedene Unternehmen nachzuverfolgen, die unterschiedliche Abschlussprozesse verwenden. Nachdem eine Vorlage erstellt wurde, können Sie sie in eine neue Vorlage kopieren und erforderliche Änderungen vornehmen. Sie können nur eine Vorlage in einem Abschlusszeitplan zuweisen.

### <a name="closing-schedules"></a>Abschlusspläne

Sie nutzen einen Abschlussplan, um eine Finanzabschlussvorlage einer bestimmten Geschäftsperiode zuzuweisen, die abgeschlossen werden muss. Die Aufgaben aus der Vorlage werden dann automatisch für den angegebenen Zeitraum generiert, und der neue Abschlusszeitplan wird dem Bereich hinzugefügt. Wenn Sie einen neuen Abschlusszeitplan erstellen, wird das Feld **Periodenenddatum** verwendet, um das Fälligkeitsdatum für tatsächliche Abschlussaufgaben, basierend auf dem relativen Fälligkeitsdatum zu bestimmen, das in der Finanzabschlussvorlage zugewiesen wurde. 

Weisen Sie den Kalender für den Abschlusszeitplan zu, um die Arbeitstage anzugeben, die bei der Aufgabenplanung verwendet werden. Wenn Sie keinen bestimmten Kalender festlegen, nutzt die Aufgabe alle Wochentage. 

Sie müssen die Unternehmen auch festlegen, die der Planung zugeordnet werden. Wenn Vorlagen mehreren Unternehmen zugewiesen sind, werden separate Aufgaben für jedes Unternehmen erstellt, das im abschließenden Zeitplan ist und der Vorlagenaufgabe zugewiesen ist. 

Nachdem ein Abschlusskonto-Zeitplan abgeschlossen ist, wählen Sie die Option für **abgeschlossen**. Der Aufgabenverlauf ist auf der Listenseite **Alle Finanzperioden abschließen**  verfügbarm aber der Abschlusszeitplan wird vom Arbeitsbereich entfernt. Nachdem ein Abschlusszeitplan als  **Geschlossen** markiert wurde, sind Sie nicht mehr in der Lage, Aufgaben hinzuzufügen, zu bearbeiten oder zu entfernen.



