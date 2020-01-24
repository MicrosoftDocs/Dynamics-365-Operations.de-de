---
title: Die Benutzerumgebung personalisieren
description: In diesem Thema wird erläutert, wie Sie die App personalisieren können.
author: jasongre
manager: AnnBe
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserSetup, DefaultDashboard
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 62363
ms.assetid: 57b445d7-3e9e-4228-8728-f63b9dbd77a3
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ac8f154fdf892553f69d135727589bf13efd6076
ms.sourcegitcommit: 34395464ec80cea800b953eae49af579d436fc1b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2020
ms.locfileid: "2935464"
---
# <a name="personalize-the-user-experience"></a>Die Benutzerumgebung personalisieren

[!include [banner](../includes/banner.md)]

In diesem Thema wird erläutert, wie Sie die App personalisieren können.

Es gibt drei grundlegende Klassen der Personalisierungen.

- Personalisierungen, die auf einer Einrichtungsseite vorgenommen werden. Hierzu gehören das Farbenthema und Zeitzone.
- Personalisierungen, die sich auf die Seitennutzung beziehen. Diese Personalisierungen nennt man *implizite* Personalisierungen. So verfolgt das System beispielsweise die Breite von Rasterspalten, wenn Sie sie anpassen sowie den erweiterten/reduzierten Status von Inforegistern.
- Personalisierungen, die ein Benutzer an der Darstellung einer Seite vornimmt, indem er ändert, wie Elemente auf der Seite angezeigt werden oder agieren, häufig in einem interaktiven Personalisierungsmodus. Diese Personalisierungen nennt man *explizite* Personalisierungen. Zum Beispiel kann der Benutzer Elemente auf der Seite hinzuzufügen, ausblenden oder neu anordnen.

Sämtliche Personalisierungen, die ein Benutzer vornimmt, gelten nur für diesen Benutzer, unabhängig von dem Unternehmen, mit dem der Benutzer interagiert. Änderungen, die ein Benutzer an einer Seite vornimmt, haben keine Auswirkungen auf andere Benutzer im System.

## <a name="system-wide-options-for-the-current-user"></a>Systemweite Optionen für den aktuellen Benutzer

Die Seite **Benutzeroptionen** enthält mehrere systemweite Einstellungen für den aktuellen Benutzer. Um die Seite **Benutzeroptionen** zu öffnen, wählen Sie die Schaltfläche **Einstellungen** (Zahnradsymbol) auf der Navigationsleiste, und wählen Sie dann **Benutzeroptionen**. Die Seite **Benutzeroptionen** besitzt vier Registerkarten, die verschiedene Benutzereinstellungen enthalten:

- **Visuell:** - Wird verwendet, um ein Farbenthema und die standardmäßige Größe der Elemente auf den Seiten auszuwählen.
- **Einstellungen** – Wählen Sie Standardwerte, die bei jedem Planungslauf verwendet werden, die Sie im System öffnen. Diese Werte umfassen das Unternehmen, die erste Seite und die Standardansicht/den Bearbeitungsmodus. (Anzeigen/Bearbeitungsmodus der bestimmt, ob eine Seite zum Anzeigen gesperrt ist oder diese zum Bearbeiten jedes Mal geöffnet wird, wenn Sie sie öffnen.) Diese Registerkarte enthält Optionen für die Sprache, die Zeitzone und das Datum, die Uhrzeit und Zahlenformate. Und schließlich enthält die Registerkarte unterschiedliche Einstellungen von Version zu Version.
- **Konto** - Verwenden, um Benutzer-ID und andere Konten bezogene Optionen anzugeben.
- **Workflow** – Wählen Sie workflowbezogene Optionen aus.

Neben der Bearbeitung der Benutzereinstellungen können Sie Ihre Nutzungsdaten und Personalisierungen auch anzeigen und löschen, indem Sie die Seite **Benutzeroptionen** verwenden. Wählen Sie einfach im Aktivitätsbereich **Nutzungsdaten** aus.

Wenn Sie die Anwendung verwenden, werden viele Ihrer Einstellungen gespeichert, damit die Nutzung des Systems beim nächsten Mal für Sie einfacher wird. Auf der Registerkarte **Personalisierung** können Sie persönliche Änderungen anzeigen und verwalten, die Sie im System an Seiten vorgenommen haben. Auf dieser Registerkarte können Sie auch Funktionslegenden zurücksetzen (d.h. die Popup-Fenster, die neue Systemfunktionen einführen). Sie werden dann erneut über zuvor aufgetretene Funktionen informiert.

> [!NOTE]
> Wenn die Funktion [Gespeicherte Ansichten](saved-views.md) aktiviert ist, können Sie die Personalisierungen anzeigen und verwalten, indem Sie **Personalisierung** im Aktivitätsbereich auf der Seite **Benutzeroptionen** auswählen.

