---
title: Aufgabenaufzeichnung und Hilfe für Retail Modern POS (MPOS) und Cloud POS
description: In diesem Artikel wird beschrieben, wie Aufgabenaufzeichnung in Retail Modern POS und Cloud POS verwendet werden.
author: josaw1
ms.date: 06/19/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.custom: 1205393
ms.assetid: 2f13e9cf-55b5-458b-8c32-3f8cd98c9ecf
ms.search.industry: Retail
ms.search.form: RetailTerminalTable, SystemParameters
ms.openlocfilehash: 32d5c959c044a628a6ed1044b6e30f3363680293
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267457"
---
# <a name="task-recorder-and-help-for-retail-modern-pos-mpos-and-cloud-pos"></a>Aufgabenaufzeichnung und Hilfe für Retail Modern POS (MPOS) und Cloud POS

[!include [banner](includes/banner.md)]

In diesem Artikel wird beschrieben, wie Aufgabenaufzeichnung in Retail Modern POS und Cloud POS verwendet werden.

## <a name="overview"></a>Übersicht

Die Aufgabenaufzeichnung in Retail Modern POS oder Cloud POS ist eine neue Lösung, die mit einem Fokus auf hoher Reaktionsfähigkeit erstellt wurde. Sie bietet eine flexible Anwendungsprogrammierschnittstelle (API) zur Erweiterbarkeit und nahtlosen Integration mit Debitoren von Geschäftsprozessaufzeichnungen. Darüber hinaus ist die Integration der Aufgabenaufzeichnung im Tool Geschäftsprozessmodellierer (BPM) in Microsoft Dynamics Lifecycle Services ([https://bpm.lcs.dynamics.com](https://bpm.lcs.dynamics.com/)) vorverlegt worden. Daher können Benutzer weiterhin erweiterte Geschäftsprozessdiagramm aus Aufzeichnungen erstellen, um ihre Anwendungen zu analysieren und zu entwerfen.

## <a name="architecture"></a>Architektur

Aufgabenaufzeichnung kann Benutzeraktionen im Client mit exakter Genauigkeit erfassen. Jedes Steuerelement ist so instrumentiert, dass es die Aufgabenaufzeichnung über die Ausführung einer Benutzeraktion benachrichtigt. Das Steuerelement benachrichtigt die Aufgabenaufzeichnung, dass ein Ereignis aufgetreten ist und übermittelt alle relevanten Informationen über die entsprechende Benutzeraktion in Echtzeit. Aus diesen Informationen kann die Aufgabenaufzeichnung den Typ der Benutzeraktion erfassen (wie beispielsweise das Klicken auf eine Schaltfläche, die Werteingabe oder Navigation) und sämtliche Daten, die mit dieser Benutzeraktion zusammenhängen (wie der Wert und Typ der Eingabedaten, der Formularkontext oder der Datensatzkontext). Aufgabenaufzeichnung behält die Informationen mit genügend Details bei, um zu gewährleisten, dass durch eine Wiedergabe der Aufzeichnung die aufgezeichneten Aktionen genauso ausgeführt werden können, wie der Benutzer sie ausführte. (Die Wiedergabefunktion ist bei Retail Modern POS oder Cloud POS noch nicht implementiert worden.)

## <a name="basic-configuration"></a>Basiskonfiguration

Um die Aufgabenaufzeichnung in POS zu aktivieren, folgen Sie diesen Schritten.

1. Klicken Sie auf **Einzelhandel und Handel** &gt; **Kanaleinrichtung** &gt; **POS-Einrichtung** &gt; **Register**.
2. Klicken Sie auf das Register, damit dafür die Aufgabenaufzeichnung aktiviert wird.
3. Legen Sie auf der Registerkarte **Erfassen** im Inforegister **Allgemein** die Option **Aufgabenaufzeichnung aktivieren** auf **Ja** fest.
4. Klicken Sie auf **Speichern**.
5. Gehen Sie zu **Retail and Commerce** &gt; **Retail and Commerce IT** &gt; **Vertriebsplan**.
6. Wählen Sie den Einzelvorgang **Register (1090)** aus, und klicken Sie dann auf **Jetzt ausführen**.

## <a name="create-a-recording"></a>Eine Aufzeichnung erstellen

Gehen Sie folgendermaßen vor, um eine neue Erfassung mithilfe der Aufgabenaufzeichnung zu erstellen.

1. Starten Sie Retail Modern POS oder Cloud POS, und melden Sie sich an.
2. Auf der Seite **Einstellungen** im Abschnitt **Aufgabenaufzeichnung** klicken Sie auf **Aufgabenaufzeichnung öffnen**. Der Bereich **Aufgabenaufzeichnung** wird angezeigt. Sie können auf die Schaltfläche **Schließen** (**X**) in der oberen rechten Ecke klicken, um den Bereich **Aufgabenaufzeichnung** zu schließen, bevor Sie eine neue Aufzeichnung beginnen. Wiederholen Sie Schritt 2, um den Bereich erneut zu öffnen.

    [![Aufgabenaufzeichnungsbereich.](./media/newrecording-1024x450.jpg)](./media/newrecording.jpg)

3. Geben Sie einen Namen und eine Beschreibung für die Aufzeichnung ein, und klicken Sie dann auf **Starten**. Die Aufzeichnungssitzung beginnt, sobald Sie auf **Starten** klicken.

    > [!NOTE]
    > Hinweis: Wenn Sie auf die Schaltfläche **Schließen** (**X**) in der oberen rechten Ecke klicken, während sich die Aufzeichnung in Bearbeitung befindet, wird der Bereich **Aufgabenaufzeichnung** geschlossen, aber die Aufzeichnungssitzung ist noch nicht beendet. Um den Aufgabenaufzeichnungsbereich erneut zu öffnen, klicken Sie auf die Schaltfläche **Hilfe** (Fragezeichen) am oberen Rand des Bildschirms.
    >
    > [![Fragezeichen.](./media/help.jpg)](./media/help.jpg)

4. Nachdem Sie auf **Starten** klicken, tritt die Aufgabenaufzeichnung in den Aufzeichnungsmodus ein. Der Bereich **Aufgabenaufzeichnung** zeigt Informationen und Steuerelemente an, die dem Aufzeichnungsprozess zugeordnet sind.
5. Führen Sie die Aktionen aus, die Sie in der Benutzeroberfläche (UI) von Retail Modern POS oder Cloud POS ausführen möchten.
6. Um die Aufzeichnungssitzung zu beenden, klicken Sie auf **Beenden**.

## <a name="download-options"></a>Downloadoptionen

Nachdem Sie die Aufzeichnungssitzung beenden, werden mehrere Optionen angezeigt, sodass Sie die Aufzeichnung herunterladen können.

[![Downloadoptionen.](./media/downlaod-options.jpg)](./media/downlaod-options.jpg)

### <a name="save-to-this-pc"></a>Auf diesem PC speichern

Sie können das Aufzeichnungspaket verwenden, um einen Aufgabenleitfaden wiederzugeben, die Aufzeichnung zu verwalten oder Anmerkungen in der Aufzeichnung zu bearbeiten. (Diese Funktion ist in Retail Modern POS oder Cloud POS noch nicht implementiert worden.)

### <a name="export-as-word-document"></a>Als Word-Dokument exportieren

Sie können die Aufzeichnung als Microsoft Word-Dokument speichern. Das Dokument enthält die aufgezeichneten Schritte und die Bildschirmabbilder, die erfasst wurden.

### <a name="save-as-developer-recording"></a>Als Entwickleraufzeichnung speichern

Die Rohdatendatei der Aufzeichnung wird für Entwicklerszenarien nützlich sein, wie beispielsweise die Testcodegenerierung. (Diese Funktion ist noch nicht implementiert worden.)

## <a name="recording-controls"></a>Aufzeichnungssteuerelemente

[![Aufzeichnungssteuerelemente.](./media/controls.jpg)](./media/controls.jpg)

### <a name="stop"></a>Stopp

Klicken Sie auf **Beenden**, um die Aufzeichnungssitzung zu beenden. Beachten Sie, dass Sie eine Sitzung nicht neu starten können, nachdem Sie sie beendet haben. Achten Sie deshalb darauf, dass die Aufzeichnung abgeschlossen ist, bevor Sie sie beenden.

### <a name="pause"></a>Anhalten

Klicken Sie auf **Anhalten**, um die Aufzeichnungssitzung vorübergehend zu beenden (anzuhalten) und mit dem Vorgang fortzufahren. Schritte, die Sie ausführen, nachdem Sie auf **Anhalten** klicken, werden nicht aufgezeichnet.

### <a name="continue"></a>Fortfahren

Um die Aufzeichnungssitzung fortzusetzen, nachdem Sie sie angehalten hatten, klicken Sie auf **Weiter**.

### <a name="capture-screenshots"></a>Bildschirmabbilder erstellen

Aufgabenaufzeichnung kann Bildschirmabbilder der Benutzeroberfläche von Retail Modern POS erfassen, während Sie einen Geschäftsprozess aufzeichnen. Um die Erfassungsfunktion für Bildschirmfotos zu aktivieren, legen Sie die Option **Bildschirmfotos erstellen** auf **Ja** fest, und nehmen Sie dann die Erfassung vor. Sobald die Erfassung abgeschlossen wurde, klicken Sie auf **Beenden** und laden Sie das Word-Dokument herunter. Das Dokument enthält die Schritte mit den relevanten Bildschirmfotos.

> [!NOTE]
> Die Capture Screenshot-Funktionalität wird in Store Commerce, Commerce Modern POS und Cloud POS nicht unterstützt.

### <a name="start-task-and-end-task"></a>Aufgabe starten und Aufgabe beenden

Sie können den Beginn und das Ende eines Satzes gruppierter Schritte angeben, indem Sie die Schaltflächen **Aufgabe starten** und **Aufgabe** **beenden** verwenden. Klicken Sie **Aufgabe starten**, um einen Schritt zu „Aufgabe starten” hinzuzufügen und dann die Schritte auszuführen, die in diese Gruppe einbezogen werden sollten. Nachdem Sie das Ausführen der Schritte für diese Gruppe abgeschlossen haben, klicken Sie auf **Aufgabe beenden**. Aufgaben unterstützen Sie beim Organisieren Ihrer Prozeduren. Aufgaben können in andere Aufgaben geschachtelt werden. Auf diese Weise können Sie besser sehr lange und komplexe Geschäftsprozesse organisieren.

## <a name="adding-annotations"></a>Hinzufügen von Anmerkungen

Eine Anmerkung ist zusätzlicher Text, den Sie einem Schritt in einer Aufzeichnung hinzufügen. Beispielsweise können Sie Anmerkungen verwenden, um dem Benutzer mehr Kontext oder Anweisungen zu erteilen. Sie können Anmerkungen vor oder nach einem Schritt hinzufügen. Sie können eine Anmerkung jedem beliebigen Schritt hinzufügen, indem Sie auf die Schaltfläche **Bearbeiten** (Bleistiftsymbol) auf der rechten Seite des Schrittes klicken.

[![Bearbeitungsschaltfläche für einen Schritt.](./media/annotate.jpg)](./media/annotate.jpg)

### <a name="texts-and-notes"></a>Texte und Hinweise

Sie können die Felder **Texte** und **Hinweise** verwenden, um Text hinzuzufügen, der einem Schritt in einem Aufgabenleitfaden zugeordnet werden soll.

[![Text- und Hinweisfelder.](./media/annotatesteps.jpg)](./media/annotatesteps.jpg)

#### <a name="text"></a>Text

Text, den Sie in das Feld **Text** eingeben, wird *über* dem Schritttext im Aufgabenleitfaden angezeigt. Diese Stelle ist geeignet für Text, den die Benutzer nach Ihren Wünschen lesen sollen, bevor sie den Schritt abschließen.

#### <a name="notes"></a>Notizen

Text, den Sie in das Feld **Hinweise** eingeben, wird *unter* dem Schritttext im Aufgabenleitfaden angezeigt. Um den Hinweistext zu lesen, muss der Benutzer den Schritttext im Popupfenster erweitern. Diese Stelle ist für optionales Lesematerial oder andere Informationen geeignet, die für den Benutzer nützlich sein können, die der Benutzer aber nicht benötigt, um die Aktion abzuschließen.

## <a name="help-in-retail-modern-pos-and-cloud-pos"></a>Direkthilfe in Retail Modern POS und Cloud POS

Damit Ihre eigenen benutzerdefinierten Aufgabenaufzeichnungen im Hilfebereich von Retail Modern POS und Cloud POS angezeigt werden, sodass sie als Text angezeigt werden können, müssen Sie die Aufgabenaufzeichnungen in Ihrer eigenen BPM-Bibliothek speichern und Ihre Hilfesystemparameter so aktualisieren, dass sie auf die BPM-Bibliothek verweisen. Weitere Informationen finden Sie unter [Hilfesystem verbinden.](../fin-ops-core/fin-ops/get-started/help-connect.md). Retail Modern POS und Cloud POS-Hilfe durchsucht LCS in Echtzeit. Es durchsucht alle BPM-Bibliotheken, die in den Commerce-Hilfesystemparametern ausgewählt sind, und zeigt die relevanten Ergebnisse an. Um auf das Menü **Hilfe** zuzugreifen, klicken Sie auf die Schaltfläche **Hilfe** (Fragezeichen) am oberen Rand des Bildschirms, und dann im Suchfeld geben Sie Ihren Prozessname ein und klicken auf die Suchschaltfläche.

[![Schaltfläche „Hilfe“.](./media/help.jpg)](./media/help.jpg)

Wenn Sie auf einen Aufgabenleitfaden in den Suchergebnissen klicken, können Sie entweder die Schritte als Hilfeartikel anzeigen oder die Schritte in ein Word-Dokument exportieren.

> [!NOTE]
> Hilfe in modernem Retail Modern POS und Cloud POS zeigt Aufgabenleitfäden nicht entsprechend der Form oder dem Arbeitsgang an, bei dem Sie sich befinden. Sie müssen den Prozeßnamen im Suchfeld eingeben und dann **Suchen** klicken.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
