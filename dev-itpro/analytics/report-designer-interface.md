---
title: Berichts-Designer-Schnittstelle
description: "Dieser Artikel erläutert das Navigieren durch den Berichtsdesigner und wie Sie die verschiedenen Optionen Ihren Bedürfnissen entsprechend verwenden."
author: RobinARH
manager: AnnBe
ms.date: 2016-03-07 18 - 50 - 10
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 59041
ms.assetid: 054de5b0-8618-4195-be12-f031b4bb4d74
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: 58c56aca6f339a5ec13703605334dd45b208ab2c
ms.lasthandoff: 03/29/2017


---

# <a name="report-designer-interface"></a>Berichts-Designer-Schnittstelle

Dieser Artikel erläutert das Navigieren durch den Berichtsdesigner und wie Sie die verschiedenen Optionen Ihren Bedürfnissen entsprechend verwenden. 

<a name="report-designer-menu-commands"></a>Berichts-Designer-Menübefehle
-----------------------------

Die folgenden Tabellen beschreiben die Menübefehle und Optionen, die Sie verwenden können, wenn Sie Finanzberichte entwerfen. Einige Menübefehle und Optionen sind nur in bestimmten Umständen verfügbar. Beispielsweise sind Befehle für das Höherstufen und das Tieferstufen von Berichtseinheiten nur verfügbar, wenn Sie eine Berichtsbaumstruktur-Definition ändern.

### <a name="file-menu"></a>Menü "Datei"

Das **Datei**-Menü ist für alle Benutzer verfügbar und umfasst die folgenden Befehle.

| Befehl                           | Beschreibung                                                                                                                                                                                      |
|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Neu                               | Erstellen Sie eine neue Berichtsdefinition, eine Zeilendefinition, eine Spaltendefinition, eine Berichtsbaumstruktur-Definition, eine Berichtsgruppendefinition oder einen Ordner. Zusätzliche Optionen sind je nach Ihrer Benutzerrolle verfügbar. |
| Geöffnet                              | Öffnen Sie eine vorhandene Zeilendefinition, eine Spaltendefinition, eine Berichtsbaumstruktur-Definition oder eine Berichtsdefinition.                                                                                             |
| Schließen                             | Schließen Sie den aktuellen Baustein.                                                                                                                                                                |
| Alle schließen                         | Schließen Sie alle Bausteine.                                                                                                                                                                       |
| Speichern                              | Speichern Sie die aktuelle Zeilendefinition, Spaltendefinition, Berichtsbaumstruktur-Definition oder Berichtsdefinition.                                                                                             |
| Speichern unter                           | Speichern Sie die aktuelle Zeilendefinition, Spaltendefinition, Berichtsbaumstruktur-Definition oder Berichtsdefinition unter einem neuen Namen.                                                                            |
| Eigenschaften                        | Öffnen Sie das Dialogfeld **Eigenschaften**, in dem Sie den Namen und die Beschreibung eines Berichts ändern können.                                                                                                   |
| Generieren                          | Generieren Sie den aktuellen Bericht. Dieser Befehl ist aus einer Berichtsdefinition verfügbar.                                                                                                                 |
| Bericht anzeigen                       | Öffnet die aktuelle Version des generierten Berichts in Dynamics 365 für Arbeitsgänge. Dieser Befehl ist aus einer Berichtsdefinition verfügbar, wenn mindestens einen Bericht generiert wurde.                                 |
| Aktuelle Berichtsdefinitionen         | Zeigen Sie eine Liste mit Berichten an, die vor kurzem erstellt oder geändert wurden. Sie können dann einen Bericht in der Liste auswählen.                                                                                    |
| Aktuelle Zeilendefinitionen            | Zeigen Sie eine Liste mit Zeilendefinitionen an, die vor kurzem erstellt oder geändert wurden. Sie können dann eine Zeilendefinition in der Liste auswählen.                                                                    |
| Aktuelle Spaltendefinitionen         | Zeigen Sie eine Liste mit Spaltendefinitionen an, die vor kurzem erstellt oder geändert wurden. Sie können dann eine Spaltendefinition in der Liste auswählen.                                                              |
| Aktuelle Berichtsbaumstruktur-Definitionen | Zeigen Sie eine Liste mit Berichtsbaumstruktur-Definitionen an, die vor kurzem erstellt oder geändert wurden. Sie können dann eine Berichtsbaumstruktur-Definition in der Liste auswählen.                                              |
| Beenden                              | Beenden Sie den Berichts-Designer.                                                                                                                                                                            |