## <a name="implicit-personalizations"></a>Implizite Personalisierungen

Implizite Personalisierungen sind die Personalisierungen, die Sie ausführen, indem Sie einfach mit bestimmten Steuerelementen interagieren, die ihren aktuell sichtbaren Status speichern.

- **Rasterspalten:** - Sie können die Breite einer Spalte in einer Liste anpassen, indem Sie die Größenänderungsleiste links oder rechts des Spaltenkopfs auswählen und sie nach links oder rechts auf die gewünschte Breite schieben. Die App speichert die Breite, die Sie festlegen,m in einer Spalte. Beim nächsten Öffnen der Seite, die dieses Raster enthält, wird die Breite dieser Spalte an diese Größe angepasst.
- **Inforegister** – Einige Seiten haben erweiterbare Abschnitte, die als *Inforegister* bezeichnet werden. Die App speichert Informationen über die Inforegister, die Sie erweitert und reduziert haben. Beim nächsten Mal, wenn Sie zu der Seite zurückkehren, werden die gleichen Inforegister erweitert oder reduziert, basierend auf Ihrer letzten Interaktion mit der Seite. In einigen Fällen verbessert das Reduzieren eines Inforegisters die Leistung, da die App diese Informationen für Inforegister erst abruft, wenn die Inforegister erweitert werden. Wie später in diesem Thema erläutert, können Sie die Reihenfolge der Inforegister einer Seite auch ändern.
- **Infoboxen** – Einige Seiten haben einen Bereich **Zugehörige Informationen**, der schreibgeschützte Informationen enthält, die dem aktuell zugeordneten Betreff der Seite zugeordnet sind. Jeder Abschnitt im Bereich **Zugehörige Informationen** wird als *Infobox* bezeichnet. Sie können den Bereich **Zugehörige Informationen** erweitern oder reduzieren, und Sie können auch einzelne Infoboxen erweitern oder reduzieren. Die App speichert diese Einstellungen. Anschließend werden das nächste Mal, wenn Sie die Seite öffnen, der Bereich **Zugehörige Informationen** und die einzelnen Infoboxen, basierend auf Ihrer letzten Interaktion mit der Seite erweitert oder reduziert. In einigen Fällen verbessert das Reduzieren einer Infobox die Leistung, da die App diese Informationen für Infoboxen erst abruft, wenn die Infoboxen erweitert werden.
- **Aktivitätsbereiche** – *Aktivitätsbereich* Wird meistens oben an den meisten Seiten angezeigt. Der Aktivitätsbereich enthält Schaltflächen für viele der Aktivitäten, die auf der aktuellen Seite ausgeführt werden können. Diese Schaltflächen werden häufig auf Registerkarten zusammengefasst. Sie können den gesamten Aktivitätsbereich öffnen, oder Sie können ihn standardmäßig reduzieren lassen. Beim nächsten Mal, wenn Sie zu der Seite zurückkehren, wird der Aktivitätsbereich entweder geöffnet oder reduziert, basierend auf Ihrer letzten Interaktion mit der Seite. Wenn Sie den Aktivitätsbereich als geöffnet fixiert haben, wird die letzte Registerkarte angezeigt, die Sie verwendet haben.
- **QuickFilters** – *QuickFilter* erscheint oberhalb vieler Raster. Mit QuickFilter können Sie Raster filtern, basierend auf einer Spalte, die Sie auswählen. Die App speichert die Spalte, die Sie gefiltert haben. Wenn Sie das nächste Mal die Seite öffnen, die dieses Raster enthält, ist der Raster in derselben Spalte gefiltert. Sie können jedoch dann eine andere Spalte auswählen, um das Raster zu filtern.
- **Spaltenüberschriftfilter** – Wenn Sie ein Raster filtern, indem Sie *Spaltenüberschriftfilter* verwenden, können Sie den Filteroperator ändern, wie Sie ihn benötigen, um die Daten zu suchen, die Sie wünschen. Beispielsweise können Sie den gewünschten Operator von **beginnt mit** in **ist genau** ändern. Immer wenn Sie einen Spaltenüberschriftfilter verwenden und den Filteroperator ändern, speichert die App die Änderung. Sie stellt dann den Filteroperator das nächste Mal wieder her, wenn Sie diese Spalte filtern.
- **Navigationsbereich** – Sie können den *Navigationsbereich* öffnen, indem Sie die Schaltfläche **Den Navigationsbereich erweitern** im oberen linken Bereich der Seite auswählen. (Die Schaltfläche _**Menü**_ wird auch als *Hamburger*, *Hamburgermenü* oder *Hamburgerschaltfläche* bezeichnet). Sie können den offenen Navigationsbereich anheften, oder Sie können ihn standardmäßig reduziert anzeigen. Nachdem Sie den Navigationsbereich als offen angeheftet haben, bleibt die App offen, bis Sie ihn wieder reduzieren.

