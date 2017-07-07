---
title: Personalisierung der Benutzerumgebung
description: In diesem Artikel wird die Personalisierung von Microsoft Dynamics 365 for Finance and Operations beschrieben.
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysUserSetup
audience: Application User, IT Pro
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 62363
ms.assetid: 57b445d7-3e9e-4228-8728-f63b9dbd77a3
ms.search.region: Global
ms.author: tlefor
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: b338a930777a5945eb6318dc8066fb3649c79dbe
ms.contentlocale: de-de
ms.lasthandoff: 06/13/2017


---

# <a name="personalize-the-user-experience"></a>Die Benutzerumgebung personalisieren

[!include[banner](../includes/banner.md)]


In diesem Artikel wird die Personalisierung von Microsoft Dynamics 365 for Finance and Operations beschrieben.

Es gibt verschiedene Personalisierungen in Microsoft Dynamics 365 for Finance and Operations. Einige Personalisierungen sind Auswahlen, die Sie in einer Liste an Optionen auf einer Einstellungsseite vornehmen. Einige sind implizit. So verfolgt beispielsweise Finance and Operations die Breite von Rasterspalten, wenn Sie sie anpassen sowie den erweiterten/reduzierten Status von Inforegistern. Andere Personalisierungen sind explizit. Für explizite Personalisierungen treten Sie in einen interaktiven Personalisierungsmodus ein und ändern die Darstellung einer Seite, indem Sie direkt verwalten, wie Elemente auf der Seite angezeigt oder agieren. 

Sämtliche Personalisierungen, die ein Benutzer in Finance and Operations vornimmt, gelten nur für diesen Benutzer, unabhängig von dem Unternehmen, mit dem der Benutzer interagiert. Änderungen, die ein Benutzer an einer Seite vornimmt, haben keine Auswirkungen auf andere Benutzer im System.

## <a name="systemwide-options-for-the-current-user"></a>Systemweite Optionen für den aktuellen Benutzer
In der Navigationsleiste sehen Sie ein Zahnrad, das als Menüschaltfläche **Einstellungen** bezeichnet wird. Durch Öffnen des Menüs **Einstellungen** werden einige Optionen angezeigt. Durch Auswählen von **Optionen** wird die Seite **Benutzeroptionen** geöffnet. Dort finden Sie vier Optionsregisterkarten: **Visuell**, **Voreinstellungen**, **Konto** und **Workflow**.

-   **Visuell:** Wird verwendet, um ein Farbenthema und die standardmäßige Größe der Elemente auf den Seiten auszuwählen.
-   **Einstellungen:** Hier können Sie Standards definierten, die verwendet werden, wenn Sie Finance and Operations öffnen, einschließlich Unternehmen, ursprüngliche Seite, standardmäßiger Ansichts- und Bearbeitungsmodus (bestimmt, ob eine Seite zur Ansicht gesperrt ist oder für die Bearbeitung geöffnet wird, wenn Sie sie öffnen). Sie finden auch Optionen für Sprache, Zeitzone, Datum, Uhrzeit und Zahlenformat. Schließlich enthält diese Seite mehrere verschiedene Voreinstellungen, die von Freigabe zu Freigabe variieren.
-   **Konto:** Wird verwendet, um Ihre Benutzerkennung und andere kontobezogene Optionen bereitzustellen.
-   **Workflow:** Hier können Sie workflowbezogene Optionen auswählen.

## <a name="implicit-personalizations"></a>Implizite Personalisierungen
Implizite Personalisierungen sind die Personalisierungen, die Sie ausführen, indem Sie einfach mit bestimmten Steuerelementen interagieren, die sich an ihren aktuell sichtbaren Status erinnern. 

**Rasterspalten:** Sie können die Breite einer Spalte in einer Liste anpassen, indem Sie die Größenänderungsleiste links oder rechts des Spaltenkopfs auswählen und sie nach links oder rechts auf die gewünschte Breite schieben. Finance and Operations speichert die gewünschte Breite und zeigt eine Spalte in dieser Breite an, wenn Sie die Seite mit der Liste öffnen. 

