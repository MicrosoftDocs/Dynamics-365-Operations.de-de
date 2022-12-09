---
title: Finanzberichte generieren
description: Dieser Artikel enthält allgemeine Informationen zun Generieren von Finanzberichten.
author: jinniew
ms.date: 02/08/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.custom: 68843
ms.assetid: 271df6f4-12b7-4b3e-b2d7-36ea98ef1871
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 2f55fe1a23735d8631a5918fa49e08f74eee4d37
ms.sourcegitcommit: d27fef61593c6d1e9e26d5c9fad21411bc52fabc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/23/2022
ms.locfileid: "9802768"
---
# <a name="generate-financial-reports"></a>Finanzberichte generieren

[!include [banner](../includes/banner.md)]

Dieser Artikel enthält allgemeine Informationen zun Generieren von Finanzberichten.

Öffnen Sie zum Generieren eines Berichts die Berichtsdefinition, und wählen Sie anschließend in der Symbolleiste **Generieren**. Die Seite **Berichtswarteschlangenstatus** öffnet sich und gibt die Position Ihres Berichts in der Warteschlange an.

Während die Berichtsgenerierung läuft, können die folgenden Berichtswarteschlangestatus auf der Seite **Berichtswarteschlangenstatus** angezeigt werden.

| Status          | Bundesstaat | Description|
|-----------------|--------|--------------------|
| Einfügen in die Warteschlange        | Vorläufig |Die Berichtsdefinition wird validiert, bevor der Bericht in die Generierungswarteschlange gestellt wird.                    |
| In Warteschlange          | Vorläufig | Der Bericht wird in die Warteschlange für die Berichterstellung weitergeleitet und wartet auf die Verarbeitung.                      |
| Bearbeitung      | Vorläufig | Dieser Status folgt normalerweise dem Status **In Warteschlange** und geht normalerweise in den Status **Endgültig** über, wenn die Bearbeitung abgeschlossen ist.       |
| Nachbearbeitung | Vorläufig | Dieser Status folgt dem Status **Bearbeitung** und gibt an, dass alle Berichtsdaten erfasst wurden, aber dass abgeleitete Aktionen, wie Berechnung und Roll-up, ausgeführt werden.            |
| Wird abgebrochen...      | Vorläufig | Die Berichterstellung wird auf Wunsch des Benutzers abgebrochen. Dieser Status ergibt sich aus einem vom Benutzer angeforderten Abbruch für einen Bericht mit dem Status **In Warteschlange** oder **Bearbeitung**. Das System versucht, den Bericht in den Status **Storniert** zu versetzen, es sei denn, das System ist zu weit fortgeschritten und muss ihn in einem anderen Status finalisieren. |
| Storniert        | Endgültig | Die Verarbeitung des Berichts ist abgeschlossen, wurde jedoch aufgrund eines vom Benutzer angeforderten Stopps nicht abgeschlossen.            |
| Fertiggestellt       | Endgültig | Der Bericht kann verwendet werden.                      |
| Nicht bestanden          | Endgültig | Der Bericht wurde verarbeitet, ist jedoch fehlgeschlagen und sollte nicht verwendet werden. |

Standardmäßig wird der generierte Bericht in Web Viewer geöffnet. Für die Erstellung von Berichten sind die folgenden Optionen verfügbar:

- Einrichten eines Zeitplans, um einen Bericht oder eine Gruppe von Berichten automatisch zu generieren
- Prüfen auf fehlende Konten oder Daten in einem Bericht und Validieren der Richtigkeit eines Berichts

Wenn Sie einen Bericht generieren, werden die Optionen verwendet, die Sie auf den Registerkarten „Berichtsdefinition“ angegeben haben.

## <a name="generate-a-financial-report"></a>Finanzbericht generieren

Rufen Sie **Hauptbuch** \> **Abfragen und Berichte** \> **Finanzberichte**, um einen Finanzbericht mit zu generieren.

- Wählen Sie einen zu generierenden Bericht aus, und wählen Sie **Generieren** aus.
- Fügen Sie das Feld **Berichtsdatum** aus, und klicken Sie auf **OK**.

Nachdem der Bericht generiert wurde, ist der Bericht verfügbar zum Anzeigen im Abschnitt **Berichte** anzuzeigen.

Sie können den Bericht **anzeigen** oder **löschen**.

