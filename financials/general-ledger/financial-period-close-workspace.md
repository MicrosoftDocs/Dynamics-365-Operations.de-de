---
title: Finanzperiodenabschluss-Arbeitsbereich
description: "Dieser Artikel enthält eine Übersicht über den Finanzperiodenabschlussarbeitsbereiche und der zugeordneten Konfiguration."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerPeriodCloseProjectWorkspace
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13791
ms.assetid: 6ee51758-639b-448e-9cb2-56cf1d804273
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 114dee90b0fe525f0b3efabbf651d2804a22dd7d
ms.openlocfilehash: ba0d709d123f56edb2a5287376c06c1f41181b1c
ms.lasthandoff: 03/31/2017


---

# <a name="financial-period-close-workspace"></a>Finanzperiodenabschluss-Arbeitsbereich

Dieser Artikel enthält eine Übersicht über den Finanzperiodenabschlussarbeitsbereiche und der zugeordneten Konfiguration.

Finanzperiodenabschluss-Arbeitsbereich

** Der Finanzperiodenschließen ** Arbeitsbereich können Sie Ihre Finanzschließvorgänge zu Unternehmen, Bereichen und Personen erfassen. Abhängig von Ihrer Ansicht des Finanzperiodenschließen ** ** Arbeitsbereichs, finden Sie entweder von alle Aufgaben und der Status für eine abschließenden Planung oder momentan durch die Aufgaben, die Ihnen zugewiesen sind. 

Sie müssen ein Abschlusskonto Zeitplan am oberen Rand des Arbeitsbereichs zunächst aktivieren. Alle Daten, die im - Arbeitsbereich angezeigt wird, werden dann nach den ausgewählten Abschlusszeitplan gefiltert.

### <a name="summary-tiles"></a>Zusammenfassungskacheln

Die Kacheln **Zusammenfassung** geben eine Übersicht über den Prozess und Anzeigen helfen Ihnen, den Abschlussvorgang im Soll zu halten. Sie können die, Aufgaben, überfällige Aufgaben für verbleibende heute, sind Aufgaben finden, die, fälliger heutiger Tag sind, jedoch wurden aufgrund der Abhängigkeiten und aller verbleibenden Aufgaben für den Prozess gesperrt. Diese Informationen sind für alle Unternehmen, die im ausgewählten Abschlusszeitplan enthalten sind.

### <a name="tasks-and-status-section"></a>Aufgaben- und Statusbereich

Im ** Aufgaben und Status ** Abschnitt wird der Status des Gesamtabschlusszeitplans auf verschiedene Arten aufgeteilt: Status nach Unternehmen, Status nach Bereich und die Status nach Personen, zuständig ist. Sie können den Status für alle Aufgaben im abschließenden Zeitplan, momentan Aufgaben, die heutiger fälliger Tag ist, oder Aufgaben angezeigt, die basierend sind, indem den Filter oben der Kartenliste ändern. Sie können den Unternehmensfilter auch auswählen, um den Status für ein bestimmtes Unternehmen anzuzeigen. Jede Statusregisterkarte gibt Aufschlüsselung dem Prozentsatz, der abgeschlossen wurde und die Aufgaben, die noch verbleiben. Klicken Sie die Karte oder auf die Details ** ** Aktivität, die detaillierte Aufgabenliste durch die ausgewählte Karte zu filtern. 

Die letzten Registerkarte ist für die detaillierte Aufgabenliste. Diese Liste wird die vollständige Aufgabenliste angezeigt und kann so gefiltert werden, dass sie nur den Aufgaben werden, denen Sie interessiert sind. Auf der Aufgabenliste auf verschiedene Weise filtern. Beispielsweise können Sie durch Aufgabenfälligkeitsdatum, verbundenen Unternehmen und zugeordneten Bereich gefiltert werden. Sie können auch auswählen, ob abgeschlossene Aufgaben in der Aufgabenliste an bzw. blenden. 

Zwei Indikatoren werden für Aufgaben verwendet:

-   Ein Ausrufezeichensymbol gibt an, dass die Aufgabe überfällig ist. Bei Aufgaben, die basierend sind, ist das Fälligkeitsdatum auch rot hervorgehoben.
-   Ein Vorhängeschlosssymbol gibt an, dass die Aufgabe von anderen Aufgaben abhängig ist, die noch nicht abgeschlossen sind. Eine Aufgabe, die durch Abhängigkeiten gesperrt wird, kann nicht markiert werden, z abgeschlossen. Zudem können Abhängigkeiten für eine Aufgabe festgelegt, indem Sie die Abhängigkeit ** ** festgelegte Aktivität verwenden.

Der Aufgabenname ist ein Link zum Microsoft Dynamics 365 für andere Arbeitsgangsseite oder Webseite, gemäß der ein Benutzer eingeben muss, die Arbeit abzuschließen. Sie können diesen Link können festlegen, indem Sie das verwenden ** Aufgabenlink ** Feld, wenn eine Aufgabe bearbeiten oder erstellen. 

