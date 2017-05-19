---
title: Berichts-Designer-Schnittstelle
description: "Dieser Artikel erläutert das Navigieren durch den Berichtsdesigner und wie Sie die verschiedenen Optionen Ihren Bedürfnissen entsprechend verwenden."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: ShylaThompson
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 59041
ms.assetid: 054de5b0-8618-4195-be12-f031b4bb4d74
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 3a82d877b2fb87eef6f2b16d528ed42debbb2874
ms.contentlocale: de-de
ms.lasthandoff: 04/25/2017


---

# <a name="report-designer-interface"></a>Berichts-Designer-Schnittstelle

[!include[banner](../includes/banner.md)]


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
| Bericht anzeigen                       | Öffnen Sie die neueste Version des generierten Berichts in Dynamics 365 for Operations. Dieser Befehl ist aus einer Berichtsdefinition verfügbar, wenn mindestens einen Bericht generiert wurde.                                 |
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
| Dimensionssatzhierarchie einfügen         | Öffnen Sie das Dialogfeld **Dimensionssatzhierarchie**, in dem Sie eine Dimensionssatzhierarchie aus den Finanzdaten importieren können. Dieser Befehl ist von einer Berichtsbaumstruktur-Definition oder für ein ..\financial-dimensions\dimension-based System verfügbar.  |
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
| Hilfe    | Öffnen der Dynamics 365 for Operations Hilfe-Themen-Seite für die Finanzberichterstellung. |
|         |                                                              |

## <a name="report-designer-toolbar-buttons"></a>Symbolleistenschaltflächen des Bericht-Designers
Die folgenden Tabellen beschreiben die Schaltflächen der Symbolleiste, die Sie verwenden können, wenn Sie Berichte entwerfen. Einige Schaltflächen der Symbolleiste sind nur unter bestimmten Umständen verfügbar. Beispielsweise sind Schaltflächen für das Höherstufen und das Tieferstufen von Berichtseinheiten nur verfügbar, wenn Sie eine Berichtsbaumstruktur-Definition ändern.

### <a name="standard-toolbar"></a>Standardsymbolleiste

Die Standardsymbolleiste bieten schnellen Zugriff auf Datei- und Bearbeiten-Befehle. Diese Symbolleiste enthält die folgenden Schaltflächen.