Öffnen Sie zum Generieren eines Berichts mithilfe des **Berichtsdesigners** die Berichtsdefinition, und wählen Sie anschließend die Schaltfläche **Generieren** in der Symbolleiste aus. Die Seite **Berichtswarteschlangenstatus** wird geöffnet und gibt die Position Ihres Berichts in der Warteschlange an. Standardmäßig wird der generierte Bericht in Web Viewer geöffnet.

## <a name="report-groups"></a>Berichtsgruppen

Berichtsgruppen sind eine effiziente Möglichkeit, mehrere Berichte gleichzeitig zu generieren. Angenommen Sie wissen, dass Ihre Benutzer zum Monatsende jeden Monat acht Berichte erstellen. Erstellen Sie eine Berichtsgruppe, und wählen Sie **Generieren** für die Berichtsgruppe aus. Die acht Berichte werden in einem Schritt generiert, und Sie müssen nicht für jeden der acht Berichte **Generieren** auswählen. Wenn die Berichte in der ausgewählten Berichtsgruppe generiert wurden, können Sie **Finanzberichte** (**Hauptbuch > Anfragen und Berichte > Finanzberichte**) aufrufen, um sich die einzelnen Berichte anzeigen zu lassen. Führen Sie folgende Schritte aus, um eine Berichtsgruppe einzurichten.

1. Wählen Sie im **Report Designer** **Berichtsgruppen** aus. 
2. Wählen Sie die vorhandenen Berichtsdefinitionen aus, die in Ihre Berichtsgruppe aufgenommen werden sollen. 
3. Wählen Sie aus jedem der Berichte, die in die Gruppe aufgenommen werden sollen, die Einstellungen zum Überschreiben von Unternehmen, Details und Datum aus.
   Wir empfehlen, für jeden Bericht die Optionen **Unternehmen**, **Periode**, **Jahr** und **Detailebene** einzustellen. 
4. Speichern Sie die Berichtsgruppe.

## <a name="schedule-report-generation"></a>Planen der Berichtsgenerierung
Viele Unternehmen verwenden einen Kernsatz von Berichten, die in Einklang mit ihren Geschäftsprozessen in geplanten Intervallen ausgeführt werden. Sie können festlegen, dass ein Bericht regelmäßig generiert wird, beispielsweise täglich, wöchentlich, monatlich oder jährlich. Sie können einen einzelnen Bericht oder eine Gruppe von Berichten, die mehrere Unternehmen umfasst, planen. Für jedes der Unternehmen, die z. B. in einer Berichtsbaumstruktur-Definition angegeben sind, müssen Anmeldeinformationen eingegeben werden. Wenn die Anmeldeinformationen nicht gültig sind, zeigt der Bericht nur die Informationen, für die Sie eine Zugriffsberechtigung haben, beispielsweise für das Unternehmen, bei dem Sie zu dem Zeitpunkt angemeldet sind. Die Ausgabeinformationen werden zuerst von der Berichtsgruppe und anschließend von den einzelnen Berichten gelesen.

Während Berichtszeitpläne erstellt und gespeichert werden, werden diese im Navigationsbereich unter **Berichtzeitpläne** angezeigt. Sie können Ordner zum Organisieren der Berichte erstellen. Wird ein einzelner Bericht in einem Berichtszeitplan nicht ausgeführt, hat dies keinen Einfluss auf die Ausführung aller anderen Berichte.

> [!IMPORTANT]
> Zum Erstellen, Ändern und Löschen von Berichtszeitplänen benötigen Sie die Rolle „Designer“ oder „Administrator“. Wenn ein Bericht ausgeführt wird, werden die Anmeldeinformationen des Benutzers, der den Zeitplan erstellt hat, verwendet, um den Bericht zu generieren.

### <a name="create-a-report-schedule"></a>Erstellen eines Berichtzeitplans

