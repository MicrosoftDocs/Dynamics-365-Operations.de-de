---
title: Die Benutzerumgebung personalisieren
description: In diesem Artikel wird die Personalisierung von Microsoft Dynamics 365 for Finance and Operations beschrieben.
author: TLeforMicrosoft
manager: AnnBe
ms.date: 05/24/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysUserSetup, DefaultDashboard
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 62363
ms.assetid: 57b445d7-3e9e-4228-8728-f63b9dbd77a3
ms.search.region: Global
ms.author: tlefor
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 862bbf4d1d9b0dc2b6dc418ee766ed4dedef49fe
ms.openlocfilehash: 8ad5bd607f08d4e0b266d86a96a0b7f3e352c4cd
ms.contentlocale: de-de
ms.lasthandoff: 05/24/2018

---

# <a name="personalize-the-user-experience"></a>Die Benutzerumgebung personalisieren

[!include [banner](../includes/banner.md)]

In diesem Artikel wird die Personalisierung von Microsoft Dynamics 365 for Finance and Operations beschrieben.

Es gibt drei Grundarten von Personalisierungen in Finance and Operations. 
- Personalisierungen auf einer Einrichtungsseite. Hierzu gehören das Farbenthema und Zeitzone.
- Personalisierungen zu Seitennutzung *implizit* Personalisierungen genannt. So verfolgt beispielsweise Finance and Operations die Breite von Rasterspalten, wenn Sie sie anpassen sowie den erweiterten/reduzierten Status von Inforegistern. 
- Für explizite Personalisierungen treten Sie in einen interaktiven Personalisierungsmodus ein und ändern die Darstellung einer Seite, indem Sie direkt verwalten, wie Elemente auf der Seite angezeigt oder agieren. Diese Personalisierungen nennt man *explizite* Personalisierungen. Zum Beispiel kann der Benutzer Elemente auf der Seite hinzuzufügen, ausblenden oder neu anordnen.

Sämtliche Personalisierungen, die ein Benutzer in Finance and Operations vornimmt, gelten nur für diesen Benutzer, unabhängig von dem Unternehmen, mit dem der Benutzer interagiert. Änderungen, die ein Benutzer an einer Seite vornimmt, haben keine Auswirkungen auf andere Benutzer im System.

## <a name="system-wide-options-for-the-current-user"></a>Systemweite Optionen für den aktuellen Benutzer
Die Seite **Benutzeroptionen** enthält mehrere systemweite Einstellungen für den aktuellen Benutzer. Um die Seite **Benutzeroptionen** zu öffnen, wählen Sie das Formular **Einstellungen** (Zahnradsymbol) auf der Navigationsleiste, und wählen Sie dann **Benutzeroptionen**. Die Seite **Benutzeroptionen** besitzt vier Registerkarten, die verschiedene Benutzereinstellungen enthalten:

- **Visuell:** - Wird verwendet, um ein Farbenthema und die standardmäßige Größe der Elemente auf den Seiten auszuwählen.
- **Einstellungen** – Wählen Sie Standardwerte, die bei jedem Planungslauf verwendet werden, die Sie in Finance and Operations öffnen. Diese Werte umfassen das Unternehmen, die erste Seite und die Standardansicht/den Bearbeitungsmodus. (Anzeigen/Bearbeitungsmodus der bestimmt, ob eine Seite zum Anzeigen gesperrt ist oder diese zum Bearbeiten jedes Mal geöffnet wird, wenn Sie es öffnen.) Diese Registerkarte enthält Optionen für die Sprache, die Zeitzone und das Datum, die Uhrzeit und das Zahlenformat. Und schließlich enthält die Registerkarte unterschiedliche Einstellungen von Version zu Version.
- **Konto** - Verwenden, um Benutzer-ID und andere Konten bezogene Optionen anzugeben.
- **Workflow** – Wählen Sie workflowbezogene Optionen aus.