### <a name="edit-menu"></a>Bearbeiten-Menü

Das Menü **Bearbeiten** ist für Benutzer mit der **Designer**-Rolle oder der **Administrator**-Rolle verfügbar. Dieses Menü beinhaltet die folgenden Befehle:

| Befehl                                | Beschreibung                                                                                                                                                                                                        |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Rückgängig machen                                   | Letzte Aktivität rückgängig machen.                                                                                                                                                                                              |
| Wiederherstellen                                   | Rückgängigmachen der letzten Aktivität stornieren.                                                                                                                                                                                      |
| Ausschneiden                                    | Ausgewähltes Element kopieren und der Zwischenablage hinzufügen.                                                                                                                                                            |
| Kopieren                                   | Kopiert den ausgewählten Text in die Zwischenablage.                                                                                                                                                                           |
| Einfügen                                  | Fügen Sie den zuletzt ausgeschnittenen oder kopierten Text aus der Zwischenablage ein.                                                                                                                                                    |
| Löschen                                  | Löschen Sie den Inhalt der ausgewählten Bausteinzelle.                                                                                                                                                           |
| Suchen                                   | Öffnen Sie das Dialogfeld **Suchen und ersetzen**, in dem Sie Text im Ansichtsbereich suchen können.                                                                                                                              |
| Ersetzen                                | Öffnen Sie das Dialogfeld **Suchen und ersetzen**, in dem Sie Text im Ansichtsbereich suchen und ersetzen können.                                                                                                                  |
| Zeilen aus Dimensionen einfügen            | Öffnen Sie das Dialogfeld **Zeilen aus Dimensionen einfügen**, in dem Sie die Dimensionswerte auswählen können, die in die Zeilendefinition enthalten sein sollen. Dieser Befehl ist aus einer Zeilendefinition verfügbar.                                  |
| Zeilen neu nummerieren                          | Alle numerischen Zeilencodes neu nummereiren. Dieser Befehl ist aus einer Zeilendefinition verfügbar.                                                                                                                                   |
| Zeilenlinks                              | Öffnen Sie das Dialogfeld **Zeilenlinks**, in dem Sie die Quellen für Datenverbindungen in Zeilendefinitionen und in den Berichtsbaumstruktur-Definitionen angeben können. Dieser Befehl ist aus einer Zeilendefinition verfügbar.                            |
| Rundungsregulierungen                    | Öffnen Sie das Dialogfeld **Rundungsregulierungen**, in dem Sie die Parameter für das Runden angeben können. Dieser Befehl ist aus einer Zeilendefinition verfügbar.                                                                  |
| Dimensionssätze verwalten                  | Öffnen Sie das Dialogfeld **Dimensionssätze**, in dem Sie Dimensionssätze erstellen und ändern können. Dieser Befehl ist von einer Zeilendefinition oder aus einer Berichtsbaumstruktur-Definition verfügbar.                                              |
| Zeile einfügen                             | Fügen Sie eine leere Zeile in die Zeilendefinition oder eine leere Kopfzeile in die Spaltendefinition ein. Dieser Befehl ist von einer Zeilendefinition oder aus einer Spaltendefinition aus verfügbar.                                               |
| Zeile löschen                             | Löschen Sie die ausgewählte Zeile aus der Zeilendefinition oder die ausgewählte Kopfzeile aus der Spaltendefinition. Dieser Befehl ist von einer Zeilendefinition oder aus einer Spaltendefinition aus verfügbar.                                       |
| Spalte einfügen                          | Fügen Sie eine leere Spalte in die Spaltendefinition ein. Dieser Befehl ist aus einer Spaltendefinition verfügbar.                                                                                                             |
| Spalte löschen                          | Löschen Sie die ausgewählte Spalte aus der Spaltendefinition. Dieser Befehl ist aus einer Spaltendefinition verfügbar.                                                                                                         |
| Berichtseinheiten aus Dimensionen einfügen | Öffnen Sie das Dialogfeld **Berichtseinheiten aus Dimensionen einfügen**, in dem Sie die Dimensionswerte auswählen können, die in die Berichtsbaumstruktur-Definition enthalten sein sollen. Dieser Befehl ist aus einer Berichtsbaumstruktur-Definition verfügbar. |
| Dimensionssatzhierarchie einfügen         | Öffnen Sie das Dialogfeld **Dimensionssatzhierarchie**, in dem Sie eine Dimensionssatzhierarchie aus den Finanzdaten importieren können. Dieser Befehl ist in einer Berichtsbaumstruktur-Definition für A. verfügbar. \ \ Finanzdimensionen dimensionsbasiertes System.  |
| Berichtserstelluungseinheit einfügen                  | Fügen Sie eine leere Zeile in die Berichtsbaumstruktur-Definition ein. Dieser Befehl ist aus einer Berichtsbaumstruktur-Definition verfügbar.                                                                                                |
| Berichtseinheit löschen                  | Löschen Sie die ausgewählte Berichtseinheitenzeile aus der Berichtsbaumstruktur-Definition. Dieser Befehl ist aus einer Berichtsbaumstruktur-Definition verfügbar.                                                                             |