1. Wählen Sie im **Report Designer** im Menü **Datei** die Option **Neu** und dann **Berichtzeitplan** aus. Das Dialogfeld **Neuer Berichtzeitplan** wird geöffnet.
2. Wählen Sie unter **Einstellungen** einen individuellen Bericht oder eine Berichtsgruppe für den Zeitplan aus. Es sind nur Berichte oder Berichtsgruppen für das Unternehmen oder den Baustein verfügbar, bei dem Sie derzeit angemeldet sind.
3. Aktivieren Sie das Kontrollkästchen **Aktiv**, um den Berichtzeitplan zu aktivieren. Nur der Ersteller des Berichts oder ein Administrator kann einen Berichtszeitplan aktivieren oder deaktivieren.
4. Wählen Sie die Schaltfläche **Berechtigungen** aus, um Unternehmens-Anmeldeinformationen einzugeben. Standardmäßig werden Ihre Anmeldeinformationen für das Unternehmen verwendet, bei dem Sie angemeldet sind. Wenn andere Unternehmen eingeschlossen sind, wie beispielsweise in den Berichtsbaumstruktur-Definitionen, wählen Sie **Gesonderte Anmeldeinformationen verwenden** und geben dann die Anmeldeinformationen für alle anderen Unternehmen ein, die im Berichtzeitplan enthalten sind. Sie können **Windows-Authentifizierung** auswählen oder einen Benutzernamen und ein Kennwort für jedes Unternehmen eingeben. Aktivieren Sie das Kontrollkästchen **Anmeldeinformationen speichern**, um die Anmeldeinformationen für diese Unternehmen zu speichern, und wählen Sie **OK** aus, um das Dialogfeld zu schließen.
5. Wählen Sie unter **Häufigkeit** im Feld **Wiederholung starten** das Datum aus, an dem der Zeitplan zu starten ist. Standardmäßig wird das aktuelle Systemdatum des Clientcomputers ausgewählt.
6. Wählen Sie im Feld **Bericht ausführen am** den Zeitpunkt aus, an dem der Bericht ausgeführt werden soll. Wenn Sie eine Uhrzeit eingeben, die vor der aktuellen Systemzeit liegt, wird der Bericht am nächsten geplanten Datum ausgeführt.
7. Geben Sie im **Wiederholungsmuster**-Bereich an, wie oft der Bericht ausgeführt wird. Standardmäßig wird **Täglich** mit einem **Intervallwert (Tage)** von **1** ausgewählt. Andere Optionen sind **Wöchentlich**, **Monatlich** oder **Jährlich**.
8. Wählen Sie im Bereich **Wiederholungsbereich** aus, wann der Bericht nicht mehr generiert werden soll.

    - **Kein Enddatum** – Der Berichtzeitplan wird auf unbestimmte Zeit ausgeführt.
    - **Anzahl der Vorkommen festlegen** – Der Berichtzeitplan wird so oft ausgeführt wie angegeben und dann deaktiviert.
    - **Beenden zum** – Der Berichtzeitplan endet am angegebenen Datum.

9. Wählen Sie **Speichern** aus. Geben Sie im Dialogfeld **Speichern unter** einen eindeutigen Namen und eine Beschreibung für den Berichtzeitplan ein.

Zum Kopieren von Berichtszeitplänen müssen Sie die Rolle eines Designers oder Administrators haben. Auch wenn ein Administrator den Berichtszeitplan ändert, behält der Bericht die Anmeldeinformationen des Benutzers, der den Bericht erstellt hat.

### <a name="copy-a-report-schedule"></a>Kopieren eines Berichtzeitplans

1. Wählen Sie im Report Designer um Navigationsbereich **Berichtzeitpläne** aus und öffnen Sie den zu kopierenden Berichtszeitplan.
2. Wählen Sie im Menü **Datei** die Option **Speichern unter** aus, und geben Sie dann einen neuen Namen und eine Beschreibung für den Zeitplan im Dialogfeld **Speichern unter** ein. Wählen Sie **OK** aus, und der neue Zeitplan wird im Navigationsbereich angezeigt.
3. Ändern Sie im neuen Zeitplan die Felder und die Informationen nach Bedarf, und wählen Sie anschließend in der Symbolleiste **Speichern** oder **Speichern** im Menü **Datei** aus.

Um einen Berichtszeitplan zu löschen, müssen Sie der Besitzer des Berichtszeitplans oder Administrator sein.

### <a name="delete-a-report-schedule"></a>Löschen eines Berichtzeitplans

1. Wählen Sie im Report Designer **Berichtszeitpläne** im Navigationsbereich aus.
2. Wählen Sie den Berichtzeitplan aus, der gelöscht werden soll, und wählen Sie anschließend **Löschen** aus, oder drücken Sie die **Löschen**-Taste.
3. Wählen Sie im Dialogfeld zum Bestätigen des Löschens **Ja** aus, um den Berichtzeitplan dauerhaft zu löschen. Wenn Sie nicht über die Berechtigung verfügen, den Zeitplan zu löschen, wird eine Meldung angezeigt und der Bericht wird nicht gelöscht.