## <a name="implicit-personalizations"></a>Implizite Personalisierungen
Implizite Personalisierungen sind die Personalisierungen, die Sie ausführen, indem Sie einfach mit bestimmten Steuerelementen interagieren, die sich an ihren aktuell sichtbaren Status erinnern.

- **Rasterspalten:** - Sie können die Breite einer Spalte in einer Liste anpassen, indem Sie die Größenänderungsleiste links oder rechts des Spaltenkopfs auswählen und sie nach links oder rechts auf die gewünschte Breite schieben. Finance and Operations speichert die Breite, die Sie festlegen,m in einer Spalte. Dann wird die Breite dieser Spalte auf jedes Mal auf diese Größe angepasst, wenn Sie die Seite öffnen, die dieses Raster enthält.
- **Inforegister** –  Einige Seiten haben erweiterbare Abschnitte, die als *Inforegister* bezeichnet werden. Finance and Operations speichert Informationen über die Inforegister, die Sie erweitert und reduziert haben. Anschließend wird jedes Mal, wenn Sie zu einer Seite zurückkehren, das gleiche Inforegister erweitert oder reduziert, basierend auf Ihrer letzten Interaktion mit der Seite. In einigen Fällen verbessert das Reduzieren eines Inforegisters die Leistung, da Finance and Operations diese Informationen für das Inforegister erst abruft, wenn das Inforegister erweitert wird. Wie später in diesem Thema erläutert, können Sie den Auftrag auf dem Inforegister einer Seite auch ändern.
- **Infoboxen** - Einige Seiten haben einen Abschnitt, der als *Infoboxbereich* bezeichnet wird. Dieser Bereich enthält schreibgeschützte Informationen zum aktuellen Betreff der Seite. Jedem Abschnitt im Infoboxbereich wird als *Infobox* bezeichnet. Sie können den gesamten Infoboxbereich ausblenden oder anzeigen, und Sie können auch einzelne Infoboxen erweitern oder reduzieren. Finance and Operations speichert Ihre Einstellungen. Anschließend wird jedes Mal, wenn Sie zur Seite zurückkehren, der Status des Infoboxbereichs und die einzelnen Infoboxen, basierend auf Ihrer letzten Interaktion mit der Seite wiederhergestellt. In einigen Fällen verbessert das Reduzieren einer Infobox die Leistung, da Finance and Operations diese Informationen für die Infobox erst abruft, wenn die Infobox erweitert wird.
- **Aktivitätsbereiche** – *Aktivitätsbereich* Wird meistens oben an den meisten Seiten angezeigt. Der Aktivitätsbereich enthält Schaltflächen für viele der Aktivitäten, die auf der aktuellen Seite ausgeführt werden können. Diese Schaltflächen werden häufig auf Registerkarten zusammengefasst. Sie können den gesamten Aktivitätsbereich öffnen, oder Sie können ihn standardmäßig reduzieren lassen. Wenn Sie das nächste Mal die Seite öffnen, stellt Finance and Operations den fixierten Status des Aktivitätsbereichs wieder her. Wenn der fixiertes Aktivitätsbereich offen ist, zeigt Finance and Operations auch die Registerkarte der Aktivitäten an, die Sie zuletzt verwendet haben.
- **QuickFilters** – *QuickFilter* erscheint oberhalb vieler Raster. Mit QuickFilter können Sie Raster filtern, basierend auf einer Spalte, die Sie auswählen. Finance and Operations speichert die Spalte, die Sie gefiltert haben. Wenn Sie das nächste Mal die Seite öffnen, die dieses Raster enthält, ist der Raster in derselben Spalte gefiltert. Sie können jedoch dann den Raster auf einer anderen Spalte filtern.
- **Spaltenüberschriftfilter** – Wenn Sie einen Raster filtern, indem Sie *Spaltenüberschriftfilter* verwenden, können Sie den Filteroperator ändern, wie Sie ihn benötigen, um die Daten zu suchen, die Sie wünschen. Beispielsweise können Sie den gewünschten Operator von **beginnt mit** in **ist genau** ändern. Immer wenn Sie einen Spaltenüberschriftfilter verwenden und den Filteroperator zu ändern, speichert Finance and Operations die Änderung. Es stellt dann den Filteroperator das nächste Mal wieder her, wenn Sie diese Spalte filtern.
- **Navigationsbereich** – Sie können den *Navigationsbereich* öffnen, indem Sie auf die Schaltfläche **Menü** im linken Bereich der Seite auswählen. (Die Schaltfläche **Menü** wird auch als *Hamburger*, *Hamburgermenü* oder *Hamburgerschaltfläche* bezeichnet). Sie können den offenen Navigationsbereich anheften, oder Sie können ihn standardmäßig reduziert anzeigen. Nachdem Sie den Navigationsbereich als offen angeheftet haben, bleibt Finance and Operations offen, bis Sie ihn wieder reduzieren.

