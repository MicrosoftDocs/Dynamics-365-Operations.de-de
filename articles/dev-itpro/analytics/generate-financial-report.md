---
title: Finanzberichte generieren
description: "Dieses Thema enthält allgemeine Informationen zun Generieren von Finanzberichten."
author: aprilolson
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 68843
ms.assetid: 271df6f4-12b7-4b3e-b2d7-36ea98ef1871
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: HT
ms.sourcegitcommit: 821d8927211d7ac3e479848c7e7bef9f650d4340
ms.openlocfilehash: b1dea07589b7fe953ec47b204441d044c19b5020
ms.contentlocale: de-de
ms.lasthandoff: 08/13/2018

---

# <a name="generate-financial-reports"></a>Finanzberichte generieren

[!include [banner](../includes/banner.md)]

Dieses Thema enthält allgemeine Informationen zun Generieren von Finanzberichten.

Um einen Bericht zu generieren, öffnen Sie die Berichtsdefinition und klicken anschließend auf die Schaltfläche Generieren in der Symbolleiste. Das Fenster Berichtswarteschlangenstatus wird geöffnet und gibt den Ort des Berichts in der Warteschlange an. Standardmäßig wird der generierte Bericht in Web Viewer geöffnet.

> [!NOTE]
> Sie können Berichte nur für Ordner und Orte generieren, auf die Sie zugreifen dürfen.

Für die Erstellung von Berichten sind die folgenden Optionen verfügbar:

- Einrichten eines Zeitplans, um einen Bericht oder eine Gruppe von Berichten automatisch zu generieren
- Prüfen auf fehlende Konten oder Daten in einem Bericht und Validieren der Richtigkeit eines Berichts

Wenn Sie einen Bericht generieren, werden die Optionen verwendet, die Sie auf den Registerkarten Berichtsdefinition angegeben haben. Über die Registerkarte Ausgabe- und Verteilung können Sie eine Berichtsbibliothek angeben, um den Bericht einfach freizugeben.

## <a name="generate-a-financial-report"></a>Finanzbericht generieren

Um einen Finanzbericht mit Microsoft Dynamics 365 for Finance and Operations zu erstellen, gehen Sie zu **Hauptbuch**\>**Abfragen und Berichte**\>**Finanzberichte**.

- Wählen Sie einen Bericht, um den Bericht zu erstellen und klicken Sie auf **Erstellen**.
- Fügen Sie das Feld**Daten berichten**und klicken sie auf **OK**.

Nachdem der Bericht generiert wurde, ist der Bericht verfügbar zum Anzeigen im Abschnitt **Berichte** anzuzeigen.

Sie können den Bericht**anzeigen** oder **löschen**.

Um einen Bericht zu generieren, öffnen Sie **Berichtsdesigner**, und klicken Sie anschließend auf die Schaltfläche Generieren in der Symbolleiste. Das Fenster Berichtswarteschlangenstatus wird geöffnet und gibt den Ort des Berichts in der Warteschlange an. Standardmäßig wird der generierte Bericht in Web Viewer geöffnet.

> [!NOTE]
> Sie können Berichte nur für Ordner und Orte generieren, auf die Sie zugreifen dürfen.

## <a name="schedule-report-generation"></a>Planen der Berichtsgenerierung
Viele Unternehmen verwenden einen Kernsatz von Berichten, die in Einklang mit ihren Geschäftsprozessen in geplanten Intervallen ausgeführt werden. Sie können festlegen, dass ein Bericht regelmäßig generiert wird, beispielsweise täglich, wöchentlich, monatlich oder jährlich. Sie können einen einzelnen Bericht oder eine Gruppe von Berichten, die mehrere Unternehmen umfasst, planen. Für jedes der Unternehmen, die z. B. in einer Berichtsbaumstruktur-Definition angegeben sind, müssen Anmeldeinformationen eingegeben werden. Wenn die Anmeldeinformationen nicht gültig sind, zeigt der Bericht nur die Informationen, für die Sie eine Zugriffsberechtigung haben, beispielsweise für das Unternehmen, bei dem Sie zu dem Zeitpunkt angemeldet sind. Die Ausgabeinformationen werden zuerst von der Berichtsgruppe und anschließend von den einzelnen Berichten gelesen.