### <a name="credentials-and-report-schedules"></a>Anmeldeinformationen und Berichtszeitpläne

Wenn Sie keine Anmeldeinformationen eingeben, die für alle Unternehmen erforderlich sind, die in den Berichten enthalten sind, erhalten Sie eine Meldung mit etwa folgendem Inhalt: „Sie müssen Ihre Anmeldeinformationen für die Unternehmen eingeben, die im Berichtszeitplan enthalten sind. Klicken Sie auf die Schaltfläche **Berechtigungen**, um Ihre Anmeldeinformationen einzugeben.“

Beispiel: Ein Benutzer meldet sich mit Anmeldeinformationen und Kennwort am Unternehmen A an. Der Benutzer erstellt einen Zeitplan für einen Bericht, der eine Berichtsbaumstruktur-Definition verwendet, um Daten aus mehreren Unternehmen zu erfassen. Beim Speichern dieses Berichtszeitplans wird der Benutzer aufgefordert, die Anmeldeinformationen für die anderen Unternehmen einzugeben, die in der Berichtsbaumstruktur-Definition angegeben sind. Wenn Ihre Anmeldeinformationen ablaufen, werden die betroffenen Berichte im Berichtszeitplan nicht generiert, bis die Anmeldeinformationen aktualisiert wurden. Eine Meldung wird in der Berichtswarteschlange angezeigt, die angibt, dass die Berechtigungen aktualisiert werden müssen. Der Berichtszeitplan schlägt fehl, wenn eines der folgenden Szenarios auftritt (da sie Anmeldeinformationen erfordern):

- Ein neues Unternehmen wurde einer Berichtsstruktur für einen einzelnen Bericht hinzugefügt.
- Ein Bericht in einer Berichtsgruppe wurde geändert.
- Einer Berichtsgruppe wurde ein neuer Bericht für ein weiteres Unternehmen hinzugefügt.

Wählen Sie zum Fortfahren **Berechtigungen** im Dialogfeld **Berichtzeitplanung** aus und geben Sie dann die entsprechenden Anmeldeinformationen ein.

## <a name="missing-account-analysis-feature"></a>Analysefunktion für fehlende Konten
Sie können nach Finanzkonten und Dimensionen suchen, die möglicherweise in allen Zeilendefinitionen, Berichtsbaumstruktur-Definitionen und Berichtsdefinitionen in einer Bausteingruppe fehlen. Dies ist hilfreich, wenn Sie mehrere Konten oder Bausteine während eines kurzen Zeitraum erstellen oder aktualisieren und Sie sicherstellen möchten, dass alle neuen Informationen in den Berichten enthalten sind.

Fehlende Konten werden anhand der höchsten und niedrigsten Werte einer Zeilendefinition oder der Berichtstruktur-Definition bestimmt. Es wird dann eine Liste von Konten angezeigt, die sich nicht in der Zeilendefinition oder in der Berichtstruktur-Definition befinden, aber Teil der Finanzdaten sind. Wenn ein fehlendes Konto größer oder kleiner ist als die Werte in der Zeilendefinition, wird das Konto nicht in die Liste fehlender Konten aufgenommen.

> [!TIP]
> Zu Überprüfungszwecken sollte dieser Vorgang vor dem Generieren monatlicher Berichte und beim Erstellen neuer Bausteine durchgeführt werden.

Bei Berichten mit Wertebereichen ist es weniger wahrscheinlich, dass Konten fehlen. Verwenden Sie, wenn möglich, Bereiche im Baustein, um neue Konten bei deren Erstellung zu integrieren. Wenn eine Berichtsdefinition auf @ANY Unternehmen eingestellt ist, können Sie sich bei einem bestimmten Unternehmen anmelden und für dieses Unternehmen eine Analyse für fehlende Konten durchführen.

> [!NOTE]
> Wurde ein neues Unternehmen hinzugefügt, müssen Sie das neue Unternehmen den Berichtstrukturen in allen vorhandenen Berichten hinzufügen, sonst wird das Unternehmen nicht in die Analyse fehlender Konten einbezogen.

