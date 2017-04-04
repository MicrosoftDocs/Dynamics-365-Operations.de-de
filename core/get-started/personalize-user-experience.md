---
title: Personalisierung der Benutzerumgebung
description: "In diesem Artikel wird beschrieben, wie Sie Microsoft Dynamics 365 für Arbeitsgänge anpassen können."
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SysUserSetup
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 62363
ms.assetid: 57b445d7-3e9e-4228-8728-f63b9dbd77a3
ms.search.region: Global
ms.author: tlefor
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4bb647cfd3f012efbffa93a81462c538a24ac850
ms.openlocfilehash: 8965c193839002776b3c61036b23b54625c974a4
ms.lasthandoff: 03/31/2017


---

# <a name="personalize-the-user-experience"></a>Personalisierung der Benutzerumgebung

In diesem Artikel wird beschrieben, wie Sie Microsoft Dynamics 365 für Arbeitsgänge anpassen können.

Es gibt viele Arten Personalisierungen in Microsoft Dynamics 365 für Arbeitsgänge. Einige Personalisierungen sind Auswahlen, die Sie in einer Liste an Optionen auf einer Einstellungsseite vornehmen. Einige sind Personalisierungen implizit werden, z Dynamics 365 für Arbeitsgänge die Breite Raster spalten aus, falls Sie diese anpassen, von erweitertem und/reduziertem Bundesland von Inforegistern nachverfolgt. Andere Personalisierungen sind explizit. Für explizite Personalisierungen treten Sie in einen interaktiven Personalisierungsmodus ein und ändern die Darstellung einer Seite, indem Sie direkt verwalten, wie Elemente auf der Seite angezeigt oder agieren. 

Alle Personalisierungen, jedes beliebigen Typs, die ein Benutzer in Dynamics 365 für Arbeitsgänge wird, sind nur für diesen Benutzer, unabhängig vom Unternehmen, dem der Benutzer in gesteuert wird. Änderungen, die ein Benutzer an einer Seite vornimmt, haben keine Auswirkungen auf andere Benutzer im System.

## <a name="systemwide-options-for-the-current-user"></a>Systemweite den aktuellen Optionen für Benutzer
In der Navigationsleiste sehen Sie ein Zahnrad, das als Menüschaltfläche **Einstellungen** bezeichnet wird. Durch Öffnen des Menüs **Einstellungen** werden einige Optionen angezeigt. Durch Auswählen von **Optionen** wird die Seite **Benutzeroptionen** geöffnet. Dort finden Sie vier Optionsregisterkarten: **Visuell**, **Voreinstellungen**, **Konto** und **Workflow**.

-   **Visuell: ** Wird verwendet, um ein Farbenthema und die standardmäßige Größe der Elemente auf den Seiten auszuwählen.
-   ** Einstellungen: ** Hier können Sie Standardeinstellungen für auswählen, wenn Sie Dynamics 365 für Arbeitsgänge, einschließlich der Unternehmen, die erste Seite und die Standardansicht/den Bearbeitungsmodus öffnen (durch, wenn eine Seite zum Anzeigen gesperrt ist, oder geöffnet für Sie jedes Mal bearbeiten Sie es öffnen.) Sie finden auch Optionen für Sprache, Zeitzone, Datum, Uhrzeit und Zahlenformat. Schließlich enthält diese Seite mehrere verschiedene Voreinstellungen, die von Freigabe zu Freigabe variieren.
-   **Konto: **Wird verwendet, um Ihre Benutzerkennung und andere kontobezogene Optionen bereitzustellen.
-   **Workflow: **Hier können Sie workflowbezogene Optionen auswählen.

## <a name="implicit-personalizations"></a>Implizite Personalisierungen
Implizite Personalisierungen sind die Personalisierungen, die Sie ausführen, indem Sie einfach mit bestimmten Steuerelementen interagieren, die sich an ihren aktuell sichtbaren Status erinnern. 

**Rasterspalten:** Sie können die Breite einer Spalte in einer Liste anpassen, indem Sie die Größenänderungsleiste links oder rechts des Spaltenkopfs auswählen und sie nach links oder rechts auf die gewünschte Breite schieben. Dynamics 365 für Arbeitsgänge speichert die Breite, die Sie möchten und dieser Spalte mit dieser Breite jedes Mal Sie zum Anzeigen der Seite mit dieser Liste öffnen Sie. 