**Inforegister:** Einige Seiten haben erweiterbare Abschnitte, die als Inforegister bezeichnet werden. Finance and Operations speichert die erweiterten Inforegister und die reduzierten Inforegister. Jedes Mal, wenn Sie zur Seite zurückkehren, werden diese gleichen Inforegister auf Grundlage der letzten Nutzung erweitert oder reduziert. In diesem Artikel erklären wir, wie die Reihenfolge Ihrer Inforegisterabschnitte geändert werden kann. In einigen Fällen verbessert das Reduzieren eines Inforegisters die Leistung, da Finance and Operations diese Informationen für das Inforegister erst abruft, wenn das Inforegister erweitert wird. 

**Infoboxen:** Einige Seiten haben einen Abschnitt, der als Infoboxbereich bezeichnet wird. Dieser Bereich enthält schreibgeschütztes Informationen zum aktuellen Betreff der Seite. Jedem Abschnitt im Infoboxbereich wird als Infobox bezeichnet. Sie können eine Infobox erweitern oder reduzieren und Finance and Operations speichert ihre Einstellungen. In einigen Fällen verbessert das Reduzieren einer Infobox die Leistung, da Finance and Operations diese Informationen für die Infobox erst abruft, wenn die Infobox erweitert wird.

## <a name="explicit-personalizations-using-the-personalization-toolbar"></a>Explizite Personalisierungen mithilfe der Personalisierungssymbolleiste
Jede Person und jedes Unternehmen hat eine unterschiedliche Meinung dazu, welche Daten für sie bzw. es am wichtigsten sind, oder welche Daten nicht für die Art und Weise erforderlich sind, wie sie ihr Geschäft führen. Die Möglichkeit, die Anordnung Ihrer Informationen anzupassen, mit diesen zu interagieren oder diese auszublenden, ist wichtig, damit Finance and Operations eine personalisierte und produktive Erfahrung ermöglicht. 

Explizite Personalisierungen stehen die Personalisierungen, denen Sie explizit mit der Absicht ausgeführt werden, um die Darstellungsweise oder das Verhalten eines Elements oder der Seite zu ändern, indem Sie ein Personalisierungsmenü auswählen. Der Typ der grundlegendste expliziten Personalisierung ist, wo Sie auf ein Element mit der rechten Maustaste klicken und auswählen **Personalisiern**. "Hinweis, dass nicht alle Elemente auf der Seite kann personalisiert werden.) Bei dieser Methode die Personalisierung auswählen, werden das Eigenschaftenfenster des Elements. 

[![Personalisieren der Eigenschaften eines Elements](./media/personalization-element-properties.jpg)](./media/personalization-element-properties.jpg) 

So personalisieren Sie ein Element auf Ihrer Seite, wenn Sie nur die Bezeichnung des Elements ändern möchten, das Element ausblenden möchten, damit es nicht auf der Seite angezeigt wird (dies ändert keine Daten, es werden lediglich Ihre Informationen nicht angezeigt), die Informationen in die Zusammenfassung des Inforegisters aufnehmen möchten (wenn das Element in einem Inforegister enthalten ist), das Feld mit der Tabulatortaste überspringen möchten oder es als „Nicht bearbeiten“ markieren, damit Daten nicht geändert werden können. 

Wenn Sie Elemente verschieben oder ausblenden oder mehrere Änderungen vornehmen möchten, können Sie die Personalisierungssymbolleiste verwenden, die im Eigenschaftenfenster der Elemente verfügbar ist, indem Sie **Dieses Formular personalisieren** auswählen. Die Personalisierungssymbolleiste ist auch im Aktivitätsbereich des Formulars verfügbar, unter der Personalisierungsgruppe der Registerkarte **Optionen**. Wählen Sie **Dieses Formular personalisieren**,und die Personalisierungssymbolleiste wird angezeigt. 