## <a name="explicit-personalizations"></a>Explizite Personalisierungen

Verschiedene Personen und Unternehmen haben eine unterschiedliche Perspektive auf die Daten, die Ihnen am wichtigsten sind, oder die Daten, die sie nicht für die Art benötigen, wie sie ihr Geschäft ausführen. Sie können die Art und Weise definieren, wie Ihre Informationen bestellt und verarbeitet werden. Sie können auch angeben, dass einige Informationen ausgeblendet werden sollen. Diese Funktionen sind zentral für eine persönliche und produktive Erfahrung und sind entscheidend für eine explizite Personalisierung. Explizite Personalisierungen sind Personalisierungen, die Sie explizit machen mit der Absicht, die Darstellungsweise oder das Verhalten eines Elements oder der Seite zu ändern, indem Sie ein Personalisierungsmenü auswählen.

### <a name="shortcut-menu-options"></a>Verknüpfungsmenüoptionen

Ein Kontextmenü enthält mehrere Möglichkeiten, explizit eine Seite zu ändern, um den Anforderungen und Bedürfnissen Ihres Unternehmens zu entsprechen. (Wird auch als *Rechtsklickmenü* oder *Kontextmenü* bezeichnet).

Einige der typischsten und wichtigsten Änderungen, die Sie an einer Seite vornehmen können, sind direkt als Optionen für ein Kontextmenü verfügbar. Zum Beispiel ist es ab Platform Upate 17 möglich, um eine Spalte in einem Raster ein- oder auszublenden, auf eine Rasterspaltenüberschrift mit der rechten Maustaste zu klicken. Wählen Sie dann **Hinzufügen von Spalten** oder **Ausblenden der Spalte** aus.

Darüber hinaus sind die Typen der grundlegendsten expliziten Personalisierung verfügbar, indem Sie auf ein Element mit der rechten Maustaste klicken und dann **Anpassen** auswählen. (Beachten Sie, dass nicht alle Elemente auf der Seite personalisiert werden können.) Wenn Sie diese Methode der Personalisierung auswählen, wird das Eigenschaftenfenster des Elements angezeigt.

![Personalisieren der Eigenschaften eines Elements](./media/personalization-element-properties.png)

Sie können das Eigenschaftenfenster verwenden, um ein Element in folgender Hinsicht zu personalisieren:

- Ändern Sie die Bezeichnung des Elements.
- Verbergen Sie das Element, damit es nicht auf der Seite angezeigt wird. Die Daten im Feld werden nicht gelöscht oder geändert. Die derzeitigen Informationen werden nicht mehr auf der Seite angezeigt.
- Schließt die zusammengefassten Informationen im Bereich des Inforegisters ein (falls das Element in einem Inforegister ist).
- Überspringen Sie das Feld, sodass es beim Blättern durch die Seite nie den Fokus erhält.
- Verhindern Sie, dass Daten im Feld (für einen beliebigen Datensatz) bearbeitet werden.

Das Eigenschaftenfenster kann andere Personalisierungsfunktionen enthalten, abhängig vom Element. Beispielsweise können Sie mit dem Eigenschaftenfenster für eine Kachel diese Kachel in einem Dashboard höher stufen, und das Eigenschaftenfenster für das Dashboard lässt Sie möglicherweise einen neuen Arbeitsbereich auf diesem Dashboard erstellen.

### <a name="the-personalization-toolbar"></a>Personalisierungssymbolleiste

Wenn Sie mehrere Änderungen auf einer Seite oder Änderungen vornehmen möchten, die über keinen anderen Mechanismen (z. B. Elemente neu anordnen) verfügbar sind, können Sie die Symbolleiste **Personalisierung** verwenden. Um die Symbolleiste **Personalisierung** zu öffnen, führen Sie die folgenden Schritte aus:

- Wählen Sie **Dieses Formular personalisieren** im Eigenschaftenfenster eines Elements aus.
- Wählen Sie im Aktivitätsbereich einer Seite in der Registerkarte **Optionen** in der Gruppe **Personalisieren** die Option **Diese Seite personalisieren** aus.
- Wählen Sie die Schaltfläche **Einstellungen** (Zahnradsymbol) auf der Navigationsleiste und wählen Sie dann **Anpassen**.

[![Personalisierungssymbolleiste](./media/restyledPersonalizationToolbar.png)](./media/restyledPersonalizationToolbar.png)

#### <a name="navigating-the-page"></a>Navigieren auf de Seite