### <a name="view-menu"></a>Menü "Ansicht"

Das Menü **Ansicht** ist für alle Benutzer verfügbar und umfasst die folgenden Befehle.

| Befehl         | Beschreibung                                                            |
|-----------------|------------------------------------------------------------------------|
| Navigationsbereich | Blenden Sie den Navigationsbereich ein- und aus.                                      |
| Symbolleisten        | Wählen Sie die Symbolleisten aus, die angezeigt werden.                                  |
| Statusleiste      | Dient zum Anzeigen oder Ausblenden der Statusinformationen im **Berichts-Designer**-Fenster. |
| Willkommensseite    | Öffnen Sie die **Begrüßungsseite**.                                             |

### <a name="format-menu"></a>Menü "Formatieren"

Das Menü **Formatieren** ist für Benutzer mit der **Designer**-Rolle oder der **Administrator**-Rolle verfügbar. Dieses Menü beinhaltet die folgenden Befehle:

| Befehl               | Beschreibung                                                                                                                                                                                                          |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Formate und Formatierung | Öffnen Sie das Dialogfeld **Formate und Formatierung**, in dem Sie das Format für Text in Zeilendefinitionen und in den Spaltendefinitionen erstellen und ändern können. Dieser Befehl ist von einer Zeilendefinition oder einer Spaltendefinition aus verfügbar. |
| Spaltenbreite          | Öffnen Sie das Dialogfeld **Spaltenbreite**, in dem Sie die Breite der ausgewählten Spalte festlegen können. Dieser Befehl ist von einer Zeilendefinition, einer Spaltendefinition oder einer Berichtsbaumstruktur-Definition verfügbar.                      |
| Ausblenden                  | Ausgewählte Spalte ausblenden. Dieser Befehl ist von einer Zeilendefinition, einer Spaltendefinition oder einer Berichtsbaumstruktur-Definition verfügbar.                                                                                        |
| Einblenden                | Blenden Sie die ausgeblendeten Spalten zwischen den ausgewählten Spalten ein. Dieser Befehl ist von einer Zeilendefinition, einer Spaltendefinition oder einer Berichtsbaumstruktur-Definition verfügbar.                                                      |

### <a name="company-menu"></a>Menü "Unternehmen"