## <a name="explicit-personalizations"></a>Explizite Personalisierungen
Verschiedene Personen und Unternehmen haben eine unterschiedliche Perspektive auf die Daten, die Ihnen am wichtigsten sind, oder die Daten, die sie nicht für die Art benötigen, wie sie ihr Geschäft ausführen. In Finance and Operations können Sie die Art und Weise definieren, wie Ihre Informationen bestellt und verarbeitet werden. Sie können auch angeben, dass einige Informationen ausgeblendet werden sollen. Diese Funktionen sind zentral für eine persönliche und produktive Erfahrung und sind entscheidend für eine explizite Personalisierung. Explizite Personalisierungen sind Personalisierungen, die Sie explizit machen mit der Absicht, die Darstellungsweise oder das Verhalten eines Elements oder der Seite zu ändern, indem Sie ein Personalisierungsmenü auswählen.

### <a name="shortcut-menu-options"></a>Verknüpfungsmenüoptionen
Ein Kontextmenü enthält mehrere Möglichkeiten, explizit einer Seite zu ändern, um den Anforderungen und Bedürfnissen Ihres Unternehmens zu entsprechen. (Wird auch als *Rechtsklickmenü* oder *Kontextmenü* bezeichnet).

Einige der typischsten und wichtigsten Änderungen, die Sie an einer Seite vornehmen können, sind direkt als Optionen für ein Kontextmenü verfügbar. Zum Beispiel um eine Spalte in einem Raster ein- oder auszublenden, klicken Sie auf eine Rasterspaltenüberschrift mit der rechten Maustaste und wählen Sie dann **Hinzufügen von Spalten** oder **Ausblenden der Spalte** aus.

Darüber hinaus sind die Typen der grundlegendsten expliziten Personalisierung verfügbar, indem Sie auf ein Element mit der rechten Maustaste klicken und dann **Anpassen** auswählen. (Beachten Sie, dass nicht alle Elemente auf der Seite personalisiert werden können.) Wenn Sie diese  Methode der Personalisierung auswählen, wird das Eigenschaftenfenster des Elements angezeigt.

[![Personalisieren der Eigenschaften eines Elements](./media/personalization-element-properties.jpg)](./media/personalization-element-properties.jpg)

Sie können das Eigenschaftenfenster verwenden, um ein Element in folgender Hinsicht zu personalisieren:

- Ändern Sie die Bezeichnung des Elements.
- Verbergen Sie das Element, damit es nicht auf der Seite angezeigt wird. Die Daten im Feld werden nicht gelöscht oder geändert. Die derzeitigen Informationen werden nicht mehr auf der Seite angezeigt.
- Schließt die zusammengefassten Informationen im Bereich des Inforegisters ein (falls das Element in einem Inforegister ist).
- Hiermit überspringen Sie das Feld, wenn Sie mithilfe dieser Registerkarte die Felder auf der Seite verschieben.
- Verhindern Sie, dass Daten im Feld (für einen beliebigen Datensatz) bearbeitet werden.

Das Eigenschaftenfenster kann andere Personalisierungsfunktionen enthalten, abhängig vom Element. Beispielsweise können Sie mit dem Eigenschaftenfenster für eine Kachel diese Kachel in einem Dashboard höher stufen, und das Eigenschaftenfenster für das Dashboard lässt Sie möglicherweise einen neuen Arbeitsbereich auf diesem Dashboard erstellen.