Während Berichtszeitpläne erstellt und gespeichert werden, werden diese im Navigationsbereich unter Report Schedules angezeigt. Sie können Ordner zum Organisieren der Berichte erstellen. Wird ein einzelner Bericht in einem Berichtszeitplan nicht ausgeführt, hat dies keinen Einfluss auf die Ausführung aller anderen Berichte.

> [!IMPORTANT]
> Zum Erstellen, Ändern und Löschen von Berichtszeitplänen benötigen Sie die Rolle „Designer“ oder „Administrator“. Wenn ein Bericht ausgeführt wird, werden die Anmeldeinformationen des Benutzers, der den Zeitplan erstellt hat, verwendet, um den Bericht zu generieren.

### <a name="create-a-report-schedule"></a>Erstellen eines Berichtzeitplans

1. Wählen Sie im Berichts-Designer im Menü Datei Neu und dann Berichtzeitplan. Das Dialogfeld Neuer Berichtzeitplan wird geöffnet.
2. Unter Einstellungen wählen Sie einen individuellen Bericht oder eine Berichtsgruppe für den Zeitplan aus. Es sind nur Berichte oder Berichtsgruppen für das Unternehmen oder den Baustein verfügbar, bei dem Sie derzeit angemeldet sind.
3. Aktivieren Sie das Kontrollkästchen Aktiv, um den Berichtszeitplan zu aktivieren. Nur der Ersteller des Berichts oder ein Administrator kann einen Berichtszeitplan aktivieren oder deaktivieren.
4. Klicken Sie auf die Schaltfläche Berechtigungen, um die Unternehmensanmeldeinformationen einzugeben. Standardmäßig werden Ihre Anmeldeinformationen für das Unternehmen verwendet, bei dem Sie angemeldet sind. Sind andere Unternehmen enthalten, z. B. in Berichtsbaumstruktur-Definitionen, wählen Sie Gesonderte Anmeldeinformationen verwenden aus. Geben Sie dann die Anmeldeinformationen für die anderen im Berichtszeitplan enthaltenen Unternehmen ein. Sie können Windows-Authentifizierung auswählen oder für jedes Unternehmen einen Benutzernamen und ein Kennwort eingeben. Aktivieren Sie das Kontrollkästchen Anmeldeinformationen speichern, um die Anmeldeinformationen für diese Unternehmen zu speichern, und klicken Sie auf OK, um das Dialogfeld zu schließen.
5. Unter Häufigkeit im Feld Wiederholung starten wählen Sie das Datum aus, an dem der Zeitplan zu starten ist. Standardmäßig wird das aktuelle Systemdatum des Clientcomputers ausgewählt.
6. Wählen Sie im Feld Bericht ausführen unter die Uhrzeit für die Ausführung des Berichts aus. Wenn Sie eine Uhrzeit eingeben, die vor der aktuellen Systemzeit liegt, wird der Bericht am nächsten geplanten Datum ausgeführt.
7. Geben Sie im Bereich Wiederholungsmuster an, wie oft der Bericht ausgeführt werden soll. Standardmäßig wird täglich mit einem Wert des Intervalls (Tage) von 1. ausgewählt. Andere Optionen wöchentlich, monatlich oder jährlich.
8. Wählen Sie im Bereich Wiederholungsbereich aus, wann die Berichtsgenerierung beendet werden soll.

    - Kein Enddatum – Der Berichtszeitplan wird unendlich ausgeführt.
    - Feste Anzahl von Vorgängen – Der Berichtszeitplan wird so häufig ausgeführt, wie angegeben, und dann deaktiviert.
    - Ende bis – Der Berichtszeitplan wird am angegebenen Datum beendet.

9. Klicken Sie auf der Symbolleiste auf Speichern. Geben Sie im Dialogfeld Speichern unter einen eindeutigen Namen und eine Beschreibung für den Berichtszeitplan ein.

Zum Kopieren von Berichtszeitplänen müssen Sie die Rolle eines Designers oder Administrators haben. Auch wenn ein Administrator den Berichtszeitplan ändert, behält der Bericht die Anmeldeinformationen des Benutzers, der den Bericht erstellt hat.

### <a name="copy-a-report-schedule"></a>Kopieren eines Berichtzeitplans