Das Menü **Unternehmen** ist für Benutzer mit der **Designer**-Rolle oder der **Administrator**-Rolle verfügbar. Dieses Menü beinhaltet die folgenden Befehle:

| Befehl               | Beschreibung                                                                                                            |
|-----------------------|------------------------------------------------------------------------------------------------------------------------|
| Unternehmen             | Öffnen Sie das Dialogfeld **Unternehmen**, in dem Sie Unternehmen erstellen und ändern können.                                          |
| Baustein-Gruppen | Öffnen Sie das Dialogfeld **Baustein-Gruppen**, in dem Sie Baustein-Gruppen erstellen, ändern, importieren und exportieren können. |

### <a name="go-menu"></a>Menü "Start"

Das Menü **Start** ist für alle Benutzer verfügbar und umfasst die folgenden Befehle. **Hinweis:** Diese Befehle haben keine sichtbare Auswirkungen, es sei denn, der Navigationsbereich wird angezeigt.

| Befehle                   | Beschreibung                                                                        |
|----------------------------|------------------------------------------------------------------------------------|
| Berichtsdefinition         | Zeigen Sie Brichtsdefinitionen im Navigationsbereich an.                                    |
| Zeilendefinitionen            | Zeigen Sie Zeilendefinitionen im Navigationsbereich an.                                       |
| Spaltendefinition         | Zeigen Sie Spaltendefinitionen im Navigationsbereich an.                                    |
| Berichtsbaumstruktur-Definitionen | Zeigen Sie Brichtsbaumstruktur-Definitionen im Navigationsbereich an.                            |
| Sicherheit                   | Zeigen Sie Sicherheitsinformationen für Benutzer, Gruppen und Unternehmen im Navigationsbereich an. |

### <a name="tools-menu"></a>Menü "Extras"

Das **Extras**-Menü ist für alle Benutzer verfügbar, aber einige Befehle haben beschränkte Verfügbarkeit. Dieses Menü beinhaltet die folgenden Befehle:

| Befehl                       | Beschreibung                                                                                                                                                                                                       |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Schützen                       | Wenden Sie ein Kennwort auf den aktuellen Baustein an. Dieser Befehl ist für Benutzer mit der **Designer**-Rolle oder der **Administrator**-Rolle verfügbar.                                                                           |
| Berichtswarteschlangenstatus           | Öffnet das Dialogfeld **Berichtswarteschlangenstatus**, in dem Sie alle kürzlich generierten Berichte und die Details für jeden Bericht finden können.                                                                                    |
| Quellsysteminformationen     | Zeigen Sie die Einstellungen für Ihr Microsoft Dynamics ERP-System an. Dieser Befehl ist für Benutzer mit der **Designer**-Rolle oder der **Administrator**-Rolle verfügbar.                                                                 |
| Ausgecheckte Elemente             | Zeigen Sie die Zeilendefinitionen, die Spaltendefinitionen, die Berichtsbaumstruktur-Definitionen und die Berichtsdefinitionen an, die zur Zeit geöffnet sind. Dieser Befehl ist für Benutzer mit der **Designer**-Rolle oder der **Administrator**-Rolle verfügbar. |
| Aktualisieren Sie zwischengespeicherte Finanzdaten | Aktualisieren Sie die Daten in der Finanzdimensionsspalte.                                                                                                                                                               |
| Optionen                       | Öffnen Sie das Dialogfeld **Optionen**, in dem Sie Benutzereinstellungen für Berichts-Designer ändern können.                                                                                                                       |

### <a name="window-menu"></a>Menü "Fenster"

Das Menü **Fenster** ist für alle Benutzer verfügbar und umfasst die folgenden Befehle.