### <a name="the-personalization-toolbar"></a>Personalisierungssymbolleiste
Wenn Sie Elementen verschieben oder ausblenden möchten oder einige Änderungen auf einer Seite vornehmen möchten, können Sie die Symbolleiste **Benutzereinstellungen** verwenden. Um die Symbolleiste **Benutzereinstellungen** zu öffnen, wählen Sie **Personalisieren Sie dieses Formular** im Fenster Eigenschaften eines Elements aus. Sie können **Personalisieren Sie dieses Formular** in der Gruppe **Anpassen** auf der Registerkarte **Optionen** des Aktivitätsbereichs jeder Seite auch auswählen.

[![Personalisierungssymbolleiste](./media/personalization-personalizationtoolbar.jpg)](./media/personalization-personalizationtoolbar.jpg)

Wenn die **Personalisierungssymbolleiste** geöffnet ist, ist die Seite nicht interaktiv. Sie können deshalb keine Daten eingeben oder Abschnitte erweitern oder reduzieren. Sie können nur Elemente ändern, die die Seite gestalten.

Folgende Tools sind auf der Symbolleiste **Benutzereinstellungen** verfügbar:

- Nutzen Sie das Werkzeug **Auswählen**, um Eigenschaften eines Elements auszuwählen und zu ändern. Nutzen Sie das Werkzeug **Auswählen**, um Eigenschaften eines Elements auszuwählen und zu ändern. Wenn Sie ein Element auswählen, wird das Eigenschaftenfenster des Elements geöffnet, und Sie können beliebige Eigenschaften für dieses Element ändern. Sie können den Prozess für andere Elemente auf Ihrem Formular wiederholen, die personalisierbar sind. Aber aufgrund der Methode, wie gewisse Elemente verwendet werden, können Sie in Finance and Operations gewisse Eigenschaften nicht ändern. Wenn Sie ein Element auswählen, werden Sie möglicherweise sehen, dass einige der Eigenschaften nicht geändert werden können. Sie können beispielsweise kein Feld ausblenden, das erforderlich ist.
- Wählen Sie das Tool **Umlagern** aus, wenn Sie ein Element auswählen und an einen anderen Lagerplatz innerhalb der aktuellen Elementgruppe umlagern möchten. (Sie können kein Element außerhalb seiner übergeordneten Gruppe verschieben.) Wählen Sie das Tool **Umlagern** aus, und aktivieren Sie anschließend das Element aus, um es zu verschieben. Wenn Sie ein Element auswählen, überprüft Finance and Operations die Seite um zu bestimmen, wohin das Element verschoben werden kann. Es erstellt dann eine Serie "Abstiegszonen." Da Sie das Element innerhalb der aktuellen Gruppe ziehen, wird jede Abstiegszone als farbige, fette Position neben dem Bereich angezeigt, in dem das Element abgelegt werden kann.
- Wählen Sie das Tool **Ausblenden**, um ein Element auf der Seite auszublenden. Wählen Sie das Tool **Verbergen** aus, und wählen Sie anschließend das Element aus, um es zu verbergen. Wenn Sie das Tool **Ausblenden** auswählen, werden alle Elemente, die gerade ausgeblendet werden, in einem schattierten Container angezeigt. Sie können sie dann einblenden. Wählen Sie das Tool **Auswählen**, um zu sehen, wie die Seite aussehen wird, wenn die ausgewählten Elementen ausgeblendet sind.
- Verwenden Sie das Tool **Zusammenfassung**, wenn ein Element im Inforegister Zusammenfassungsbereich angezeigt werden sollen. Das Tool „Zusammenfassung“ gilt nur für Felder, die innerhalb eines Inforegisterabschnitts enthalten sind. Wenn Sie das Tool **Zusammenfassung** auswählen, werden alle Felder, die ausgewählt wurden, in einem schattierten Container angezeigt. Sie können Felder der Inforegisterzusammenfassung interaktiv hinzufügen und Felder aus der Inforegisterzusammenfassung entfernen, indem Sie die Felder auswählen.
- Wählen Sie das **Überspringen** Tool, um ein Element aus der Tastaturtabulatorsequenz der Seite zu entfernen. Wenn Sie das Tool **Ausblenden** auswählen, werden alle Elemente, die gerade ausgeblendet werden, in einem schattierten Container angezeigt. Sie können sie Teil von der Tabulatorsequenz erneut erstellen.
- Wählen Sie das Tool **Bearbeiten** aus, wenn Sie ein Element als „Bearbeitbar“ oder „Nicht bearbeitbar“ markieren wollen. Wenn Sie das Tool **Bearbeiten** auswählen, werden alle Elemente, die gerade ausgeblendet werden, in einem schattierten Container angezeigt. Sie können definieren, dass sie wieder geändert werden können. Beachten Sie: Mehrere Felder sind obligatorisch und können nicht als nicht bearbeitbar festgelegt werden. Ein Schlosssymbol wird neben den Feldern angezeigt.
- Verwenden Sie die Schaltfläche **Einfügen**, um eine Liste mit Elementen zu finden, die für eine Seite eingefügt werden können.

    - Wählen Sie das Tool **Feld** unter **Einfügen**, um ein Feld der Seite hinzuzufügen. Wenn Sie das Tool **Feld** verwenden, können Sie nur Felder hinzufügen, die Teil der Seitendefinition sind, aber nicht die derzeit auf der Seite angezeigt werden. Informationen darüber, wie neue Felder erstellt werden, die nicht Teil der Definition der aktuellen Seite sind, finden Sie unter [Benutzerdefinierte Felder](user-defined-fields.md). Nachdem Sie das Tool **Feld** auswählen, müssen Sie die Gruppe oder den Bereich zunächst aktivieren, dem Sie ein Feld hinzufügen möchten. Ein Dialogfeld wird in der Liste der Felder angezeigt, die dem Bereich zugeordnet sind, den Sie ausgewählt haben. Wählen Sie im Dialogfeld mindestens ein Feld aus und wählen Sie **Einfügen**en Benutzer oder mindestens eine Gruppe aus. Wenn Sie ein Feld entfernen, das Sie zuvor hinzugefügten haben, wiederholen Sie den Vorgang aber deaktivieren Sie die Option im Dialogfeld.
    - Wählen Sie das Tool **PowerApp** unter **Einfügen**, um eine App einzfügen, die unter Microsoft PowerApps auf der Seite erstellt wurden. Ausführliche Informationen dazu, wie eine PowerApps-App in eine Seite eingebettet wird, finden Sie unter [Betten Sie Sie PowerApps ein](embed-power-apps.md).