[![Personalisierungssymbolleiste](./media/personalization-personalizationtoolbar.jpg)](./media/personalization-personalizationtoolbar.jpg)

Der Personalisierungssymbolleiste gibt es einige Personalisierungsaktivitäten. Wählen Sie das Tool **Auswählen**, wenn Sie die Eigenschaften viele Elemente einzeln auswählen und ändern möchten. Klicken Sie zuerst auf das Tool „Auswählen“, und klicken Sie anschließend auf das Element, dessen Eigenschaften Sie ändern möchten. Wenn Sie ein Element auswählen, wird das Eigenschaftenfenster des Elements geöffnet, und Sie können beliebige Eigenschaften für dieses Element ändern. Sie können den Prozess für andere Elemente auf Ihrem Formular wiederholen, die personalisierbar sind. In einigen Fällen wählen Sie ein Element aus und stellen fest, dass einige der Eigenschaften nicht geändert werden können. Das heißt, dass je nach Art der Nutzung des aktuellen Elements lässt Finance and Operations nicht zu, dass Sie die Eigenschaft ändern. Sie können beispielsweise kein Feld ausblenden, das erforderlich ist. 

Wählen Sie das Tool **Umlagern** aus, wenn Sie ein Element auswählen und an einen anderen Lagerplatz innerhalb der aktuellen Elementgruppe umlagern möchten. (Sie können kein Element außerhalb seiner übergeordneten Gruppe verschieben.) Klicken Sie zuerst auf das Tool „Umlagern“ und anschließend auf das Element, das Sie verschieben möchten. Wenn Sie auf das gewünschte Element klicken, scannt Finance and Operations das Formular, um zu verstehen, wohin dieses Element verschoben werden kann und erstellt eine Reihe von „Ablagezonen“, die als farbige, fette Linie neben dem Bereich angezeigt wird, an dem das Element abgelegt werden kann, wenn Sie das Element innerhalb der aktuellen Gruppe verschieben. 

Wählen Sie das Tool **Ausblenden**, um ein Element auszuwählen und auszublenden. Um ein Element auszublenden, wählen Sie einfach das Tool „Ausblenden“, und klicken Sie auf das Element, das Sie ausblenden möchten. Wenn Sie das Tool „Ausblenden“ auswählen, werden alle aktuell ausgeblendeten Elemente sichtbar gemacht und in einem schattierten Container angezeigt, damit Sie das Element auswählen können, um es einzublenden. Wählen Sie das Tool „Auswählen“, um zu sehen, wie die Seite mit den ausgewählten Elementen ausgeblendet aussehen wird. Wählen Sie das Tool **Zusammenfassung** aus, wenn Sie ein numerisches oder Zeichenfolgenfeld im Zusammenfassungsbereich des Inforegisters anzeigen möchten. Das Tool „Zusammenfassung“ gilt nur für Felder, die innerhalb eines Inforegisterabschnitts enthalten sind. Wenn Sie das Tool „Zusammenfassung“ auswählen, zeigt Finance and Operations alle Felder, die als Zusammenfassungsfelder ausgewählt wurden, indem es sie in einem schattierten Container einschließt. Sie können Felder aus einer Inforegisterzusammenfassung interaktiv hinzufügen und entfernen, indem Sie auf das Feld klicken. 

Wählen Sie das **Überspringen** Tool, um ein Element aus der Tastaturtabulatorsequenz der Seite zu entfernen. Wenn Sie das Tool „Überspringen“ auswählen, werden alle derzeit übersprungenen Elemente in einem schattierten Container angezeigt, damit Sie diese erneut auswählen können, um sie zu einem Teil der Tabulatorsequenz zu machen, indem Sie ein übersprungenes Element auswählen. 