**Inforegister:** Einige Seiten haben erweiterbare Abschnitte, die als Inforegister bezeichnet werden. Dynamics 365 für Arbeitsgänge, werden die Inforegister Sie erweitert haben und die Inforegister Sie verringert haben. Jedes Mal, wenn Sie zur Seite zurückkehren, werden diese gleichen Inforegister auf Grundlage der letzten Nutzung erweitert oder reduziert. In diesem Artikel erklären wir, wie die Reihenfolge Ihrer Inforegisterabschnitte geändert werden kann. In einigen Fällen werden möglicherweise das Reduzieren des Inforegisters Leistung, da Dynamics 365 für Arbeitsgänge nicht bei, um die Informationen für dieses Inforegister ab, bis das Inforegister erweitert ist. 

**Infoboxen:** Einige Seiten haben einen Abschnitt, der als Infoboxbereich bezeichnet wird. Dieser Bereich enthält schreibgeschütztes Informationen zum aktuellen Betreff der Seite. Jedem Abschnitt im Infoboxbereich wird als Infobox bezeichnet. Sie können Geldbeträge erweitern, oder, eine Infobox und Dynamics 365 zu reduzieren für Arbeitsgänge speichert diese Einstellungen. In einigen Fällen werden das Reduzieren kann eine Infobox Leistung, da Dynamics 365 für Arbeitsgänge nicht bei, um die Informationen für diese Infobox ab, bis die Infobox erweitert ist.

## <a name="explicit-personalizations-using-the-personalization-toolbar"></a>Explizite Personalisierungen mithilfe der Personalisierungssymbolleiste
Jede Person und jedes Unternehmen hat eine unterschiedliche Meinung dazu, welche Daten für sie bzw. es am wichtigsten sind, oder welche Daten nicht für die Art und Weise erforderlich sind, wie sie ihr Geschäft führen. Die Möglichkeit, so anzupassen Ihre Informationen bestellt wird, eingewirkt auf, ausgeblendet oder sogar der Herstellung ist Dynamics 365 für Arbeitsgänge einer persönlichen produktiven und Erfahrung " aktivierte Funktionen. 

Explizite Personalisierungen stehen die Personalisierungen, denen Sie explizit mit der Absicht ausgeführt werden, um die Darstellungsweise oder das Verhalten eines Elements oder der Seite zu ändern, indem Sie ein Personalisierungsmenü auswählen. Der Typ der grundlegendste expliziten Personalisierung ist, wo Sie auf ein Element mit der rechten Maustaste klicken und auswählen ** personalisieren Sie **. "Hinweis, dass nicht alle Elemente auf der Seite kann personalisiert werden.) Bei dieser Methode die Personalisierung auswählen, werden das Eigenschaftenfenster des Elements. 