Wenn die Symbolleiste **Personalisierung** geöffnet ist, ist die zugrunde liegende Seite schreibgeschützt (in anderen Worten, Sie können die Daten nicht bearbeiten), ist jedoch noch interaktiv. Sie können insbesondere den Bereich **Zugehörige Informationen** erweitern oder reduzieren, zwischen Registerkarten wechseln und Abschnitte erweitern oder reduzieren, ebenso Sie normalerweise die Aktivitäten auf der Seite ausführen. Um eine Personalisierungsänderung auf einen reduzierten Bereich oder eine Registerkarte anzuwenden (z. B. ein Inforegister ausblenden), müssen Sie nur die Schaltfläche auswählen, die neben dem Abschnitt oder der Registerkarte angezeigt wird, wenn sie Tastaturfokus erhält oder wenn Sie darüber fahren.

#### <a name="personalization-tools"></a>Personalisierungswerkzeuge

Folgende Tools sind auf der Symbolleiste **Benutzereinstellungen** verfügbar:

- Nutzen Sie das Werkzeug **Auswählen**, um Eigenschaften eines Elements auszuwählen und zu ändern. Um dieses Tool zu verwenden, aktivieren Sie die Schaltfläche **Auswählen** auf der Symbolleiste, und wählen Sie dann das gewünschte Element aus. Das Eigenschaftenfenster des Elements wird geöffnet, und Sie können beliebige Eigenschaften für dieses Element ändern. Sie können den Prozess für andere Elemente auf der Seite wiederholen, die personalisierbar sind. Beachten Sie, dass einige Personalisierungseigenschaften möglicherweise nicht in einigen Szenarien verfügbar sind. Sie können beispielsweise kein Feld sperren, das erforderlich ist.
- Wählen Sie das Tool **Ausblenden**, um ein Element auf der Seite auszublenden. Um dieses Tool zu verwenden, aktivieren Sie die Schaltfläche **Ausblenden** auf der Symbolleiste, und wählen Sie dann das gewünschte Element aus, das ausgeblendet werden soll. Wenn Sie das Tool **Ausblenden** verwenden, werden alle Elemente, die gerade ausgeblendet werden, in einem schattierten Container angezeigt. Sie können anschließend ein Element sichtbar machen, indem Sie es auswählen. Um zu sehen, wie die Seite aussehen wird, wenn Elemente ausgeblendet sind, wechseln Sie zu einem anderen Personalisierungstool.
- Wählen Sie das Tool **Ein Feld hinzufügen**, um ein Feld zur Seite hinzuzufügen. Wenn Sie dieses Tool verwenden, können Sie nur Felder hinzufügen, die Teil der Seitendefinition sind. Informationen zum Erstellen neuer Felder, die nicht Teil der aktuellen Seitendefinition sind, finden Sie unter [Erstellen und Arbeiten mit benutzerdefinierten Feldern](user-defined-fields.md). Nachdem Sie die Schaltfläche **Feld hinzufügen** auf der Symbolleiste ausgewählt haben, müssen Sie die Gruppe oder den Bereich zunächst aktivieren, dem Sie ein Feld hinzufügen möchten. Ein Dialogfeld wird in der Liste der Felder angezeigt, die der Gruppe oder dem Bereich zugeordnet sind, den Sie ausgewählt haben. Wählen Sie im Dialogfeld mindestens ein Feld aus und wählen Sie **Einfügen**en Benutzer oder mindestens eine Gruppe aus. Wenn Sie ein Feld entfernen, das Sie zuvor hinzugefügten haben, wiederholen Sie den Vorgang aber deaktivieren Sie die Option im Dialogfeld.
- Wählen Sie das Tool **Umlagern** aus, wenn Sie ein Element auswählen und an einen anderen Lagerplatz innerhalb der aktuellen Elementgruppe umlagern möchten. Sie können kein Element außerhalb seiner übergeordneten Gruppe verschieben. Um dieses Tool zu verwenden, aktivieren Sie die Schaltfläche **Umlagern** auf der Symbolleiste, und wählen Sie dann das gewünschte Element aus, das umgelagert werden soll. Wenn Sie ein Element auswählen, überprüft die App die Standorte, an die das Element verschoben werden kann. Diese Lagerplätze werden als *Abstiegszonen* bezeichnet. Da Sie das Element innerhalb der aktuellen Gruppe ziehen, wird jede Abstiegszone als farbige, fette Position neben dem Bereich angezeigt, in dem das Element abgelegt werden kann.
- Wählen Sie das **Überspringen** Tool, um ein Element aus der Tastaturtabulatorsequenz der Seite zu entfernen. Wenn Sie die Schaltfläche **Überspringen** auf der Symbolleiste auswählen, werden alle Elemente, die gerade ausgeblendet werden, in einem schattierten Container angezeigt. Sie können Felder der Tabulatorsequenz interaktiv entfernen oder hinzufügen.
- Verwenden Sie das Tool **In Kopfzeile anzeigen**, wenn ein Feld im Zusammenfassungsbereich des Inforegisters angezeigt werden soll. Wenn Sie die Schaltfläche **In Kopfzeile anzeigen** auf der Symbolleiste auswählen, werden alle Felder, die als Zusammenfassungsfelder ausgewählt wurden, in einem schattierten Container angezeigt. Sie können Felder der Inforegisterzusammenfassung interaktiv hinzufügen und Felder daraus entfernen, indem Sie die Felder auswählen.
- Wählen Sie das Tool **Sperren** aus, wenn Sie ein Element als „Bearbeitbar“ oder „Nicht bearbeitbar“ markieren wollen. Wenn Sie die Schaltfläche **Sperren** auf der Symbolleiste auswählen, werden alle Elemente, die gerade nicht bearbeitbar sind, in einem schattierten Container angezeigt. Sie können definieren, dass sie wieder geändert werden können. Beachten Sie: Mehrere Felder sind obligatorisch und können nicht als nicht bearbeitbar festgelegt werden. Ein Schlosssymbol wird neben den Feldern angezeigt.
- Verwenden Sie die Schaltfläche **PowerApp hinzufügen**, um eine App einzufügen, die unter Microsoft PowerApps auf der Seite erstellt wurde. Detaillierte Informationen zum Einbetten einer PowerApps App in eine Seite finden Sie unter [Einbetten von PowerApps Apps](embed-power-apps.md).
- Verwenden Sie das Tool **Löschen**, um die Seite auf den Standard, also den installierten Standard zurückzusetzen. Alle Personalisierungen auf der aktuellen Seite werden gelöscht. Es gibt keine rückgängig gemachte Aktion. Daher verwenden Sie dieses Tool nur, wenn Sie sicher sind, dass Sie die Seite zurücksetzen möchten.
- Verwenden Sie das Tool **Importieren**, um eine Personalisierung aus einer Datei zu verwenden, die Sie oder eine andere Person zuvor erstellt haben. Wenn Sie Personalisierungen für eine Seite importieren, können Sie auswählen, ob sie hinzugefügt werden oder die vorhandenen Personalisierungen für die Seite ersetzen sollen. Es gibt keine rückgängig gemachte Aktion. Daher nachdem Sie Personalisierungen importieren, müssen Sie oder Änderungen, die Sie nicht möchten, manuelle rückgängig machen oder löschen.
- Verwenden Sie das Tool **Exportieren**, um die Personalisierungen für die Seite in einer Datei zu speichern. Sie können Ihre Personalisierungen mit anderen Benutzern teilen. Diese Benutzer müssen nur die Datei importieren, die für Ihre Personalisierungen die Seite enthält.
- Wählen Sie die Schaltfläche **Schließen**, um die Symbolleiste **Personalisieren** zu schließen und den vorherigen interaktiven Status zurückzuversetzen.