Wählen Sie das Tool **Bearbeiten** aus, wenn Sie ein Element als „Bearbeitbar“ oder „Nicht bearbeitbar“ markieren wollen. Wenn Sie das Tool „Bearbeiten“ auswählen, werden alle aktuell nicht bearbeitbaren Elemente sichtbar gemacht und in einem schattierten Container angezeigt, damit Sie sie auswählen können, um sie bearbeitbar zu machen. Beachten Sie: Mehrere Felder sind obligatorisch und können nicht als nicht bearbeitbar festgelegt werden. Diese Felder werden mit einem Vorhängeschlosssymbol angezeigt. 

Wählen Sie das Tool **Hinzufügen**, um ein Feld zur Seite hinzuzufügen. Mit dem Tool „Hinzufügen“ können Sie kein neues Feld erstellen, Sie können aber Felder hinzufügen, die Teil der aktuellen Seitendefinition sind, aber nicht auf der Seite dargestellt werden. Wenn Sie das Tool „Hinzufügen“ auswählen, müssen Sie zunächst die Gruppe oder den Bereich auswählen, der bzw. dem Sie ein Feld hinzufügen möchten. Ein Dialogfeld wird in der Liste der Felder angezeigt, die dem Bereich zugeordnet sind, den Sie ausgewählt haben. In diesem Dialogfeld können Sie ein oder mehrere Felder zum Hinzufügen auswählen und auf „Einfügen“ klicken. Wenn Sie später ein Feld entfernen möchten, das Sie zuvor hinzugefügt haben, wiederholen Sie den Prozess, aber deaktivieren Sie einfach das Feld, das Sie zuvor hinzugefügt haben. 

Wählen Sie die **Verwalten** Schaltfläche, um eine Liste der zu Verwaltungsoptionen finden, die für alle Personalisierungen für die aktuelle Seite zugeordnet werden. 

Wählen Sie **Löschen**, um die Seite zu dem Standard, installiertes Bundesland zurückzusetzen. Alle Personalisierungen auf der aktuellen Seite sind deaktiviert. Es gibt keine rückgängig gemachte Aktion, können so nur diese Option, wenn Sie sicher sind, die Seite zurücksetzen möchten. 

Wählen Sie **Importieren**, um eine Personalisierung aus einer Personalisierungsdatei zu verwenden, die Sie oder eine andere Person zuvor für diese Seite erstellt haben. Durch das Importieren einer Personalisierung werden alle Personalisierungen gelöscht, die Sie auf der gesamten Seite ausgeführt haben, und stattdessen werden alle Personalisierungen aus der ausgewählten Datei verwendet. Wenn Sie eine Personalisierung speichern oder freigeben möchten, wählen Sie die Option **Exportieren** aus, um die Personalisierungen in einer Datei zu speichern. 

Wählen Sie die Schaltfläche **Schließen**, um die Symbolleiste zu schließen und die Seite wieder in den interaktiven Status zurückzuversetzen. 

Bei der Personalisierungssymbolleiste ist das Speichern implizit. Ihre Personalisierungen sind sofort wirksam, wenn sie vornehmen, und es ist nicht erforderlich, auf die Schaltfläche **Speichern** zu klicken. Manchmal finden Sie ein Vorhängeschlosssymbol neben einem Element ein Tool, wenn Sie auswählen. Das bedeutet das, damit die Seite, funktioniert einwandfrei, wie Sie die Eigenschaften nicht ändern können, die dem ausgewählten zugeordnet Tool werden. Wenn die Personalisierungssymbolleiste geöffnet wird, wird die Seite nicht interaktiv. Sie können keine Daten eingeben oder Abschnitte erweitern oder reduzieren.

## <a name="explicit-personalization-adding-a-tile-or-list-to-a-workspace"></a>Explizite Personalisierung: Hinzufügen einer Kachel oder Liste zu einem Arbeitsbereich
Einige Seiten mit Listen haben eine zusätzliche Personalisierungsfunktion innerhalb des Aktivitätsbereichs, unter der Personalisierensgruppe der Registerkarte „Optionen“. Wählen Sie **Zum Arbeitsbereich hinzufügen** aus, um die Dropdownliste zu öffnen, die Ihnen die Möglichkeit gibt, die Informationen in der aktuellen Liste (gefiltert und sortiert oder Standard) in einen Arbeitsbereich als Liste oder Zusammenfassungskachel anzuzeigen (diese kann verwendet werden, um die Anzahl der Artikel in der Liste anzuzeigen). 