[![an![die Eigenschaften eines Elements Verwendungsweise] ". /media/personalization-element-properties.jpg)]". /media/personalization-element-properties.jpg) 

So personalisieren Sie ein Element auf Ihrer Seite, wenn Sie nur die Bezeichnung des Elements ändern möchten, das Element ausblenden möchten, damit es nicht auf der Seite angezeigt wird (dies ändert keine Daten, es werden lediglich Ihre Informationen nicht angezeigt), die Informationen in die Zusammenfassung des Inforegisters aufnehmen möchten (wenn das Element in einem Inforegister enthalten ist), das Feld mit der Tabulatortaste überspringen möchten oder es als „Nicht bearbeiten“ markieren, damit Daten nicht geändert werden können. 

Wenn Sie Elemente verschieben oder ausblenden oder mehrere Änderungen vornehmen möchten, können Sie die Personalisierungssymbolleiste verwenden, die im Eigenschaftenfenster der Elemente verfügbar ist, indem Sie **Dieses Formular personalisieren** auswählen. Die Personalisierungssymbolleiste ist auch im Aktivitätsbereich des Formulars verfügbar, unter der Personalisierungsgruppe der Registerkarte **Optionen**. Wählen Sie **Dieses Formular personalisieren**,und die Personalisierungssymbolleiste wird angezeigt. 

![Personalisierungssymbolleiste( [] . /media/personalization-personalizationtoolbar.jpg)]". /media/personalization-personalizationtoolbar.jpg)

Die Personalisierungssymbolleiste weist mehrere Personalisierungsaktivitäten. Wählen Sie das Tool **Auswählen**, wenn Sie die Eigenschaften viele Elemente einzeln auswählen und ändern möchten. Klicken Sie zuerst auf das Tool „Auswählen“, und klicken Sie anschließend auf das Element, dessen Eigenschaften Sie ändern möchten. Wenn Sie ein Element auswählen, wird das Eigenschaftenfenster des Elements geöffnet, und Sie können beliebige Eigenschaften für dieses Element ändern. Sie können den Prozess für andere Elemente auf Ihrem Formular wiederholen, die personalisierbar sind. In einigen Fällen wählen Sie ein Element aus und stellen fest, dass einige der Eigenschaften nicht geändert werden können. Dies bedeutet, dass auf der Methode basieren das Stromanpassungsglied verwendet werden, Dynamics 365 für Arbeitsgänge können Sie über diese Eigenschaft nicht ändern lassen. Sie können beispielsweise kein Feld ausblenden, das erforderlich ist. 

Wählen Sie das Tool **Umlagern** aus, wenn Sie ein Element auswählen und an einen anderen Lagerplatz innerhalb der aktuellen Elementgruppe umlagern möchten. (Sie können kein Element außerhalb seiner übergeordneten Gruppe verschieben.) Klicken Sie zuerst auf das Tool „Umlagern“ und anschließend auf das Element, das Sie verschieben möchten. Wenn Sie auf das Element klicken, die Sie verschieben möchten, überwacht Dynamics 365 für Arbeitsgänge des Formulars, um, bei denen das Element "verschoben werden und eine Reihe von Abstiegszonen" diese angezeigt als farbige, fette Position erstellen kann neben den Bereich zu veranschaulichen, in dem das Element als Sie werden verworfen ziehen kann das Element rund innerhalb der aktuellen Gruppe. 

Wählen Sie das Tool **Ausblenden**, um ein Element auszuwählen und auszublenden. Um ein Element auszublenden, wählen Sie einfach das Tool „Ausblenden“, und klicken Sie auf das Element, das Sie ausblenden möchten. Wenn Sie das Tool „Ausblenden“ auswählen, werden alle aktuell ausgeblendeten Elemente sichtbar gemacht und in einem schattierten Container angezeigt, damit Sie das Element auswählen können, um es einzublenden. Wählen Sie das Tool „Auswählen“, um zu sehen, wie die Seite mit den ausgewählten Elementen ausgeblendet aussehen wird. Wählen Sie das Tool **Zusammenfassung** aus, wenn Sie ein numerisches oder Zeichenfolgenfeld im Zusammenfassungsbereich des Inforegisters anzeigen möchten. Das Tool „Zusammenfassung“ gilt nur für Felder, die innerhalb eines Inforegisterabschnitts enthalten sind. Wenn Sie das Tool zusammenfassende auswählen, zeigt Dynamics 365 für alle Arbeitsgänge Felder an, die als die Felder ausgewählt wurden, indem sie in schattierten einen Container. einschloss Sie können Felder aus einer Inforegisterzusammenfassung interaktiv hinzufügen und entfernen, indem Sie auf das Feld klicken. 

Wählen ** ** Hiermit überspringen Sie das Tool, um ein Element aus der Tastaturtabulatorsequenz der Seite zu entfernen. Wenn Sie das Überspringentool auswählen, werden alle derzeit übersprungenen Elemente in einem in schattierten Container angezeigt, damit Sie diese erneut auswählen können, um sie Teil von der Tabulatorsequenz zu erstellen, indem Sie ein übersprungenes Element auswählen. 

Wählen Sie das Tool **Bearbeiten** aus, wenn Sie ein Element als „Bearbeitbar“ oder „Nicht bearbeitbar“ markieren wollen. Wenn Sie das Tool „Bearbeiten“ auswählen, werden alle aktuell nicht bearbeitbaren Elemente sichtbar gemacht und in einem schattierten Container angezeigt, damit Sie sie auswählen können, um sie bearbeitbar zu machen. Beachten Sie: Mehrere Felder sind obligatorisch und können nicht als nicht bearbeitbar festgelegt werden. Diese Felder werden mit einem Vorhängeschlosssymbol angezeigt. 

Wählen Sie das Tool **Hinzufügen**, um ein Feld zur Seite hinzuzufügen. Mit dem Tool „Hinzufügen“ können Sie kein neues Feld erstellen, Sie können aber Felder hinzufügen, die Teil der aktuellen Seitendefinition sind, aber nicht auf der Seite dargestellt werden. Wenn Sie das Tool „Hinzufügen“ auswählen, müssen Sie zunächst die Gruppe oder den Bereich auswählen, der bzw. dem Sie ein Feld hinzufügen möchten. Ein Dialogfeld wird in der Liste der Felder angezeigt, die dem Bereich zugeordnet sind, den Sie ausgewählt haben. In diesem Dialogfeld können Sie ein oder mehrere Felder zum Hinzufügen auswählen und auf „Einfügen“ klicken. Wenn Sie später ein Feld entfernen möchten, das Sie zuvor hinzugefügt haben, wiederholen Sie den Prozess, aber deaktivieren Sie einfach das Feld, das Sie zuvor hinzugefügt haben. 

Wählen Sie die ** Verwalten ** Schaltfläche, um eine Liste der zu Verwaltungsoptionen finden, die für alle Personalisierungen für die aktuelle Seite zugeordnet werden. 

Wählen Sie ** deaktivieren Sie ** um die Seite zu dem Standard, installiertes Bundesland zurückzusetzen. Alle Personalisierungen auf der aktuellen Seite sind deaktiviert. Es gibt keine rückgängig gemachte Aktion, können so nur diese Option, wenn Sie sicher sind, die Seite zurücksetzen möchten. 

Wählen Sie **Importieren**, um eine Personalisierung aus einer Personalisierungsdatei zu verwenden, die Sie oder eine andere Person zuvor für diese Seite erstellt haben. Durch das Importieren einer Personalisierung werden alle Personalisierungen gelöscht, die Sie auf der gesamten Seite ausgeführt haben, und stattdessen werden alle Personalisierungen aus der ausgewählten Datei verwendet. Wenn Sie eine Personalisierung speichern oder freigeben möchten, wählen Sie die Option **Exportieren** aus, um die Personalisierungen in einer Datei zu speichern. 

Wählen Sie die Schaltfläche **Schließen**, um die Symbolleiste zu schließen und die Seite wieder in den interaktiven Status zurückzuversetzen. 

Bei der Personalisierungssymbolleiste ist das Speichern implizit. Ihre Personalisierungen sind sofort wirksam, wenn sie vornehmen, und es ist nicht erforderlich, auf die Schaltfläche **Speichern** zu klicken. Manchmal finden Sie ein Vorhängeschlosssymbol neben einem Element ein Tool, wenn Sie auswählen. Das bedeutet das, damit die Seite, funktioniert einwandfrei, wie Sie die Eigenschaften nicht ändern können, die dem ausgewählten zugeordnet Tool werden. Wenn die Personalisierungssymbolleiste geöffnet wird, wird die Seite nicht interaktiv. Sie können keine Daten eingeben oder Abschnitte erweitern oder reduzieren.

## <a name="explicit-personalization-adding-a-tile-or-list-to-a-workspace"></a>Explizite Personalisierung: Hinzufügen einer Kachel oder Liste zu einem Arbeitsbereich
Einige Seiten mit Listen haben eine zusätzliche Personalisierungsfunktion innerhalb des Aktivitätsbereichs, unter der Personalisierensgruppe der Registerkarte „Optionen“. Wählen Sie **Zum Arbeitsbereich hinzufügen** aus, um die Dropdownliste zu öffnen, die Ihnen die Möglichkeit gibt, die Informationen in der aktuellen Liste (gefiltert und sortiert oder Standard) in einen Arbeitsbereich als Liste oder Zusammenfassungskachel anzuzeigen (diese kann verwendet werden, um die Anzahl der Artikel in der Liste anzuzeigen). 

[![Add to workspace](./media/personalization-addtoworkspace.png)](./media/personalization-addtoworkspace.png) 

Um eine Liste zu einem Arbeitsbereich hinzuzufügen, sortieren oder filtern Sie zuerst die Liste mit diesen Informationen so, wie sie in Ihrem Arbeitsbereich angezeigt werden sollen. Wählen Sie dann das Dialogfeld „Zum Arbeitsbereich hinzufügen“ aus. Danach wählen Sie den gewünschten Arbeitsbereich aus und wählen **Liste** aus der Präsentationsdropdownliste aus. Wenn Sie **Liste** auswählen, wird ein Dialogfeld geöffnet, in dem Sie die Spalten auswählen können, die Sie in der Liste anzeigen möchten, sowie die Beschriftung für die Liste, wie sie im Arbeitsbereich angezeigt wird. 

Um eine Kachel zu einem Arbeitsbereich hinzuzufügen, filtern Sie zuerst die Liste, um die Daten darzustellen, die Sie zusammenfassen möchten (oder schnellen Zugriff darauf wünschen). Öffnen Sie anschließend das Dialogfeld „Zum Arbeitsbereich hinzufügen“. Danach wählen Sie den gewünschten Arbeitsbereich aus und wählen **Kachel** aus der Präsentationsdropdownliste aus. Wenn Sie **Kachel** auswählen, wird ein Dialogfeld angezeigt, in dem Sie eine Kachelbeschriftung angeben und entscheiden können, ob die Kachel eine Zahl anzeigt. Wenn die Kachel auf einen Arbeitsbereich platziert ist, können Sie die aktuelle Seite über den Arbeitsbereich öffnen und die Liste der Informationen in Bezug auf die Kachel anzeigen. 

Wenn die Liste oder Kachel zu einem Arbeitsbereich hinzugefügt wird, können Sie diesen Arbeitsbereich öffnen und die Liste oder Kachel in der Gruppe neu anordnen, in der sie platziert wurde.

## <a name="explicit-personalization-adding-a-summary-from-a-workspace-to-a-dashboard"></a>Explizite Personalisierung: Hinzufügen einer Zusammenfassung aus einem Arbeitsbereich zu einem Dashboard
Einige Arbeitsbereiche enthalten die Anzahl kacheln (Kacheln mit Zahlen für sie diese) möchten Sie auch in Ihrem Dashboard finden. In ein Arbeitsbereich auf eine Anzahlkachel mit der rechten Maustaste und wählen Sie aus ** personalisieren Sie **. Wählen Sie **An Dashboard anheften** aus. Das nächste Mal, wenn Sie zum ausgewählten Dashboard navigieren (und es aktualisieren), finden Sie die Zahl unter der Navigationskachel dieses Arbeitsbereichs im Dashboard.

## <a name="explicit-personalization-personalizing-your-dashboard"></a>Explizite Personalisierung: Personalisieren des Dashboards
Dashboard Das ist häufig die erste Seite, die Sie sehen, wenn Sie Dynamics 365 für Arbeitsgänge öffnen. Sie können das Dashboard personalisieren, um die Arbeitsbereichsnavigationskacheln umzubenennen, um nur nur Kacheln anzuzeigen, die Sie sehen möchten, um die Kacheln umzubenennen oder um die Kacheln in der Reihenfolge anzuordnen, in der Sie sie sehen möchten. Um das Dashboard zu personalisieren, wählen Sie eine beliebige Kachel aus und klicken Sie mit der rechten Maustaste, um ein Kontextmenü zu öffnen. Wählen Sie im Kontextmenü **Anpassen** aus. Wenn die ausgewählte Kachel eine ist, die Sie ausblenden oder umbenennen oder übersprungen möchten, können Sie diese Änderung direkt im anzeigten Eigenschaftenfenster vornehmen. Wenn Sie die Kacheln anordnen möchten, wählen Sie **Dieses Formular personalisieren** im Eigenschaftenfenster aus, um die Personalisierungssymbolleiste zu öffnen. Sie können das Tool „Umlagern“ dann verwenden, um die Kacheln anzuordnen.

## <a name="administration-of-personalization"></a>Verwalten der Personalisierung
Es ist möglich, eine Seite zu personalisieren und sie für andere Benutzer freizugeben, indem Sie einfach die personalisierte Seite exportieren und die anderen Benutzer auffordern, zur personalisierten Seite zu navigieren und die Personalisierungsdatei zu importieren, die Sie erstellt haben. Wenn ein Benutzer Administratorrechte besitzt, können sie die Personalisierungen auch für andere Benutzer in der Seite **Personalisierungseinstellung** verwalten. Navigieren Sie zur b-Seite. Auf der Seite **Personalisierung** finden Sie zwei Registerkarten, **System** und** Benutzer**. 

**System:** Hier können Sie vorübergehend alle Personalisierungen im System deaktivieren oder „ausschalten“. Damit werden die Personalisierungen nicht gelöscht, stattdessen werden alle Formulare auf ihren Standardstatus zurückgesetzt. Sie können Personalisierung später erneut aktivieren, damit alle Personalisierungen erneut auf die einzelnen Benutzerformulare angewendet werden. Sie können auch Personalisierungen für alle Benutzer löschen. Beachten Sie, dass wenn Sie Personalisierungen löschen, keine Möglichkeit besteht, Personalisierungen vom System automatisch zu aktivieren. Stellen Sie sicher, dass sie Personalisierungen exportiert haben, die Sie vielleicht später importieren möchten, bevor Sie diesen Schritt durchführen. 

**Benutzer:** Hier können Sie für jeden Benutzer entscheiden, ob er eine implizite oder explizite Personalisierung ausführen kann. Sie können auch entscheiden, ob jeder Benutzer implizite oder explizite Personalisierungen an einem bestimmten Formular ausführen kann. Zuletzt können Sie eine Personalisierung für jeden Benutzer importieren oder exportieren oder löschen. 

**Hinweis:** In der ersten Version ermöglicht die Personalisierungsverwaltung nur die Verwaltung eines Benutzers auf Benutzerbasis.