Traditionsgemäß wenn die Symbolleiste **Personalisierung** verwendet wird, werden die Personalisierungen wirksam, sobald Sie diese erstellen. Ist jedoch die Funktion [Gespeicherte Ansichten](saved-views.md) aktiviert, müssen Sie Personalisierungen explizit in einer Ansicht speichern, die Sie auswählen.

Manchmal finden Sie ein Schlosssymbol neben einem Element, wenn Sie ein Tool auswählen. Dieses Symbol zeigt an, dass Sie die Elementeigenschaften nicht ändern können, die dem ausgewählten Tool zugeordnet sind, da sich die vorgenommenen Änderungen auf den Eigenschaften verhindern, dass die Seite ordnungsgemäß funktioniert.

### <a name="adding-a-tile-list-or-link-to-a-workspace"></a>Hinzufügen einer Kachel oder Liste zu einem Arbeitsbereich

Für mehrere Seiten, die Listen enthalten, ist die Personalisierungsfunktion **Zum Arbeitsbereich hinzufügen** in der Gruppe **Anpassen** auf der Registerkarte **Optionen** im Aktivitätsbereich verfügbar. Diese Funktion lässt Sie die relevanten Informationen für die aktuelle Liste in einen bestimmten Arbeitsbereich übertragen. Die Informationen, die im Arbeitsbereich angezeigt werden, können auf der gesamten Liste oder einer gefilterten und sortierten Version der Liste basieren. Sie können auch angeben, ob die Informationen im Arbeitsbereich als Liste, als zusammenfassende Kachel, die die Anzahl der Elemente in der Liste anzeigt, oder als Link angezeigt wird.