| Befehl              | Beschreibung                                                                                                                                                                                   |
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Untereinander    | Hier werden alle offenen Fenster nebeneinander angezeigt.                                                                                                                                                     |
| Nebeneinander      | Hier werden alle offenen Fenster gestapelt angezeigt.                                                                                                                                               |
| Kaskade              | Zeigen Sie alle offenen Fenster so an, dass die Titelleiste jedes Fensters sichtbar ist.                                                                                                                      |
| Horizontal fixieren    | Sperren Sie die ausgewählte Zeile, sodass sie bei einem Bildlauf weiterhin im Fenster angezeigt wird. Dieser Befehl ist für Benutzer mit der **Designer**-Rolle oder der **Administrator**-Rolle verfügbar.       |
| Vertikal fixieren      | Sperren Sie die ausgewählte Spalte, sodass sie bei einem Bildlauf weiterhin im Fenster angezeigt wird. Dieser Befehl ist für Benutzer mit der **Designer**-Rolle oder der **Administrator**-Rolle verfügbar. |
| Liste der geöffneten Fenster | Hier wird eine Liste von Fenstern angezeigt, die offen sind. Wählen Sie ein Fenster aus, um es vorne anzuzeigen.                                                                                                               |

### <a name="help-menu"></a>Menü "Hilfe"

Das Menü **Hilfe** ist für alle Benutzer verfügbar und umfasst die folgenden Befehle.

| Befehl | Beschreibung                                                  |
|---------|--------------------------------------------------------------|
| Hilfe    | Öffnet das Dynamics 365 für Arbeitsgangshilfe-Wiki-Seite für die Finanzberichte. |
|         |                                                              |

## <a name="report-designer-toolbar-buttons"></a>Symbolleistenschaltflächen des Bericht-Designers
Die folgenden Tabellen beschreiben die Schaltflächen der Symbolleiste, die Sie verwenden können, wenn Sie Berichte entwerfen. Einige Schaltflächen der Symbolleiste sind nur unter bestimmten Umständen verfügbar. Beispielsweise sind Schaltflächen für das Höherstufen und das Tieferstufen von Berichtseinheiten nur verfügbar, wenn Sie eine Berichtsbaumstruktur-Definition ändern.

### <a name="standard-toolbar"></a>Standardsymbolleiste

Die Standardsymbolleiste bieten schnellen Zugriff auf Datei- und Bearbeiten-Befehle. Diese Symbolleiste enthält die folgenden Schaltflächen.

