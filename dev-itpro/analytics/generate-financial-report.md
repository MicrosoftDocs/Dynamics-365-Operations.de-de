---
title: Finanzbericht generieren
description: "Dieses Thema enthält allgemeine Informationen zun Generieren von Finanzberichten."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: ShylaThompson
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 68843
ms.assetid: 271df6f4-12b7-4b3e-b2d7-36ea98ef1871
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 9b0d8fd9f5ae9d99f299cc71d7caef021ad3fb9d
ms.contentlocale: de-de
ms.lasthandoff: 05/25/2017


---

# <a name="generate-a-financial-report"></a>Finanzbericht generieren

[!include[banner](../includes/banner.md)]


Dieses Thema enthält allgemeine Informationen zun Generieren von Finanzberichten. 

Um einen Bericht zu generieren, öffnen Sie die Berichtsdefinition und klicken anschließend auf die Schaltfläche Generieren in der Symbolleiste. Das Fenster Berichtswarteschlangenstatus wird geöffnet und gibt den Ort des Berichts in der Warteschlange an. Standardmäßig wird der generierte Bericht im Web-Viewer geöffnet.
| ![Hinweis](https://i-technet.sec.s-msft.com/areas/global/content/clear.gif "Hinweis")**Hinweis**        |
|------------------------------------------------------------------------------------------------|
| Sie können Berichte nur für Ordner und Orte generieren, auf die Sie zugreifen dürfen. |

In der folgenden Tabelle werden die Optionen beschrieben, die für das Generieren von Berichten zulässig sind.

| Mit der folgenden Option...                                                                                | Weitere Informationen |
|---------------------------------------------------------------------------------------|----------------------|
| Einrichten eines Zeitplans, um einen Bericht oder eine Gruppe von Berichten automatisch zu generieren              |                      |
| Prüfen auf fehlende Konten oder Daten in einem Bericht und Validieren der Richtigkeit eines Berichts |                      |

Wenn Sie einen Bericht generieren, werden die Optionen verwendet, die Sie auf den Registerkarten Berichtsdefinition angegeben haben. Über die Registerkarte Ausgabe- und Verteilung können Sie eine Berichtsbibliothek angeben, um den Bericht einfach freizugeben.

## <a name="schedule-report-generation"></a> Berichterstellung planen
Viele Unternehmen haben einen Satz an Berichten, die im Einklang mit den Geschäftsprozessen in geplanten Intervallen ausgeführt werden. Sie können festlegen, dass ein Bericht regelmäßig generiert wird, beispielsweise täglich, wöchentlich, monatlich oder jährlich. Dabei kann es sich um einen einzelnen Bericht oder um eine Gruppe von Berichten handeln, die mehrere Unternehmen umfasst. Sie müssen Ihre Anmeldeinformationen für jedes festgelegte Unternehmen eingeben, beispielsweise für die in der Berichtsbaumstruktur-Definition. Wenn die Anmeldeinformationen nicht gültig sind, zeigt der Bericht nur die Informationen, für die Sie eine Zugriffsberechtigung haben, beispielsweise für das Unternehmen, bei dem Sie zu dem Zeitpunkt angemeldet sind. Die Ausgabeinformationen werden zuerst von der Berichtsgruppe und anschließend von den einzelnen Berichten gelesen.

Während Berichtszeitpläne erstellt und gespeichert werden, werden diese im Navigationsbereich unter Report Schedules angezeigt. Sie können Ordner erstellen, um die Berichte zu organisieren. Wenn ein einzelner Bericht in einem Zeitplan nicht ausgeführt wird, werden alle anderen Berichte weiterhin ausgeführt.
| ![Wichtig](https://i-technet.sec.s-msft.com/areas/global/content/clear.gif "Wichtig")**Wichtig**                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Zum Erstellen, Ändern und Löschen von Berichtszeitplänen müssen Sie die Rolle eines Designers oder Administrators haben. Wenn ein Bericht ausgeführt wird, werden die Anmeldeinformationen des Benutzers, der den Zeitplan erstellt hat, verwendet, um den Bericht zu generieren. |

### <a name="create-a-report-schedule"></a>Erstellen eines Berichtzeitplans

1.  Wählen Sie im Berichts-Designer im Menü Datei Neu und dann Berichtzeitplan. Das Dialogfeld Neuer Berichtzeitplan wird geöffnet.
2.  Unter Einstellungen wählen Sie einen individuellen Bericht oder eine Berichtsgruppe für den Zeitplan aus. Nur Berichte oder Berichtsgruppen für das ausgewählte Unternehmen oder den ausgewählten Baustein, für das bzw. den Sie gerade angemeldet sind, sind verfügbar.
3.  Aktivieren Sie das Kontrollkästchen Aktiv, um den Berichtszeitplan zu aktivieren. Nur der Ersteller des Berichts oder ein Administrator können einen Berichtszeitplan aktivieren oder deaktivieren.
4.  Klicken Sie auf die Schaltfläche Berechtigungen, um Unternehmens-Anmeldeinformationen einzugeben. Standardmäßig werden Ihre Anmeldeinformationen für das Unternehmen verwendet, bei dem Sie angemeldet sind. Wenn andere Unternehmen eingeschlossen sind, wie beispielsweise in den Berichtsbaumstruktur-Definitionen, wählen Sie Gesonderte Anmeldeinformationen verwenden und geben dann die Anmeldeinformationen für alle anderen Unternehmen ein, die im Berichtszeitplan enthalten sind. Sie können Windows-Authentifizierung auswählen oder einen Benutzernamen und ein Kennwort für jedes Unternehmen eingeben. Aktivieren Sie das Kontrollkästchen Anmeldeinformationen speichern, um die Anmeldeinformationen für diese Unternehmen zu speichern, und klicken Sie auf OK, um das Dialogfeld zu schließen.
5.  Unter Häufigkeit im Feld Wiederholung starten wählen Sie das Datum aus, an dem der Zeitplan zu starten ist. Standardmäßig wird das aktuelle Systemdatum des Clientcomputers ausgewählt.
6.  Wählen Sie im Feld Bericht ausführen am die Zeit aus, an dem der Bericht ausgeführt werden soll. Wenn Sie eine Zeit eingeben, die vor der aktuellen Systemzeit liegt, wird der Bericht am nächsten geplanten Datum ausgeführt.
7.  Im Wiederholungsmuster-Bereich geben Sie an, wie oft der Bericht ausgeführt wird. Standardmäßig wird täglich mit einem Wert des Intervalls (Tage) von 1. ausgewählt. Andere Optionen wöchentlich, monatlich oder jährlich.
8.  Im Wiederholungsbereich-Bereich wählen Sie aus, wann der Bericht nicht mehr generiert werden soll.
    -   Kein Enddatum – Der Berichtszeitplan wird auf unbestimmte Zeit ausgeführt.
    -   Anzahl der Vorkommen festlegen – Der Berichtszeitplan wird so oft ausgeführt wie angegeben und dann deaktiviert.
    -   Beenden zum – Der Berichtszeitplan endet am angegebenen Datum.

9.  Klicken Sie in der Symbolleiste auf Speichern. Geben Sie im Dialogfeld Speichern unter einen eindeutigen Namen und eine Beschreibung für den Berichtszeitplan ein.

Zum Kopieren von Berichtszeitplänen müssen Sie die Rolle eines Designers oder Administrators haben. Auch wenn ein Administrator den Berichtszeitplan ändert, behält der Bericht die Anmeldeinformationen des Benutzers, der den Bericht erstellt hat.
### <a name="copy-a-report-schedule"></a>Kopieren eines Berichtzeitplans

1.  Im Berichts-Designer klicken Sie im Navigationsbereich auf Berichtzeitpläne und öffnen den zu kopierenden Bericht.
2.  Wählen Sie im Menü Datei Speichern unter, und geben Sie dann einen neuen Namen und eine Beschreibung für den Zeitplan im Dialogfeld Speichern unter ein. Klicken Sie auf OK, und der neue Zeitplan wird im Navigationsbereich angezeigt.
3.  Ändern Sie im neuen Zeitplan die Felder und die Informationen nach Bedarf, und klicken Sie anschließend in der Symbolleiste auf Speichern, oder klicken Sie auf Speichern im Menü Datei.

Um einen Berichtszeitplan zu löschen, müssen Sie der Besitzer des Berichtszeitplans oder Administrator sein.
### <a name="delete-a-report-schedule"></a>Löschen eines Berichtzeitplans

1.  Klicken Sie im Berichts-Designer auf Berichtzeitpläne im Navigationsbereich.
2.  Wählen Sie den Berichtszeitplan aus, der gelöscht werden soll, und klicken Sie anschließend auf Löschen, oder drücken Sie die Löschen-Taste.
3.  Im Dialogfeld zum Bestätigen des Löschens klicken Sie auf Ja, um den Berichtszeitplans dauerhaft zu löschen. Wenn Sie nicht über die Berechtigung verfügen, den Zeitplan zu löschen, wird eine Meldung angezeigt und der Bericht wird nicht gelöscht.

### <a name="credentials-and-report-schedules"></a>Anmeldeinformationen und Berichtszeitpläne

Wenn Sie keine Anmeldeinformationen eingeben, die für alle Unternehmen erforderlich sind, die in den Berichten enthalten sind, erhalten Sie eine Meldung mit etwa folgendem Inhalt: „Sie müssen Ihre Anmeldeinformationen für die Unternehmen eingeben, die im Berichtszeitplan enthalten sind. Klicken Sie auf die Schaltfläche Berechtigungen, um Ihre Anmeldeinformationen einzugeben.“

Beispiel: Franziska meldet sich beim Unternehmen A mit Ihrem Anmeldenamen und Kennwort an. Sie erstellt einen Zeitplan für einen Bericht, der eine Berichtsbaumstruktur-Definition verwendet, um Daten aus mehreren Unternehmen zu erfassen. Wenn dieser Berichtszeitplan gespeichert wird, wird Franziska aufgefordert, die Anmeldeinformationen für die anderen Unternehmen einzugeben, die in der Berichtsbaumstruktur-Definition angegeben sind. Wenn Ihre Anmeldeinformationen ablaufen, werden die betroffenen Berichte im Berichtszeitplan nicht generiert, bis die Anmeldeinformationen aktualisiert wurden. Eine Meldung wird in der Berichtswarteschlange angezeigt, die angibt, dass die Berechtigungen aktualisiert werden müssen. Der Berichtszeitplan schlägt fehl, wenn eines der folgenden Szenarios auftritt (da sie Anmeldeinformationen erfordern):
-   Ein neues Unternehmen wurde einer Berichtsstruktur für einen einzelnen Bericht hinzugefügt.
-   Ein Bericht in einer Berichtsgruppe wurde geändert.
-   Ein neuer Bericht für ein weiteres Unternehmen wurde einer Berichtsgruppe hinzugefügt.

Klicken Sie zum Fortfahren auf Berechtigungen im Dialogfeld Berichtzeitplanung, und geben Sie dann die entsprechenden Anmeldeinformationen ein.

## <a name="missing-account-analysis-feature"></a>Funktion für Analyse fehlender Konten
Sie können nach Finanzkonten und Dimensionen suchen, die möglicherweise in allen Zeilendefinitionen, Berichtsbaumstruktur-Definitionen und Berichtsdefinitionen in einer Bausteingruppe fehlen. Dies ist hilfreich, wenn Sie mehrere Konten oder Bausteine während eines kurzen Zeitraum erstellen oder aktualisieren und Sie sicherstellen möchten, dass alle neuen Informationen in den Berichten enthalten sind.

Fehlende Konten werden anhand der höchsten und niedrigsten Werte einer Zeilendefinition oder der Berichtstruktur-Definition bestimmt. Es wird dann eine Liste von Konten angezeigt, die sich nicht in der Zeilendefinition oder in der Berichtstruktur-Definition befinden, aber Teil der Finanzdaten sind. Wenn ein fehlendes Konto größer oder kleiner ist als die Werte in der Zeilendefinition, ist dieses Konto nicht in der Liste fehlender Konten enthalten.
| ![Tipp](https://i-technet.sec.s-msft.com/areas/global/content/clear.gif "Tipp")**Tipp**                                             |
|----------------------------------------------------------------------------------------------------------------------------------|
| Zu Prüfungszwecken sollte dieser Prozess ausgeführt werden, bevor Sie monatliche Berichte generieren und wenn Sie neue Bausteine erstellen. |

Bei Berichten mit Wertebereichen ist es weniger wahrscheinlich, dass Konten fehlen. Sofern möglich, verwenden Sie Bereiche im Baustein, um neue Konten nach dem Erstellen mit einzuschließen. Wird eine Berichtsdefinition für @ANY Unternehmen festgelegt, können Sie sich bei einem bestimmten Unternehmen anmelden und eine Analyse fehlender Konten für dieses Unternehmen ausführen.
| ![Hinweis](https://i-technet.sec.s-msft.com/areas/global/content/clear.gif "Hinweis")**Hinweis**                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Wurde ein neues Unternehmen hinzugefügt, müssen Sie das neue Unternehmen den Berichtstrukturen in allen vorhandenen Berichten hinzufügen, sonst wird das Unternehmen nicht in die Analyse fehlender Konten einbezogen. |

### <a name="run-missing-account-analysis"></a>Analyse für fehlende Konten ausführen

1.  Im Berichts-Designer klicken Sie auf Extras und anschließend Analyse für fehlende Konten.
2.  Wählen Sie im Feld Unternehmensfilter ein Unternehmen für das Filtern aus, oder wählen Sie Alle (kein Filter), um die Ergebnisse aller verfügbaren Unternehmen anzuzeigen.
3.  Wählen Sie im Feld Dimensionsfilter eine Dimension aus, um die Ergebnisse zu filtern, oder wählen Sie Alle (kein Filter), um alle Dimensionsinformationen für alle verfügbaren Dimensionen anzuzeigen.
4.  Wählen Sie im Feld Gruppieren nach die geeignete Option zum Sortieren der Ergebnisse aus. Sie können Ergebnisse gemäß dem Baustein sortieren, der betroffen ist, oder Sie können Ergebnisse nach Dimensions- und Wertsätzen sortieren.
5.  Überprüfen Sie die angezeigten Ergebnisse. Wenn Sie einen Artikel im oberen Bereich auswählen, werden im unteren Bereich zusätzliche Informationen zur Ausnahme angezeigt. Hierzu zählen zugehörige Dimensionen, Werte und Berichte.
6.  Um den betreffenden Artikel zu öffnen, klicken Sie auf das zugeordnete Symbol im Listenbereich, oder klicken mit der rechten Maustaste auf den Artikel und wählen Öffnen. Um mehrere Artikel auszuwählen, halten Sie während des Auswählens im unteren Bereich die STRG-Taste gedrückt.
7.  Werden Werte, Bausteine oder Berichte zurückgegeben, die nicht in die Analyse einbezogen werden sollen, klicken Sie mit der rechten Maustaste auf den Artikel und wählen Ausschließen, oder Sie aktivieren das Kontrollkästchen Ausschließen neben dem Artikel, um den Artikel aus der Liste zu entfernen. Ausgeschlossene Artikel sind nicht enthalten, wenn die Liste aktualisiert wird. Um mehrere Artikel auszuwählen, halten Sie beim Auswählen im unteren Bereich die STRG-Taste gedrückt. Zum Anzeigen aller Artikel einschließlich der Ergebnisse, die Sie zuvor aus der Analyse ausgeschlossen haben, aktivieren Sie das Kontrollkästchen Ausgeschlossene Bausteine und Werte anzeigen und klicken dann auf Aktualisieren.
8.  Klicken Sie auf Aktualisieren, um Ausnahmen zu aktualisieren, die Sie adressiert haben. Klicken Sie auf Ja, um alle Ergebnisse zu aktualisieren, oder klicken Sie auf Nein für eine teilweise Aktualisierung der betroffenen Artikel.
    | ![Hinweis](https://i-technet.sec.s-msft.com/areas/global/content/clear.gif "Hinweis")**Hinweis**                    |
    |------------------------------------------------------------------------------------------------------------|
    | Das Formular wird automatisch aktualisiert, wenn es geöffnet wird, es sei denn, das Formular wurde in den letzten 15 Minuten geöffnet. |

9.  Klicken Sie nach der Problembehebung auf OK, um das Dialogfeld zu schließen.

## <a name="keyboard-shortcuts-for-missing-account-analysis"></a>Tastenkombinationen für eine Analyse für fehlende Konten
Wenn Sie eine Analyse für fehlende Konten ausführen, sind die folgenden Tastenkombinationen verfügbar.

| Ergebnis                           | Verwenden Sie diese Tastenkombination |
|--------------------------------------|----------------------------|
| Filtern nach Unternehmen                    | ALT+C                      |
| Filtern nach Dimension                  | ALT+D                      |
| Auswahl des Felds Gruppieren nach            | ALT+G                      |
| Ausgeschlossene Blöcke und Werte anzeigen      | ALT+S                      |
| Ergebnisse aktualisieren                      | ALT+R                      |
| Ausgewählten Baustein ausschließen  | ALT+X                      |
| Ausgewählte Zeilendefinition ausschließen  | STRG+B                     |
| Ausgewählten Dimensionswert ausschließen | STRG+D                     |
| Ausgewählte Berichtsdefinition öffnen  | STRG+R                     |
| Ausgewählte Zeilendefinition öffnen     | STRG+O                     |

 
<a name="see-also"></a>Siehe auch
--------

[Finanzberichterstellung](financial-reporting-intro.md)

[Berichts-Designer-Schnittstelle](report-designer-interface.md)