| Schaltfläche                                                                                                                                                                                   | Beschreibung                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [![Neue Schaltfläche](./media/rowc130389.png)](./media/rowc130389.png)                              | Erstellen Sie eine neue (leere) Berichtsdefinition, Zeilendefinition, Spaltendefinition oder Berichtsbaumstruktur-Definition.                                                                               |
| [![Schaltfläche "Öffnen"](./media/openfolderc130389.png)](./media/openfolderc130389.png)               | Öffnen Sie eine vorhandene Zeilendefinition, eine Spaltendefinition, eine Berichtsbaumstruktur-Definition oder eine Berichtsdefinition.                                                                                   |
| [![Schaltfläche "Speichern"](./media/savec130389.png)](./media/savec130389.png)                           | Speichern Sie die aktuelle Zeilendefinition, Spaltendefinition, Berichtsbaumstruktur-Definition oder Berichtsdefinition.                                                                                   |
| [![Schaltfläche "Kopieren"](./media/copyc130389.png)](./media/copyc130389.png)                           | Kopiert den ausgewählten Text in die Zwischenablage.                                                                                                                                               |
| [![Schaltfläche "Ausschneiden"](./media/cutc130389.png)](./media/cutc130389.png)                              | Ausgewähltes Element kopieren und der Zwischenablage hinzufügen.                                                                                                                                |
| [![Schaltfläche "Einfügen"](./media/pastec130389.png)](./media/pastec130389.png)                        | Fügen Sie den Text aus der Zwischenablage ein.                                                                                                                                                    |
| [![Schaltfläche "Rückgängig"](./media/undoc130389.png)](./media/undoc130389.png)                           | Letzte Aktivität rückgängig machen.                                                                                                                                                                  |
| [![Schaltfläche "Wiederherstellen"](./media/redoc130389.png)](./media/redoc130389.png)                           | Rückgängigmachen der letzten Aktivität stornieren.                                                                                                                                                          |
| [![Schaltfläche "Suchen"](./media/findc130389.png)](./media/findc130389.png)                           | Öffnen Sie das Dialogfeld **Suchen und ersetzen**, in dem Sie Text im aktiven Fenster suchen und ersetzen können.                                                                                  |
| [![Schaltfläche "Zeile einfügen"](./media/insertrowc130389.png)](./media/insertrowc130389.png)           | Fügen Sie eine leere Zeile in die Zeilendefinition oder eine leere Kopfzeile in die Spaltendefinition ein. Diese Schaltfläche ist von einer Zeilendefinition oder aus einer Spaltendefinition aus verfügbar.                    |
| [![Schaltfläche "Spalte einfügen"](./media/insertcolumnc130389.png)](./media/insertcolumnc130389.png)  | Fügen Sie eine leere Spalte in die Spaltendefinition ein. Diese Schaltfläche ist aus einer Spaltendefinition verfügbar.                                                                                  |
| [![Schaltfläche "Sperren"](./media/lockc130389.png)](./media/lockc130389.png)                           | Wenden Sie ein Kennwort auf den aktuellen Baustein an. Diese Schaltfläche ist für Benutzer mit der **Designer**-Rolle oder der **Administrator**-Rolle verfügbar.                                                 |
| [![Schaltfläche "Zeilenlink"](./media/rowlinkc130389.png)](./media/rowlinkc130389.png)                 | Öffnen Sie das Dialogfeld **Zeilenlinks**, in dem Sie die Quellen für Datenverbindungen in Zeilendefinitionen und in den Berichtsbaumstruktur-Definitionen angeben können. Diese Schaltfläche ist aus einer Zeilendefinition verfügbar. |
| [![Schaltfläche "Höherstufen"](./media/promotec130389.png)](./media/promotec130389.png)                  | Stufen Sie eine Einheit der Berichtsbaumstruktur-Definition hoch. Wenn Sie eine untergeordnete Einheit auswählen und dann auf **Höherstufen** klicken, wird die untergeordnete Einheit auf die Ebene der übergeordneten Einheit verschoben.                |
| [![Schaltfläche "Tieferstufen"](./media/demotec130389.png)](./media/demotec130389.png)                     | Stufen Sie eine Einheit der Berichtsbaumstruktur-Definition herunter. Wenn Sie eine Einheit auswählen und dann auf **Tieferstufen** klicken, wird die Einheit zu einem untergeordneten Element der vorangehenden Einheit.                               |
| [![Schaltfläche "Erweitern"](./media/expandtreebuttonc130389.png)](./media/expandtreebuttonc130389.png) | Erweitern Sie alle Einheiten der Berichtsbaumstruktur-Definition auf der Ebene der ausgewählten Einheit.                                                                                                   |
| [![Schaltfläche "Reduzieren"](./media/collapsec130389.png)](./media/collapsec130389.png)               | Reduzieren Sie die Berichtsbaumstruktur.                                                                                                                                                           |
| [![Schaltfläche "Hilfe"](./media/helpc130389.png)](./media/helpc130389.png)                           | Hilfe öffnen.                                                                                                                                                                             |

### <a name="formatting-toolbar"></a>Formatsymbolleiste

Die Formatierungssymbolleiste bietet einfachen Zugriff auf Formatbefehle. Diese Symbolleiste enthält die folgenden Schaltflächen.