- Wählen Sie die **Verwalten** Schaltfläche, um eine Liste der zu Verwaltungsoptionen finden, die für alle Personalisierungen für die aktuelle Seite zugeordnet werden.

    - Wählen Sie **Löschen**, um die Seite zu dem Standard zurückzusetzen, installiertes Bundesland zurückzusetzen. Alle Personalisierungen auf der aktuellen Seite sind deaktiviert. Es gibt keine rückgängig gemachte Aktion. Daher verwenden Sie diese Option, wenn Sie sicher sind, dass Sie die Seite zurücksetzen möchten.
    - Wählen Sie **Importieren**, um eine Personalisierung aus einer Personalisierungsdatei zu verwenden, die Sie oder eine andere Person zuvor für diese Seite erstellt haben. Alle Ihre aktuellen Personalisierungen für die Seite werden von der Personalisierungen aus der ausgewählten Datei ersetzt.
    - Wählen Sie **Exportieren**, um die Personalisierungen für die Seite in einer Datei zu speichern. Sie können hre Personalisierungen mit  anderen Benutzern teilen. Diese Benutzer müssen nur die Datei importieren, die für Ihre Personalisierungen die Seite enthält.

- Wählen Sie die Schaltfläche **Schließen**, um die Symbolleiste **Personalisieren**zu schließen und den vorherigen interaktiven Status zurückzuversetzen.