Sie können Dateien, Hinweise, Bilder und URLs zu einer Aufgabe zuordnen, indem Sie die Zuordnungen ** ** Aktivität verwenden. So können Sie beispielsweise angeben Erfassungsnummern, die als Teil einer Aufgabe, Hinzufügen von Kommentaren zu zu einer bestimmten Aufgabe verwendet werden, oder legen eine Berichtsdatei, die für eine Aufgabe gedruckt wurde. Ein Symbol wird in der Anlage ** ** Spalte für die Aufgabe, wenn eine Anlage vorhanden ist. 

** Die Aufgabe abgeschlossen ** Option muss manuell aktiviert werden, nachdem die Aufgabe abgeschlossen ist. Wenn eine Aufgabe markiert wird, die als abgeschlossen, das abgeschlossen wird ** Datum ** Feld automatisch mit dem aktuellen Datum und der Systemzeit aktualisiert. Abhängigkeitsindikatoren werden ebenfalls bei Bedarf aktualisiert.

## <a name="all-financial-period-close-tasks-list-page"></a>Listenseite für alle Aufgaben für den Finanzperiodenabschluss
Sie können alle Aufgaben des Nahen laufende und der vorherigen Periode ** alle von der Finanzperiodenschließenaufgaben ** Listenseite angezeigt. Diese Listenseite eignet zu historischen Analyse Ihres Abschlussprozess ggf. verwendet, da sie die Informationen zum geplanten Fälligkeitsdatum, den tatsächlichen Abschlussdatum und die Person beinhaltet, der die Aufgabe abgeschlossen hat. Nun können Sie die Informationen auf dieser Listenseite in Microsoft Excel zum Melden und das Überwachen der Zwecke einfacher exportieren.

## <a name="financial-period-close-configuration-page"></a>Seite der Finanzperiodenabschluss-Konfiguration
Bevor Sie den Finanzperiodenschließen ** ** Arbeitsbereich verwenden können, muss der Prozess in Microsoft Dynamics 365 für Arbeitsgänge konfigurieren, indem Sie die Finanzperiodenschließenkonfiguration ** ** Seite. (Auf ** Hauptbuch ** &gt; ** Periodenabschluss ** &gt; ** Finanzperiodenschließenkonfiguration **.)

### <a name="resources"></a>Ressourcen

** ** Ressourcen auf der Registerkarte definieren Sie die Person an, die in die Schließvorgänge beteiligt sind. Alle Mitarbeiter, das für eine abschließenden Aufgabe zuständig ist, muss zunächst hier zugeordnet werden. Sie müssen der Ansicht des Mitarbeiters des Arbeitsbereichs auch angeben. Die folgenden Optionen sind verfügbar:

-   **Nur zugewiesene Aufgaben** - Der Benutzer sieht nur die Aufgaben, die ihm zugewiesen werden.
-   **Alle Aufgaben und Status** - Der Benutzer sieht alle Abschlussaufgaben und den Status des Gesamtprozesses.

Benutzer, die nur dazu berechtigt sind, ihre zugewiesenen Aufgaben anzuzeigen, können der Aufgabenliste keine Aufgaben hinzufügen, Aufgaben bearbeiten oder Aufgaben aus der Aufgabenliste entfernen.

### <a name="task-areas"></a>Aufgabenbereiche

Sie verwenden Aufgabenbereiche, um die Abschlussaufgaben in logische Bereiche der Eigentümerschaft innerhalb der Organisation zu gruppieren. Beispielsweise können Kreditoren, Debitoren oder das Hauptbuch als Aufgabenbereiche verwendet werden.

### <a name="calendars"></a>Kalender

Erstellen und bearbeiten Sie finanziellkalender Verbindung unter Verwendung der Kalenderregisterkarte.  Dies ist, in dem Sie die für Schließvorgänge Arbeitstage definieren, und ist für die Planung von Abschlusskontosalden Aufgaben verwendet werden.  Hier können Sie einen neuen Kalender, und geben Sie den für die Aufgabenplanung Arbeitstagen verwendet werden.  Es empfiehlt sich, ein Kalender für lange Zeitspanne Zeitpunkt, wie ein Jahr oder Mehrfachverbindungsstellenjahre erstellen, da diese nach Erstellung bearbeitet werden kann.  Nachdem Sie die Kalender erstellt haben, klicken Sie auf die bearbeitensschaltfläche, um den Kalender für bestimmte Tage, wie etwa Feiertage zu aktualisieren.  Schließen von Aufgaben werden an den Tagen geplant, in der Steuerwert festgelegt, um sie zu öffnen.  Wenn nicht die Abschlussaufgaben Planung an einem bestimmten Tag sind, sollte dieses den Tag Steuerwert haben, der Status der festgelegt wird.

### <a name="templates"></a>Vorlagen