> [!NOTE]
> Wenn die Funktion [Gespeicherte Ansichten](saved-views.md)-aktiviert wird, wird der Inhalt, den Sie an einen Arbeitsbereich übertragen, direkt mit einer Ansicht verknüpft. Die Abfrage der Ansicht wird verwendet, um Daten im Arbeitsbereich abzurufen, und die entsprechende Kachel oder der Link im Arbeitsbereich öffnet die Seite zu dieser Ansicht, sodass die Abfrage und die Personalisierungen der Ansicht auf sie angewendet werden.

[![Zum Arbeitsbereich hinzufügen](./media/personalization-addtoworkspace.png)](./media/personalization-addtoworkspace.png)

- Um eine Liste einem Arbeitsbereich hinzuzufügen, sortieren oder filtern Sie zuerst die Liste auf der Seite, sodass die Informationen so angezeigt werden, wie Sie sie im Arbeitsbereich wünschen. (Wenn die gespeicherte Ansichtsfunktion aktiviert ist, können Sie nicht fortfahren, bis Sie eine Ansicht speichern, die den angegebenen Bedingungen entspricht.) Wählen Sie dann **Zum Arbeitsbereich hinzufügen** aus. Wählen Sie einen Arbeitsbereich und dann im Feld **Präsentation** wählen Sie **Liste** aus. Nachdem Sie **Konfigurieren** auswählen, wird ein Dialogfeld angezeigt, wo Sie die Spalten auswählen können, die in der Liste im Arbeitsbereich angezeigt werden sollen. Sie können auch die Beschriftung definieren, die für die Liste im Arbeitsbereich verwendet wird.
- Um eine Kachel zu einem Arbeitsbereich hinzuzufügen, filtern Sie zuerst die Liste auf der Seite, um die Daten darzustellen, die Sie zusammenfassen möchten (oder schnellen Zugriff darauf wünschen). (Wenn die gespeicherte Ansichtsfunktion aktiviert ist, können Sie nicht fortfahren, bis Sie eine Ansicht speichern, die den angegebenen Bedingungen entspricht.) Wählen Sie dann **Zum Arbeitsbereich hinzufügen** aus. Wählen Sie einen Arbeitsbereich und dann im Feld **Präsentation** wählen Sie **Kachel** aus. Nachdem Sie **Konfigurieren** auswählen, wird ein Dialogfeld angezeigt, in dem Sie die Beschriftung angeben können, die für die Kachel im Arbeitsbereich zu verwenden ist. Sie können auch angeben, ob die Kachel eine Anzahl anzeigen soll. Nachdem Sie die Kachel dem Arbeitsbereich hinzugefügt haben, können Sie sie auswählen, um die aktuelle Seite über den Arbeitsbereich zu öffnen. Sie können anschließend die gefilterte Liste anzeigen, die der Kachel zugeordnet ist.
- Um einen Link einem Arbeitsbereich hinzuzufügen, filtern Sie zuerst die Liste auf der Seite, sodass Sie die Daten sehen, die für Sie interessant sind. (Wenn die gespeicherte Ansichtsfunktion aktiviert ist, können Sie nicht fortfahren, bis Sie eine Ansicht speichern, die den angegebenen Bedingungen entspricht.) Wählen Sie dann **Zum Arbeitsbereich hinzufügen** aus. Wählen Sie einen Arbeitsbereich und dann im Feld **Präsentation** wählen Sie **Link** aus. Nachdem Sie **Konfigurieren** auswählen, wird ein Dialogfeld angezeigt, in dem Sie die Beschriftung angeben können, die für Links im Arbeitsbereich zu verwenden ist. Sie können optional auch eine Beschriftung für einen neuen Abschnitt angeben, der diesen Link enthält.

Nachdem eine Liste, Kachel oder einen Link dem Arbeitsbereich hinzugefügt wurde, können Sie den Arbeitsbereich öffnen und die Element so anordnen, wie Sie dies wünschen.

### <a name="adding-a-summary-from-a-workspace-to-a-dashboard"></a>Hinzufügen einer Zusammenfassung von einem Arbeitsbereich zu einem Dashboard

Einige Arbeitsbereiche enthalten Zählkacheln (das heißt, Kacheln, die Zahlen enthalten) und Sie wollen möglicherweise diese Kacheln auch auf Ihrem Dashboard anzeigen. Klicken Sie in einem Arbeitsbereich auf eine Anzahlkachel mit der rechten Maustaste, wählen Sie **Anpassen** und anschließend im Eigenschaftenfenster der Kachel **An Dashboard anheften**. Das nächste Mal, wenn Sie zum ausgewählten Dashboard navigieren (und es aktualisieren), finden Sie die Zahl unter der Navigationskachel dieses Arbeitsbereichs. Sie können diese Anzahl auswählen, um direkt zu den Daten zu wechseln, die dargestellt werden.

### <a name="personalizing-your-dashboard"></a>Ihr Dashboard personalisieren