Wenn die Symbolleiste **Personalisierungen** verwendet wird, sind Speichervorgänge implizit. Ihre Personalisierungen werden wirksam, sobald Sie diese erstellen, und Sie müssen eine Schaltfläche **Speichern** nicht auswählen. Manchmal finden Sie ein Schlosssymbol neben einem Element, wenn Sie ein Tool auswählen. Dieses Symbol zeigt an, dass Sie die Elementeigenschaften nicht ändern können, die dem ausgewählten Tool zugeordnet sind, da sich die vorgenommenen Änderungen auf den Eigenschaften verhindern, dass die Seite ordnungsgemäß funktioniert.

### <a name="adding-a-tile-list-or-link-to-a-workspace"></a>Hinzufügen einer Kachel oder Liste zu einem Arbeitsbereich
Für mehrere Seiten, die Listen enthalten, ist eine weitere Personalisierungsfunktion verfügbar. Die Schaltfläche **Zum Bereich hinzugefügt** in der Gruppe **Anpassen** auf der Registerkarte **Optionen** im Aktivitätsbereich zeigt die Informationen der aktuellen Liste in einem bestimmten Arbeitsbereich an. Sie können eine gefilterte und sortierte Ansicht der Informationen im Arbeitsbereich anzeigen oder die Standardansicht anzeigen. Sie können auch angeben, ob die Informationen als Liste im Arbeitsbereich als Liste, als zusammenfassende Kachel, die die Anzahl der Elemente in der Liste anzeigt oder als Link angezeigt wird.

[![Zum Arbeitsbereich hinzufügen](./media/personalization-addtoworkspace.png)](./media/personalization-addtoworkspace.png)

- Um eine Liste einem Arbeitsbereich hinzuzufügen, sortieren oder filtern Sie zuerst die Liste auf der Seite, sodass die Informationen so angezeigt werden, wie Sie sie im Arbeitsbereich wünschen. Wählen Sie dann **zum Arbeitsbereich hinzufügen** aus. Wählen Sie einen Arbeitsbereich und dann im Feld **Präsentation** wählen Sie **Liste** aus. Nachdem Sie **Konfigurieren** auswählen, wird ein Dialogfeld angezeigt, wo Sie die Spalten auswählen können, die in der Liste im Arbeitsbereich angezeigt werden sollen. Sie können auch die Beschriftung definieren, um die Liste im Arbeitsbereich zu verwenden.
- Um eine Kachel zu einem Arbeitsbereich hinzuzufügen, filtern Sie zuerst die Liste, um die Daten darzustellen, die Sie zusammenfassen möchten (oder schnellen Zugriff darauf wünschen). Wählen Sie dann **zum Arbeitsbereich hinzufügen** aus. Wählen Sie einen Arbeitsbereich und dann im Feld **Präsentation** wählen Sie **Kachel** aus. Nachdem Sie **Konfigurieren** auswählen, wird ein Dialogfeld angezeigt, in dem Sie die Beschriftung angeben können, die für Kachel im Arbeitsbereich zu verwenden sind. Sie können auch angeben, ob die Kachel eine Anzahl anzeigen soll. Nachdem Sie die Kachel dem Arbeitsbereich hinzugefügt haben, können Sie ihn aktivieren, um die aktuelle Seite über Arbeitsbereich zu öffnen und die gefilterte Liste anzuzeigen, die der Kachel zugeordnet ist.
- Um einen Link einem Arbeitsbereich hinzuzufügen, filtern Sie zuerst die Liste auf der Seite, sodass Sie die Daten sehen, die für Sie interessant sind. Wählen Sie dann **zum Arbeitsbereich hinzufügen** aus. Wählen Sie einen Arbeitsbereich und dann im Feld **Präsentation** wählen Sie **Link** aus. Nachdem Sie **Konfigurieren** auswählen, wird ein Dialogfeld angezeigt, in dem Sie die Beschriftung angeben können, die für Links im Arbeitsbereich zu verwenden sind. Sie können eine Beschriftung für einen neuen Abschnitt optional auch angeben, der diesen Link enthält.