| Schaltfläche                                                                                                                                                                                                   | Beschreibung                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| [![Schaltfläche "Schriftschnitt"](./media/formattingc130389.png)](./media/formattingc130389.png)                         | Hiermit können Sie den ausgewählten Schriftschnitt auf den aktuellen Text anwenden.      |
| [![Schaltfläche "Schriftart"](./media/fonttype.png)](./media/fonttype.png)                                                 | Legen Sie die ausgewählte Schriftart für den aktuellen Text fest.              |
| [![Schaltfläche "Schriftgröße"](./media/fontsize.png)](./media/fontsize.png)                                            | Legen Sie die ausgewählte Schriftgröße (in Punkten) für den aktuellen Text fest. |
| [![Schaltfläche "Fett"](./media/boldc130389.png)](./media/boldc130389.png)                                           | Hebt den aktuellen Text fett hervor.                             |
| [![Schaltfläche "Kursiv"](./media/italicsc130389.png)](./media/italicsc130389.png)                                   | Hebt den aktuellen Text kursiv hervor.                           |
| [![Schaltfläche "Unterstreichen"](./media/underlinec130389.png)](./media/underlinec130389.png)                            | Unterstreicht den aktuellen Text.                             |
| [![Schaltfläche "Einrückung verringern"](./media/outdentlsc130389.png)](./media/outdentlsc130389.png)                      | Verkleinern Sie die Einzugsebene des aktuellen Texts.                |
| [![Schaltfläche "Einrückung vergrößern"](./media/indentlsc130389.png)](./media/indentlsc130389.png)                        | Vergrößern Sie die Einzugsebene des aktuellen Texts.                |
| [![Schaltfläche "Hintergrundfarbe"](./media/fillbackgroundcolorc130389.png)](./media/fillbackgroundcolorc130389.png) | Ändern Sie die Hintergrundfarbe der aktuellen Zelle        |
| [![Schaltfläche "Schriftfarbe"](./media/fontcolorc130389.png)](./media/fontcolorc130389.png)                           | Ändern Sie die Farbe des aktuellen Texts.                   |

### <a name="report-designer-toolbar"></a>Symbolleisten des Bericht-Designers

Die Berichtsdesigner-Symbolleiste bietet Schnellzugriff auf Befehle für das Navigieren innerhalb des Berichtsdesigners. Diese Symbolleiste enthält die folgenden Schaltflächen.

| Schaltfläche                                                                                                                                                                                          | Beschreibung                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [![Schaltfläche "Berichtsdefinition"](./media/reportc130389.png)](./media/reportc130389.png)                 | Hier wird die Berichtsdefinition angezeigt, die im Menü **Fenster** aufgeführt ist.                                                                                                            |
| [![Schaltfläche "Zeilendefinition"](./media/rowc130389.png)](./media/rowc130389.png)                          | Hier wird die Zeilendefinition angezeigt, die der aktiven Berichtsdefinition zugewiesen ist.                                                                                                    |
| [![Schaltfläche "Spaltendefinition"](./media/columnc130389.png)](./media/columnc130389.png)                 | Hier wird die Spaltendefinition angezeigt, die der aktiven Berichtsdefinition zugewiesen ist.                                                                                                 |
| [![Schaltfläche "Berichtsbaumstruktur-Definition"](./media/treec130389.png)](./media/treec130389.png)             | Hier wird die Berichtsbaumstruktur-Definition angezeigt, die der aktiven Berichtsdefinition zugewiesen ist.                                                                                         |
| [![Report-Viewer-Schaltfläche](./media/reportviewerc130389.png)](./media/reportviewerc130389.png)         | Starten Sie den Report-Viewer, und zeigen Sie die neueste Version des generierten Berichts an. Diese Schaltfläche ist aus einer Berichtsdefinition verfügbar, wenn mindestens einen Bericht generiert wurde. |
| [![Schaltfläche "Bericht generieren"](./media/generate-to-ddvc130389.png)](./media/generate-to-ddvc130389.png) | Generieren Sie einen Bericht aus der aktiven Berichtsdefinition. Diese Schaltfläche ist aus einer Berichtsdefinition verfügbar.                                                                      |



<a name="see-also"></a>Siehe auch
--------

[Finanzberichterstellung](financial-reporting-intro.md)

[Finanzbericht generieren](generate-financial-report.md)