Das Dashboard ist oftmals die erste Seite, die beim Öffnen der App angezeigt wird. Sie können das Dashboard personalisieren, so dass lediglich dje Arbeitsbereichskacheln angezeigt werden, die Sie sehen möchten. Sie können die Kacheln auch neu anordnen, damit sie in der von Ihnen gewünschten Reihenfolge erscheinen, Ihren Arbeitsbereich mit den Navigationskacheln neu benennen oder eine komplett neue Arbeitsbereichskachel hinzufügen.

Um das Dashboard zu personalisieren, klicken Sie auf eine beliebige Kachel mit der rechten Maustaste, und wählen Sie dann das **Anpassen**-Eigenschaftenfenster, um die Kachel zu öffnen.

- Wenn Sie die ausgewählten Kachel ausblenden oder umbenennen möchten, können Sie diese Änderung direkt im Eigenschaftenfenster vornehmen.
- Wenn Sie die Kacheln im Arbeitsbereich neu anordnen möchten, wählen Sie **Dieses Formular personalisieren** im Eigenschaftenfenster aus, um die Symbolleiste **Personalisierung** zu öffnen. Sie können das Tool **Verschieben** verwenden, um die Kacheln neu anzuordnen.
- Wenn Sie eine neue Arbeitsbereichskachel hinzufügen möchten, wählen Sie im Eigenschaftenfenster **Arbeitsbereich hinzufügen** aus. Eine neue Arbeitsbereichkachel wird am unteren Rand das Dashboard erstellt. Sie können diese neue Arbeitsbereichkachel umbenennen, wenn Sie dies wünschen. Sie können, Kacheln, Listen und auch Links dem Arbeitsbereich hinzufügen wie im Abschnitt [Hinzufügen von Kacheln, Listen oder Links zu Arbeitsbereichen](#adding-a-tile-list-or-link-to-a-workspace) beschrieben.

## <a name="administration-of-personalizations"></a>Verwalten der Personalisierungen

Nach dem Personalisieren einer Seite können Sie die Personalisierungen mit anderen Benutzern teilen, indem Sie die personalisierte exportieren. Sie können dann die anderen Benutzer auffordern, die personalisierte Seite zu öffnen und die personalisierte Datei zu importieren. Alternativ können Sie die Personalisierungen an einen Benutzer geben, der Administratorrechte besitzt. Dieser Benutzer kann die Personalisierungsdatei für viele Benutzer gleichzeitig übernehmen.

Benutzer mit Administratorrechten können Personalisierungen auch für andere Benutzer auf der Seite **Personalisierung** verwalten.

Für Kunden, die die Funktion [Gespeicherte Ansichten](saved-views.md) nicht aktiviert haben, hat diese Seite vier Registerkarten:

- **Anwenden** - Sie können eine Personalisierung für einen oder mehrere Benutzer auswählen. Um eine Personalisierung für einen oder mehrere Benutzer anzuwenden, wählen Sie zuerst eine Rolle und Benutzer aus, die diese Rolle besitzen. Wählen Sie anschließend eine vorhandene Personalisierung aus, um die ausgewählten Benutzer zu übernehmen oder importieren Sie eine Personalisierung. Die Personalisierung wird geprüft und auf alle ausgewählten Benutzer angewendet, wenn diese die ausgewählte Seite das nächste Mal öffnen.
- **Löschen** – Sie können eine Seiten- oder Arbeitsbereichspersonalisierung für einen oder mehrere Benutzer löschen. Wählen Sie eine Seite oder einen Arbeitsbereich aus, um die Liste der Benutzer zu sehen, die diese Seite personalisiert haben. Anschließend wählen Sie die Benutzer, die für diese deaktivierte Seite oder Arbeitsbereich aus und wählen Sie **Löschen** aus. Alle Personalisierungen, die die ausgewählten Benutzer auf die ausgewählte Seite oder den ausgewählten Arbeitsbereich angewendet haben, werden gelöscht. Diese Aktion kann nicht rückgängig gemacht werden. Wenn eine Personalisierung für die Seite oder den Arbeitsbereich gespeichert wurde, dann kann die Personalisierung neu importiert werden.
- **Benutzer** – Wählen Sie einen Benutzer aus, um die Liste der Seiten anzuzeigen, die der Benutzer personalisiert hat. Sie können dann die Möglichkeit aktivieren oder deaktivieren, um zu bestimmen, ob der Benutzer Personalisierungen für bestimmte Seiten oder das gesamte System verwenden kann oder nicht. Sie können Personalisierungen auch löschen, importieren oder exportieren für diesen Benutzer. Darüber hinaus können Sie Funktionslegenden für den Benutzer zurücksetzen. In diesem Fall, wenn der Benutzer zuvor Popup-Fenster, die neue Funktionen einführen, abgelehnt hat, werden sie beim nächsten Mal, wenn der Benutzer auf diese Funktionen trifft, wieder angezeigt.
- **System** – Sie können temporär Personalisierungen im System für alle Benutzer deaktivieren. In diesem Fall werden alle Personalisierungen für alle Benutzer gelöscht und alle Seiten auf ihren Standardstatus zurückgesetzt. Wenn Sie die Personalisierungen später wieder reaktivieren, werden diese wieder angewendet. Sie können temporär alle Personalisierungen im System für alle Benutzer deaktivieren oder abschalten. Es gibt keine Möglichkeit, Personalisierungen wiederherzustellen, die gelöscht wurden. Deshalb müssen Sie vor diesem Schritt sicherstellen, dass Sie alle Personalisierungen exportiert haben, die Sie später importieren möchten.

Für Kunden, die die Funktion [Gespeicherte Ansichten](saved-views.md) aktiviert haben, hat diese Seite **Personalisierung** fünf Registerkarten:

- **Veröffentlichte Ansichten** – Diese Ansichten wurden für die Organisation veröffentlicht. Um die Benutzer zu ändern, an die sich diese Ansichten richten, können Sie die Sicherheitsrollen oder juristischen Personen ändern, die jeder Ansicht zugeordnet sind. Sie können mindestens eine veröffentlichte Ansicht exportieren oder löschen.
- **Unveröffentlichte Ansichten** – Diese Ansichten sind Vorlagenansichten, die in das System importiert wurden, aber noch nicht veröffentlicht wurden. Sie können diese Ansichten veröffentlichen, exportieren oder löschen.
- **Persönliche Ansichten** – Diese Ansichten wurden von den Benutzern im System erstellt. Sie können eine persönliche Ansicht für die Organisation veröffentlichen oder eine oder mehrere der Ansichten an andere Benutzer kopieren. Sie können diese Ansichten auch nach Bedarf exportieren oder löschen.
- **Benutzer** – Wählen Sie einen Benutzer aus, um die Liste der Seiten anzuzeigen, die der Benutzer personalisiert hat. Sie können dann die Möglichkeit aktivieren oder deaktivieren, um zu bestimmen, ob der Benutzer Personalisierungen für bestimmte Seiten oder das gesamte System verwenden kann oder nicht. Sie können Personalisierungen auch löschen, importieren oder exportieren für diesen Benutzer. Darüber hinaus können Sie Funktionslegenden für den Benutzer zurücksetzen. In diesem Fall, wenn der Benutzer zuvor Popup-Fenster, die neue Funktionen einführen, abgelehnt hat, werden sie beim nächsten Mal, wenn der Benutzer auf diese Funktionen trifft, wieder angezeigt.
- **System** – Sie können temporär Personalisierungen im System für alle Benutzer deaktivieren. In diesem Fall werden alle Personalisierungen für alle Benutzer gelöscht und alle Seiten auf ihren Standardstatus zurückgesetzt. Wenn Sie die Personalisierungen später wieder reaktivieren, werden diese wieder angewendet. Sie können temporär alle Personalisierungen im System für alle Benutzer deaktivieren oder abschalten. Es gibt keine Möglichkeit, Personalisierungen wiederherzustellen, die gelöscht wurden. Deshalb müssen Sie vor diesem Schritt sicherstellen, dass Sie alle Personalisierungen exportiert haben, die Sie später importieren möchten.

Benutzer, die Zugriff auf die Seite **Personalisierung** haben, können die persönlichen oder Vorlagenansichten auch importieren, indem sie die Schaltfläche **Ansichten importieren** im Aktivitätsbereich verwenden.

## <a name="personalizing-inventory-dimensions"></a>Personalisierung von Lagerungsdimensionen

Wenn Sie die Einstellungen der Lagerungsdimensionen auf einer Seite personalisieren, beachten Sie die Einstellungen, die erstellt wurden, indem Sie die Option **Anzeigendimension** nutzen. So verwenden Sie die Personalisierung, um eine Spalte für die Chargennummerenlagerungsdimension auszublenden, doch die Spalte erscheint das nächste Mal, wenn die Seite geöffnet wird. Dieses Verhalten tritt auf, da die Einstellungen die Lagerungsdimensionsspalten **Dimensionenanzeige** steuern, die angezeigt werden. Die **Dimensionsanzeigeeinstellungen** gelten für alle Seiten und diese Einstellungen setzen alle personalisierten Lagerdimensionsfelder einer individuellen Seite außer Kraft.

Wenn Sie wie im vorhergehenden Beispiel nicht möchten, dass die Spalte für die Chargennummerlagerungsdimension auf einer Seite erscheint, müssen Sie die Dimension als Teil der Option **Dimensionen anzeigen** für diese Seite deaktivieren.