Nachdem Ihre Liste, Kachel oder Link dem Arbeitsbereich hinzugefügt wurde, können Sie den Arbeitsbereich öffnen und die Element so anordnen, wie Sie dies wünschen.

### <a name="adding-a-summary-from-a-workspace-to-a-dashboard"></a>Hinzufügen einer Zusammenfassung von einem Arbeitsbereich zu einem Dashboard
Einige Arbeitsbereiche enthalten Zählkacheln (das heißt, Kacheln, die Zahlen enthalten) und Sie wollen möglicherweise diese Kacheln auch auf Ihrem Dashboard anzeigen. Klicken Sie in einem Arbeitsbereich mit der rechten Maustaste auf eine Zählkachel, und klicken Sie auf **Anpassen**. Im Eigenschaftenfenster der Kachel, wählen Sie **an Dashboard anheften**. Das nächste Mal, wenn Sie zum ausgewählten Dashboard navigieren (und es aktualisieren), finden Sie die Zahl unter der Navigationskachel dieses Arbeitsbereichs im Dashboard. Sie können diese Anzahl auswählen, um direkt zu den Daten zu wechseln, die dargestellt werden.

### <a name="personalizing-your-dashboard"></a>Ihr Dashboard personalisieren
Das Dashboard ist oftmals die erste Seite, die beim Öffnen von Finance and Operations angezeigt wird. Sie können das Dashboard personalisieren, so dass lediglich dje Arbeitsbereichskacheln angezeigt werden, die Sie sehen möchten. Sie können die Kacheln auch neu anordnen, damit sie in der von Ihnen gewünschten Reihenfolge erscheinen, Ihren Arbeitsbereich mit den Navigationskacheln neu benennen oder eine komplett neue Arbeitsbereichkachel hinzufügen.

Um das Dashboard zu personalisieren, klicken Sie auf eine beliebige Kachel mit der rechten Maustaste, und wählen Sie dann das **Anpassen**-Eigenschaftenfenster, um die Kachel zu öffnen.