[![Zum Arbeitsbereich hinzufügen](./media/personalization-addtoworkspace.png)](./media/personalization-addtoworkspace.png) 

Um eine Liste zu einem Arbeitsbereich hinzuzufügen, sortieren oder filtern Sie zuerst die Liste mit diesen Informationen so, wie sie in Ihrem Arbeitsbereich angezeigt werden sollen. Wählen Sie dann das Dialogfeld „Zum Arbeitsbereich hinzufügen“ aus. Danach wählen Sie den gewünschten Arbeitsbereich aus und wählen **Liste** aus der Präsentationsdropdownliste aus. Wenn Sie **Liste** auswählen, wird ein Dialogfeld geöffnet, in dem Sie die Spalten auswählen können, die Sie in der Liste anzeigen möchten, sowie die Beschriftung für die Liste, wie sie im Arbeitsbereich angezeigt wird. 

Um eine Kachel zu einem Arbeitsbereich hinzuzufügen, filtern Sie zuerst die Liste, um die Daten darzustellen, die Sie zusammenfassen möchten (oder schnellen Zugriff darauf wünschen). Öffnen Sie anschließend das Dialogfeld „Zum Arbeitsbereich hinzufügen“. Danach wählen Sie den gewünschten Arbeitsbereich aus und wählen **Kachel** aus der Präsentationsdropdownliste aus. Wenn Sie **Kachel** auswählen, wird ein Dialogfeld angezeigt, in dem Sie eine Kachelbeschriftung angeben und entscheiden können, ob die Kachel eine Zahl anzeigt. Wenn die Kachel auf einen Arbeitsbereich platziert ist, können Sie die aktuelle Seite über den Arbeitsbereich öffnen und die Liste der Informationen in Bezug auf die Kachel anzeigen. 

Wenn die Liste oder Kachel zu einem Arbeitsbereich hinzugefügt wird, können Sie diesen Arbeitsbereich öffnen und die Liste oder Kachel in der Gruppe neu anordnen, in der sie platziert wurde.

## <a name="explicit-personalization-adding-a-summary-from-a-workspace-to-a-dashboard"></a>Explizite Personalisierung: Hinzufügen einer Zusammenfassung aus einem Arbeitsbereich zu einem Dashboard
Einige Arbeitsbereiche enthalten die Anzahl kacheln (Kacheln mit Zahlen für sie diese) möchten Sie auch in Ihrem Dashboard finden. Klicken Sie in einem Arbeitsbereich mit der rechten Maustaste eine Zählkachel, und klicken Sie auf **Anpassen**. Wählen Sie **An Dashboard anheften** aus. Das nächste Mal, wenn Sie zum ausgewählten Dashboard navigieren (und es aktualisieren), finden Sie die Zahl unter der Navigationskachel dieses Arbeitsbereichs im Dashboard.

## <a name="explicit-personalization-personalizing-your-dashboard"></a>Explizite Personalisierung: Personalisieren des Dashboards
Das Dashboard ist oftmals die erste Seite, die beim Öffnen von Finance and Operations angezeigt wird. Sie können das Dashboard personalisieren, um die Arbeitsbereichsnavigationskacheln umzubenennen, um nur nur Kacheln anzuzeigen, die Sie sehen möchten, um die Kacheln umzubenennen oder um die Kacheln in der Reihenfolge anzuordnen, in der Sie sie sehen möchten. Um das Dashboard zu personalisieren, wählen Sie eine beliebige Kachel aus und klicken Sie mit der rechten Maustaste, um ein Kontextmenü zu öffnen. Wählen Sie im Kontextmenü **Anpassen** aus. Wenn die ausgewählte Kachel eine ist, die Sie ausblenden oder umbenennen oder übersprungen möchten, können Sie diese Änderung direkt im anzeigten Eigenschaftenfenster vornehmen. Wenn Sie die Kacheln anordnen möchten, wählen Sie **Dieses Formular personalisieren** im Eigenschaftenfenster aus, um die Personalisierungssymbolleiste zu öffnen. Sie können das Tool „Umlagern“ dann verwenden, um die Kacheln anzuordnen.