Sie verwenden Sie eine finanziellVorlage, um alle Aufgaben definieren, die Teil eines Abschlussprozess ggf. sind. Eine Verbindung ist Aufgabe regelmäßig Arbeitseinsatz einer Person, der zugewiesen wird, die als Teil jedes Abschlussprozess ggf. abzuschließen. In muss der Vorlage ein relatives Fälligkeitsdatum für jede Aufgabe in definiert sind. Das Fälligkeitsdatum wird die relative Anzahl von Tagen vor oder nach dem Enddatum der definierten Periode, dass die Aufgabe jede Periode fällig ist. Eine für Zeit wird auch an jede Aufgabe zugeordnet. Die für Zeit festgelegt, indem den Kontext der Zeitzone verwendet und ist der Zeitzone für jeden Benutzer festgelegt werden. 

Sie können eine Aufgabe in der Vorlage zuweisen mindestens einem Unternehmen, in denen diese Aufgabe gilt. Wenn eine andere Person zugewiesen wird, um diesen Arbeitseinsatz in jedem Unternehmen ausführen, stellen Sie möglicherweise fest hilfreich, mehrere Aufgaben für den gleichen Arbeitseinsatz zu erstellen. Erstellen Sie eine Aufgabe für jedes Unternehmen. 

** Aufgabenlink ** Die Menüoption wird mit dem Aufgabenarbeitseinsatz zugeordnet und kann verwendet werden, um in direktem Bezug zur zugeordneten Seite über Aufgabenlink im - Arbeitsbereich zu wechseln. Beispielsweise kann eine abschließenden Aufgabe, den Währungsaufwertungsprozess für Kreditoren ausführen der zugeordneten ** Neubewertung der Fremdwährung ** Seite in Microsoft Dynamics 365 für Arbeitsgänge verknüpft werden. Sie können auch eine externe URL verknüpfen. 

> [! Tipp] wenn Sie ein bestimmtes Management Reporter-Bericht zu einer Finanzperiodenschließenaufgabe verknüpfen möchten, können Sie die Berichts-URL verwenden. Um die Berichts-URL zuzugreifen, öffnen Sie den Bericht im Berichts-Designer, und klicken Sie dann ** Datei ** &gt; ** auf Ansichtsbericht ** den Bericht in einem Webbrowser öffnen. Sie können die URL dann in die Adressleiste des Browsers kopieren und in das Feld **Aufgabenlink**-**URL** einfügen. 

Sie können Aufgabenabhängigkeiten in der Vorlage definieren. Wenn eine Aufgabe, die von einem oder mehrere Aufgaben abhängig ist eingerichtet wurde, kann diese Aufgabe nicht markiert werden, z abgeschlossen, bis alle Abhängigkeiten abgeschlossen wurden. 

Sie können mehrere finanziellVorlagen Sie erstellen. Sie können anschließend die verschiedenen Vorlagen verwenden, um die Schließvorgänge für verschiedene Periodentypen zu erfassen, z oder Ende des Monats mit unterschiedlichen Geschäftsjahresenddaten oder Unternehmen, zu verfolgen, die verschiedene Schließvorgänge verwenden. Nachdem eine Vorlage erstellt wurde, können Sie sie in eine neue Vorlage kopieren und erforderliche Änderungen vornehmen. Sie können nur eine Vorlage in einem Zeitplan in zuordnen.

### <a name="closing-schedules"></a>Abschlusspläne

Mithilfe eines bei Planung, um eine finanziellVorlage Sie auf eine bestimmte Geschäftsperioden zuzuweisen, die abgeschlossen werden muss. Die Aufgaben aus der Vorlage werden dann automatisch für den angegebenen Zeitraum generiert, und der neue Abschlusszeitplan wird mit dem zum Bereich hinzugefügt. Wenn Sie einen neuen Abschlusszeitplan erstellen, wird das ** Periodenenddatum ** Feld verwendet, um das Fälligkeitsdatum für tatsächliche die Abschlussaufgaben, basierend relativen das Fälligkeitsdatum zu bestimmen, das in der finanziellVorlage Nahen zugewiesen wird. 

Weisen Sie den Kalender an, der für den Plan die Abschlusskontosalden, um den in der Aufgabenplanung geeignet ist zu Arbeitstagen verwendet werden, um anzugeben. Wenn Sie keinen bestimmten Kalender festlegen, verwendet das Aufgabenfälligkeitsdatum alle Wochentage ein. 

Sie müssen die Unternehmen auch festlegen, die dem bei Planung zugeordnet werden. Bei mehreren Unternehmen Vorlagenaufgaben zugewiesen sind, sind separate Aufgaben für jedes Unternehmen erstellt, das im abschließenden Zeitplan ist und der Vorlagenaufgabe. 

Nachdem ein Abschlusskonto Zeitplan abgeschlossen ist, wählen Sie die Option für ** geschlossen ** sie aus. Die Aufgabenhistorie noch von der Finanzperiodenschließenaufgaben ** alle ** Listenseite verfügbar, jedoch in der Auszugserfassung Zeitplan wird aus dem Arbeitsbereich entfernt. Nachdem ein Abschlusskonto Planung als markiert wurde geschlossen ** **, sind Sie dann nicht mehr in der Lage, Aufgaben diese zur hinzuzufügen, bearbeiten Aufgaben oder entfernen Aufgaben in Verbindung.