### <a name="run-missing-account-analysis"></a>Analyse für fehlende Konten ausführen

1. Wählen Sie im Report Designer **Tools** und anschließend **Analyse für fehlende Konten** aus.
2. Wählen Sie im Feld **Unternehmensfilter** ein Unternehmen aus, für das Ergebnisse gefiltert werden sollen, oder wählen Sie **Alle (kein Filter)** aus, um die Ergebnisse aller verfügbaren Unternehmen anzuzeigen.
3. Wählen Sie im Feld **Dimensionsfilter** eine Dimension aus, um die Ergebnisse zu filtern, oder wählen Sie **Alle (kein Filter)**, um alle Dimensionsinformationen für alle verfügbaren Dimensionen anzuzeigen.
4. Wählen Sie im Feld **Gruppieren nach** die geeignete Option zum Sortieren der Ergebnisse aus. Sie können die Ergebnisse nach dem betroffenen Baustein oder nach Dimensions- und Wertsätzen sortieren.
5. Überprüfen Sie die angezeigten Ergebnisse. Wenn Sie im oberen Bereich ein Element auswählen, werden im unteren Bereich zusätzliche Informationen zu der Ausnahme angezeigt. Dies umfasst zugehörige Dimensionen, Werte und Berichte.
6. Wählen Sie das zugeordnete Symbol im Listenbereich aus, oder klicken mit der rechten Maustaste auf das Element, und wählen Sie **Öffnen** aus, um das betreffende Element zu öffnen. Um mehrere Elemente auszuwählen, halten Sie während des Auswählens im unteren Bereich die **STRG**-Taste gedrückt.
7. Werden Werte, Bausteine oder Berichte zurückgegeben, die nicht in die Analyse einbezogen werden sollen, klicken Sie mit der rechten Maustaste auf den Artikel und wählen Sie **Ausschließen** aus, oder Sie aktivieren das Kontrollkästchen **Ausschließen** neben dem Artikel, um den Artikel aus der Liste zu entfernen. Ausgeschlossene Artikel sind nicht enthalten, wenn die Liste aktualisiert wird. Um mehrere Elemente auszuwählen, halten Sie während des Auswählens im unteren Bereich die **STRG**-Taste gedrückt. Wenn Sie alle Elemente inklusive aller Ergebnisse, die Sie zuvor aus der Analyse ausgeschlossen haben, anzeigen möchten, aktivieren Sie das Kontrollkästchen **Ausgeschlossene Bausteine und Werte anzeigen** und wählen Sie dann **Aktualisieren** aus.
8. Wählen Sie **Aktualisieren** aus, um Ausnahmen zu aktualisieren, die Sie adressiert haben. Wählen Sie **Ja** aus, um alle Ergebnisse zu aktualisieren, oder wählen Sie für eine teilweise Aktualisierung der betroffenen Elemente **Nein** aus.

    > [!NOTE]
    > Das Formular wird beim Öffnen automatisch aktualisiert, es sei denn, die Seite wurde in den letzten 15 Minuten bereits geöffnet.

9. Wählen Sie nach der Problembehebung **OK** aus, um das Dialogfeld zu schließen.

## <a name="keyboard-shortcuts-for-missing-account-analysis"></a>Tastenkombinationen für eine Analyse für fehlende Konten
Wenn Sie eine Analyse für fehlende Konten ausführen, sind die folgenden Tastenkombinationen verfügbar.

| Aktion                           | Drücken Sie folgende Taste: . |
|--------------------------------------|----------------------------|
| Filtern nach Unternehmen                    | ALT+C                      |
| Nach Dimension filtern                  | ALT+D                      |
| Das Feld Gruppieren nach auswählen            | ALT+G                      |
| Ausgeschlossene Bausteine und Werte anzeigen      | ALT+S                      |
| Ergebnisse aktualisieren                      | ALT+R                      |
| Den ausgewählten Baustein ausschließen  | ALT+X                      |
| Die ausgewählte Zeilendefinition ausschließen  | STRG+B                     |
| Den ausgewählten Dimensionswert ausschließen | STRG+D                     |
| Die ausgewählte Berichtsdefinition öffnen  | STRG+R                     |
| Die ausgewählte Zeilendefinition öffnen     | STRG+O                     |


## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Finanzberichterstellung](financial-reporting-intro.md)

[Schnittstelle „Berichts-Designer“](report-designer-interface.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