| Schaltfläche                                                                                                                                                                                   | Beschreibung                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [![New button](./media/rowc130389.png)](./media/rowc130389.png)                              | Erstellen Sie eine neue (leere) Berichtsdefinition, Zeilendefinition, Spaltendefinition oder Berichtsbaumstruktur-Definition.                                                                               |
| [] (offene Schaltfläche ![. /media/openfolderc130389.png)]". /media/openfolderc130389.png)               | Öffnen Sie eine vorhandene Zeilendefinition, eine Spaltendefinition, eine Berichtsbaumstruktur-Definition oder eine Berichtsdefinition.                                                                                   |
| ![Abwehrschaltfläche( [] . /media/savec130389.png)]". /media/savec130389.png)                           | Speichern Sie die aktuelle Zeilendefinition, Spaltendefinition, Berichtsbaumstruktur-Definition oder Berichtsdefinition.                                                                                   |
| Mit ![( [] . /media/copyc130389.png)]". /media/copyc130389.png)                           | Kopiert den ausgewählten Text in die Zwischenablage.                                                                                                                                               |
| ![Schnittschaltfläche( [] . /media/cutc130389.png)]". /media/cutc130389.png)                              | Ausgewähltes Element kopieren und der Zwischenablage hinzufügen.                                                                                                                                |
| ![Pastenschaltfläche( [] . /media/pastec130389.png)]". /media/pastec130389.png)                        | Fügen Sie den Text aus der Zwischenablage ein.                                                                                                                                                    |
| ![[] (rückgängig machen Schaltfläche. /media/undoc130389.png)]". /media/undoc130389.png)                           | Letzte Aktivität rückgängig machen.                                                                                                                                                                  |
| [] (![überprüfen Schaltfläche. /media/redoc130389.png)]". /media/redoc130389.png)                           | Rückgängigmachen der letzten Aktivität stornieren.                                                                                                                                                          |
| [](![Suchschaltfläche . /media/findc130389.png)]". /media/findc130389.png)                           | Öffnen Sie das Dialogfeld **Suchen und ersetzen**, in dem Sie Text im aktiven Fenster suchen und ersetzen können.                                                                                  |
| ![] [Zeilenschaltfläche![" . /media/insertrowc130389.png)]". /media/insertrowc130389.png)           | Fügen Sie eine leere Zeile in die Zeilendefinition oder eine leere Kopfzeile in die Spaltendefinition ein. Diese Schaltfläche ist von einer Zeilendefinition oder aus einer Spaltendefinition aus verfügbar.                    |
| ![] [Spaltenschaltfläche![" . /media/insertcolumnc130389.png)]". /media/insertcolumnc130389.png)  | Fügen Sie eine leere Spalte in die Spaltendefinition ein. Diese Schaltfläche ist aus einer Spaltendefinition verfügbar.                                                                                  |
| ![Sperrenschaltfläche( [] . /media/lockc130389.png)]". /media/lockc130389.png)                           | Wenden Sie ein Kennwort auf den aktuellen Baustein an. Diese Schaltfläche ist für Benutzer mit der **Designer**-Rolle oder der **Administrator**-Rolle verfügbar.                                                 |
| ![Zeilenlinkschaltfläche ([]. /media/rowlinkc130389.png)]". /media/rowlinkc130389.png)                 | Öffnen Sie das Dialogfeld **Zeilenlinks**, in dem Sie die Quellen für Datenverbindungen in Zeilendefinitionen und in den Berichtsbaumstruktur-Definitionen angeben können. Diese Schaltfläche ist aus einer Zeilendefinition verfügbar. |
| ![[] (höher stufen Schaltfläche. /media/promotec130389.png)]". /media/promotec130389.png)                  | Stufen Sie eine Einheit der Berichtsbaumstruktur-Definition hoch. Wenn Sie eine untergeordnete Einheit auswählen und dann auf **Höherstufen** klicken, wird die untergeordnete Einheit auf die Ebene der übergeordneten Einheit verschoben.                |
| ![[] (tiefer stufen Schaltfläche. /media/demotec130389.png)]". /media/demotec130389.png)                     | Stufen Sie eine Einheit der Berichtsbaumstruktur-Definition herunter. Wenn Sie eine Einheit auswählen und dann auf **Tieferstufen** klicken, wird die Einheit zu einem untergeordneten Element der vorangehenden Einheit.                               |
| [] (![erweitern Schaltfläche. /media/expandtreebuttonc130389.png)]". /media/expandtreebuttonc130389.png) | Erweitern Sie alle Einheiten der Berichtsbaumstruktur-Definition auf der Ebene der ausgewählten Einheit.                                                                                                   |
| ![Einsturzschaltfläche( [] . /media/collapsec130389.png)]". /media/collapsec130389.png)               | Reduzieren Sie die Berichtsbaumstruktur.                                                                                                                                                           |
| [] (![Schaltfläche. /media/helpc130389.png)]". /media/helpc130389.png)                           | Hilfe öffnen.                                                                                                                                                                             |

### <a name="formatting-toolbar"></a>Formatsymbolleiste

Die Formatierungssymbolleiste bietet einfachen Zugriff auf Formatbefehle. Diese Symbolleiste enthält die folgenden Schaltflächen.

| Schaltfläche                                                                                                                                                                                                   | Beschreibung                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| ![Schriftschnittschaltfläche( [] . /media/formattingc130389.png)]". /media/formattingc130389.png)                         | Hiermit können Sie den ausgewählten Schriftschnitt auf den aktuellen Text anwenden.      |
| ![Schriftartschaltfläche( [] . /media/fonttype.png)]". /media/fonttype.png)                                                 | Legen Sie die ausgewählte Schriftart für den aktuellen Text fest.              |
| ![Schriftgrößeschaltfläche( [] . /media/fontsize.png)]". /media/fontsize.png)                                            | Legen Sie die ausgewählte Schriftgröße (in Punkten) für den aktuellen Text fest. |
| [] (Schaltfläche fette ![. /media/boldc130389.png)]". /media/boldc130389.png)                                           | Hebt den aktuellen Text fett hervor.                             |
| [] (Schaltfläche kursive ![. /media/italicsc130389.png)]". /media/italicsc130389.png)                                   | Hebt den aktuellen Text kursiv hervor.                           |
| ![Unterstrichschaltfläche( [] . /media/underlinec130389.png)]". /media/underlinec130389.png)                            | Unterstreicht den aktuellen Text.                             |
| ![Verringerungseinzugsschaltfläche ([]. /media/outdentlsc130389.png)]". /media/outdentlsc130389.png)                      | Verkleinern Sie die Einzugsebene des aktuellen Texts.                |
| ![Erhöhungseinzugsschaltfläche ([]. /media/indentlsc130389.png)]". /media/indentlsc130389.png)                        | Vergrößern Sie die Einzugsebene des aktuellen Texts.                |
| ![Hintergrundfarbenschaltfläche( [] . /media/fillbackgroundcolorc130389.png)]". /media/fillbackgroundcolorc130389.png) | Ändern Sie die Hintergrundfarbe der aktuellen Zelle        |
| ![Schriftfarbenschaltfläche( [] . /media/fontcolorc130389.png)]". /media/fontcolorc130389.png)                           | Ändern Sie die Farbe des aktuellen Texts.                   |

### <a name="report-designer-toolbar"></a>Symbolleisten des Bericht-Designers

Die Berichtsdesigner-Symbolleiste bietet Schnellzugriff auf Befehle für das Navigieren innerhalb des Berichtsdesigners. Diese Symbolleiste enthält die folgenden Schaltflächen.

| Schaltfläche                                                                                                                                                                                          | Beschreibung                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ![Berichtsdefinitionsschaltfläche( [] . /media/reportc130389.png)]". /media/reportc130389.png)                 | Hier wird die Berichtsdefinition angezeigt, die im Menü **Fenster** aufgeführt ist.                                                                                                            |
| ![Zeilendefinitionsschaltfläche( [] . /media/rowc130389.png)]". /media/rowc130389.png)                          | Hier wird die Zeilendefinition angezeigt, die der aktiven Berichtsdefinition zugewiesen ist.                                                                                                    |
| ![Spaltendefinitionsschaltfläche( [] . /media/columnc130389.png)]". /media/columnc130389.png)                 | Hier wird die Spaltendefinition angezeigt, die der aktiven Berichtsdefinition zugewiesen ist.                                                                                                 |
| ![Berichtsbaumstruktur-Definitions-Schaltfläche ([]. /media/treec130389.png)]". /media/treec130389.png)             | Hier wird die Berichtsbaumstruktur-Definition angezeigt, die der aktiven Berichtsdefinition zugewiesen ist.                                                                                         |
| ![Berichts-Viewer-Schaltfläche ([]. /media/reportviewerc130389.png)]". /media/reportviewerc130389.png)         | Starten Sie den Report-Viewer, und zeigen Sie die neueste Version des generierten Berichts an. Diese Schaltfläche ist aus einer Berichtsdefinition verfügbar, wenn mindestens einen Bericht generiert wurde. |
| []( Berichtsschaltfläche ![erfolgen . /media/generate-to-ddvc130389.png)]". /media/generate-to-ddvc130389.png) | Generieren Sie einen Bericht aus der aktiven Berichtsdefinition. Diese Schaltfläche ist aus einer Berichtsdefinition verfügbar.                                                                      |



<a name="see-also"></a>Siehe auch
--------

[Finanzberichterstellung in Microsoft Dynamics ERP](financial-reporting-intro.md)

[Generate a financial report](\financials\general-ledger\generate-financial-report.md)