- Wenn Sie die ausgewählten Kachel ausblenden oder umbenennen möchten, können Sie diese Änderung direkt im Eigenschaftenfenster vornehmen.
- Wenn Sie die Kacheln im Arbeitsbereich neu anordnen möchten, wählen Sie **Dieses Formular personalisieren** im Eigenschaftenfenster aus, um die **Personalisierungs**symbolleiste zu öffnen. Sie können das Tool **Umlagern** verwenden, um die Kacheln anzuordnen.
- Wenn Sie eine neue Arbeitsbereichskachel erstellen möchten, wählen Sie im Eigenschaftenfenster **Arbeitsbereich hinzufügen** aus. Eine neue Arbeitsbereichkachel wird am unteren Rand das Dashboard erstellt. Sie können diese neue Arbeitsbereichkachel umbenennen, wenn Sie dies wünschen. Sie können, Kacheln, Listen und auch Links dem Arbeitsbereich hinzufügen wie im Abschnitt [Hinzufügen von Kacheln, Listen oder Links zu Arbeitsbereichen](personalize-user-experience.md#adding-a-tile-list-or-link-to-a-workspace) beschrieben.

## <a name="administration-of-personalization"></a>Verwalten der Personalisierung
Nach dem Personalisieren einer Seite können Sie die Personalisierungen mit anderen Benutzern teilen, indem Sie die personalisierte exportieren. Sie können dann die anderen Benutzer auffordern, die personalisierte Seite zu öffnen und die personalisierte Datei zu importieren. Alternativ können Sie die Personalisierung an einen Benutzer geben, der Administratorrechte besitzt. Dieser Benutzer kann die Personalisierungsdatei für viele Benutzer gleichzeitig übernehmen.

Benutzer mit Administratorrechten können Personalisierungen auch für andere Benutzer auf der Seite **Personalisierung** verwalten. Diese Seite besitzt vier Registerkarten:

- **Anwenden** - Sie können eine Personalisierung für einen oder mehrere Benutzer auswählen. Um eine Personalisierung für einen oder mehrere Benutzer anzuwenden, wählen Sie zuerst eine Rolle und Benutzer aus, die diese Rolle besitzen. Wählen Sie anschließend eine vorhandene Personalisierung aus, um die ausgewählten Benutzer zu übernehmen oder importieren Sie eine Personalisierung. Die Personalisierung wird geprüft und auf alle ausgewählten Benutzer angewendet, wenn diese die ausgewählte Seite das nächste Mal öffnen.
- **Löschen** – Sie können eine Seiten- oder Arbeitsbereichspersonalisierung für einen oder mehrere Benutzer löschen. Wählen Sie eine Seite oder einen Arbeitsbereich aus, um die Liste der Benutzer zu sehen, die diese Seite personalisiert haben. Anschließend wählen Sie die Benutzer, die für diese deaktivierte Seite oder Arbeitsbereich aus und wählen Sie **Löschen** aus. Alle Personalisierungen, die die ausgewählten Benutzer auf die ausgewählte Seite oder den ausgewählten Arbeitsbereich angewendet haben, werden gelöscht. Diese Aktion kann nicht rückgängig gemacht werden. Wenn eine Personalisierung für die Seite oder den Arbeitsbereich gespeichert wurde, dann kann die Personalisierung neu importiert werden.
- **Manager pro Benutzer** – Wählen Sie einen Benutzer aus, um die Liste der Seiten anzuzeigen, die personalisiert wurde. Sie können dann die Möglichkeit aktivieren oder deaktivieren, um zu bestimmen, ob der ausgewählte Benutzer Personalisierungen für bestimmte Seiten oder das gesamte System verwenden kann oder nicht. Sie können Personalisierungen auch löschen, importieren oder exportieren für diesen Benutzer.
- **System** – Sie können temporär alle Personalisierungen im System für alle Benutzer deaktivieren oder abschalten. In diesem Fall werden keine Personalisierungen gelöscht. Alle Seiten werden derzeit für ihre Standardannahhme für alle Benutzer zurückgesetzt. Wenn Sie die Personalisierungen später wieder reaktivieren, werden diese wieder auf die Seiten der Benutzer angewendet. Sie können temporär alle Personalisierungen im System für alle Benutzer deaktivieren oder abschalten. Es gibt keine Möglichkeit, Personalisierungen wiederherzustellen, die gelöscht wurden. Deshalb müssen Sie vor diesem Schritt sicherstellen, dass Sie alle Personalisierungen exportiert haben, die Sie später importieren möchten.

## <a name="personalization-of-inventory-dimensions"></a>Personalisierung von Lagerungsdimensionen

Wenn Sie die Einstellungen der Lagerungsdimensionen auf einer Seite personalisieren, beachten Sie die Einstellungen, die erstellt wurden, indem Sie die Option **Anzeigendimension** nutzen. So verwenden Sie die Personalisierung, um eine Spalte für die Chargennummerenlagerungsdimension auszublenden, doch die Spalte erscheint das nächste Mal, wenn die Seite geöffnet wird. Dieses Verhalten tritt auf, da die Einstellungen die Lagerungsdimensionsspalten **Dimensionenanzeige** steuern, die angezeigt werden.

Die **Dimensionsanzeigeeinstellungen** gelten für alle Seiten und diese Einstellungen setzen alle personalisierten Lagerdimensionsfelder einer individuellen Seite außer Kraft.

Wenn Sie wie im vorhergehenden Beispiel nicht möchten, dass die Spalte für die Chargennummerenlagerungsdimension erscheint, müssen Sie die die Dimension als Teil der Tabelle  **Anzeigendimensionen** deaktivieren. Schließlich wird diese Änderung nicht nur auf einer bestimmten Seite jedoch über allen Seiten gelten.