1. Im Berichts-Designer klicken Sie im Navigationsbereich auf Berichtzeitpläne und öffnen den zu kopierenden Bericht.
2. Klicken Sie im Menü Datei auf Speichern unter, und geben Sie dann im Dialogfeld Speichern unter einen neuen Namen und eine Beschreibung für den Zeitplan ein. Klicken Sie auf OK. Daraufhin erscheint der neue Zeitplan im Navigationsbereich.
3. Ändern Sie im neuen Zeitplan die Felder und die Informationen nach Bedarf, und klicken Sie anschließend in der Symbolleiste auf Speichern, oder klicken Sie auf Speichern im Menü Datei.

Um einen Berichtszeitplan zu löschen, müssen Sie der Besitzer des Berichtszeitplans oder Administrator sein.

### <a name="delete-a-report-schedule"></a>Löschen eines Berichtzeitplans

1. Klicken Sie im Berichts-Designer auf Berichtzeitpläne im Navigationsbereich.
2. Wählen Sie den zu löschenden Berichtszeitplan aus, und klicken Sie dann auf Löschen, oder drücken Sie die ENTF-TASTE.
3. Klicken Sie im Dialogfeld zur Löschbestätigung auf Ja, um den Berichtszeitplan dauerhaft zu löschen. Wenn Sie nicht über die Berechtigung verfügen, den Zeitplan zu löschen, wird eine Meldung angezeigt und der Bericht wird nicht gelöscht.

### <a name="credentials-and-report-schedules"></a>Anmeldeinformationen und Berichtszeitpläne

Wenn Sie keine Anmeldeinformationen eingeben, die für alle Unternehmen erforderlich sind, die in den Berichten enthalten sind, erhalten Sie eine Meldung mit etwa folgendem Inhalt: „Sie müssen Ihre Anmeldeinformationen für die Unternehmen eingeben, die im Berichtszeitplan enthalten sind. Klicken Sie auf die Schaltfläche Berechtigungen, um Ihre Anmeldeinformationen einzugeben.“

Beispiel: Phyllis meldet sich mit Ihren Anmeldeinformationen und Ihrem Kennwort am Unternehmen A an. Sie erstellt einen Zeitplan für einen Bericht, der eine Berichtsbaumstruktur-Definition verwendet, um Daten aus mehreren Unternehmen zu erfassen. Beim Speichern dieses Berichtszeitplans wird Phyllis aufgefordert, die Anmeldeinformationen für die anderen Unternehmen einzugeben, die in der Berichtsbaumstruktur-Definition angegeben sind. Wenn Ihre Anmeldeinformationen ablaufen, werden die betroffenen Berichte im Berichtszeitplan nicht generiert, bis die Anmeldeinformationen aktualisiert wurden. Eine Meldung wird in der Berichtswarteschlange angezeigt, die angibt, dass die Berechtigungen aktualisiert werden müssen. Der Berichtszeitplan schlägt fehl, wenn eines der folgenden Szenarios auftritt (da sie Anmeldeinformationen erfordern):

- Ein neues Unternehmen wurde einer Berichtsstruktur für einen einzelnen Bericht hinzugefügt.
- Ein Bericht in einer Berichtsgruppe wurde geändert.
- Einer Berichtsgruppe wurde ein neuer Bericht für ein weiteres Unternehmen hinzugefügt.

Klicken Sie zum Fortfahren auf Berechtigungen im Dialogfeld Berichtzeitplanung, und geben Sie dann die entsprechenden Anmeldeinformationen ein.

## <a name="missing-account-analysis-feature"></a>Analysefunktion für fehlende Konten
Sie können nach Finanzkonten und Dimensionen suchen, die möglicherweise in allen Zeilendefinitionen, Berichtsbaumstruktur-Definitionen und Berichtsdefinitionen in einer Bausteingruppe fehlen. Dies ist hilfreich, wenn Sie mehrere Konten oder Bausteine während eines kurzen Zeitraum erstellen oder aktualisieren und Sie sicherstellen möchten, dass alle neuen Informationen in den Berichten enthalten sind.

Fehlende Konten werden anhand der höchsten und niedrigsten Werte einer Zeilendefinition oder der Berichtstruktur-Definition bestimmt. Es wird dann eine Liste von Konten angezeigt, die sich nicht in der Zeilendefinition oder in der Berichtstruktur-Definition befinden, aber Teil der Finanzdaten sind. Wenn ein fehlendes Konto größer oder kleiner ist als die Werte in der Zeilendefinition, wird das Konto nicht in die Liste fehlender Konten aufgenommen.