## <a name="administration-of-personalization"></a>Verwalten der Personalisierung
Nach dem Personalisieren einer Seite können Sie die Personalisierungen mit anderen Benutzern teilen. Exportieren Sie einfach die personalisierte Seite. Sie können dann die anderen Benutzer auffordern, zur personalisierten Seite zu navigieren und die von Ihnen personalisierte Datei zu importieren.

Benutzer mit Administratorrechten können Personalisierungen auch für andere Benutzer auf der Seite **Personalisierung** verwalten. Diese Seite hat vier Registerkarten: **System**, **Benutzer**, **Importieren** und **Löschen**.

- **System** – Sie können temporär alle Personalisierungen im System deaktivieren oder abschalten. In diesem Fall werden keine Personalisierungen gelöscht. Sie setzen nur alle Seiten auf den Standardstatus zurück. Wenn Sie die Personalisierungen später wieder reaktivieren, werden diese wieder auf die Seiten der Benutzer angewendet. Sie können auch Personalisierungen für alle Benutzer löschen. Beachten Sie, dass wenn Sie Personalisierungen löschen, keine Möglichkeit besteht, Personalisierungen vom System automatisch zu aktivieren. Deshalb müssen Sie vor diesem Schritt sicherstellen, dass Sie alle Personalisierungen exportiert haben, die Sie später importieren möchten.
- **Benutzer** – Sie können festlegen, ob die einzelnen Benutzer implizite oder explizite Personalisierungen vornehmen können. Sie können auch festlegen, ob Benutzer auf einer bestimmten Seite implizite oder explizite Personalisierungen vornehmen können. Abschließend können Sie eine Personalisierung für einen Benutzer importieren, exportieren oder löschen.
- **Importieren** – Sie können eine Personalisierung für einen oder mehrere Benutzer importieren. Sie nutzen diese Registerkarte, nachdem Sie eine Personalisierung auf einer Seite oder einem Arbeitsbereich vorgenommen haben und diese dann als Personalisierungsdatei exportiert haben. Zum Importieren der Personalisierungsdatei und zum Anwenden dieser auf einen oder mehrere Benutzer wählen Sie die Benutzer in der Liste aller Benutzer aus oder Filtern nach einer bestimmten Rolle und wählen die Benutzer in der Rolle aus. Nach Auswahl der Benutzer, die die Personalisierung nutzen, klicken Sie auf **Importieren**, und wählen Ihre personalisierte Datei aus. Die Personalisierung wird geprüft und auf alle ausgewählten Benutzer angewendet, wenn diese die ausgewählte Seite das nächste Mal öffnen.
- **Löschen** – Sie können eine Seiten- oder Arbeitsbereichspersonalisierung für einen oder mehrere Benutzer löschen. Wählen Sie zunächst die Seite oder den Arbeitsbereich, dessen Personalisierung Sie löschen möchten. Wählen Sie dann die Benutzer in der Liste aller Benutzer aus oder filtern Sie nach einer bestimmten Rolle und wählen Sie dann die Benutzer in der Rolle aus. Klicken Sie auf **Löschen**, nachdem Sie eine Seite oder einen Arbeitsbereich sowie Benutzer ausgewählt haben. Alle Personalisierungen, die die ausgewählten Benutzer auf die ausgewählte Seite oder den ausgewählten Arbeitsbereich angewendet haben, werden gelöscht. Diese Aktion kann nicht rückgängig gemacht werden. Wenn die Seite oder der Arbeitsbereich eine gespeicherte Personalisierung hat, kann diese erneut importiert werden.