> [!TIP]
> Zu Überprüfungszwecken sollte dieser Vorgang vor dem Generieren monatlicher Berichte und beim Erstellen neuer Bausteine durchgeführt werden.

Bei Berichten mit Wertebereichen ist es weniger wahrscheinlich, dass Konten fehlen. Sofern möglich, verwenden Sie Bereiche im Baustein, um neue Konten nach dem Erstellen mit einzuschließen. Wird eine Berichtsdefinition für @ANY Unternehmen festgelegt, können Sie sich bei einem bestimmten Unternehmen anmelden und eine Analyse fehlender Konten für dieses Unternehmen ausführen.

> [!NOTE]
> Wurde ein neues Unternehmen hinzugefügt, müssen Sie das neue Unternehmen den Berichtstrukturen in allen vorhandenen Berichten hinzufügen, sonst wird das Unternehmen nicht in die Analyse fehlender Konten einbezogen.

### <a name="run-missing-account-analysis"></a>Analyse für fehlende Konten ausführen

1. Im Berichts-Designer klicken Sie auf Extras und anschließend Analyse für fehlende Konten.
2. Wählen Sie im Feld Unternehmensfilter ein Unternehmen aus, für das die Ergebnisse gefiltert werden sollen, oder wählen Sie Alle (kein Filter) aus, um die Ergebnisse für alle verfügbaren Unternehmen anzuzeigen.
3. Wählen Sie im Feld Dimensionsfilter eine Dimension aus, für die die Ergebnisse gefiltert werden sollen, oder wählen Sie Alle (kein Filter) aus, um alle Dimensionsinformationen für alle verfügbaren Dimensionen anzuzeigen.
4. Wählen Sie im Feld Gruppieren nach eine Option für die Sortierung der Ergebnisse aus. Sie können die Ergebnisse nach dem betroffenen Baustein oder nach Dimensions- und Wertsätzen sortieren.
5. Überprüfen Sie die angezeigten Ergebnisse. Wenn Sie im oberen Bereich ein Element auswählen, werden im unteren Bereich zusätzliche Informationen zu der Ausnahme angezeigt. Dies umfasst zugehörige Dimensionen, Werte und Berichte.
6. Um den betreffenden Artikel zu öffnen, klicken Sie auf das zugeordnete Symbol im Listenbereich, oder klicken mit der rechten Maustaste auf den Artikel und wählen Öffnen. Um mehrere Artikel auszuwählen, halten Sie während des Auswählens im unteren Bereich die STRG-Taste gedrückt.
7. Werden Werte, Bausteine oder Berichte zurückgegeben, die nicht in die Analyse einbezogen werden sollen, klicken Sie mit der rechten Maustaste auf den Artikel und wählen Ausschließen, oder Sie aktivieren das Kontrollkästchen Ausschließen neben dem Artikel, um den Artikel aus der Liste zu entfernen. Ausgeschlossene Artikel sind nicht enthalten, wenn die Liste aktualisiert wird. Halten Sie zum Auswählen mehrerer Elemente die STRG-Taste gedrückt, und wählen Sie die Elemente im unteren Bereich aus. Wenn Sie alle Elemente inklusive aller Ergebnisse, die Sie zuvor aus der Analyse ausgeschlossen haben, anzeigen möchten, aktivieren Sie das Kontrollkästchen Ausgeschlossene Bausteine und Werte anzeigen, und klicken Sie dann auf Aktualisieren.
8. Klicken Sie auf Aktualisieren, um bearbeitete Ausnahmen zu aktualisieren. Klicken Sie auf Ja, um eine vollständige Aktualisierung aller Ergebnisse durchzuführen, oder auf Nein, um eine teilweise Aktualisierung der bearbeiteten Elemente durchzuführen.

    > [!NOTE]
    > Das Formular wird beim Öffnen automatisch aktualisiert, es sei denn, es wurde in den letzten 15 Minuten bereits geöffnet.

9. Klicken Sie nach der Problembehebung auf OK, um das Dialogfeld zu schließen.

## <a name="keyboard-shortcuts-for-missing-account-analysis"></a>Tastenkombinationen für eine Analyse für fehlende Konten
Wenn Sie eine Analyse für fehlende Konten ausführen, sind die folgenden Tastenkombinationen verfügbar.

| Ergebnis                           | Verwenden Sie diese Tastenkombination |
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

