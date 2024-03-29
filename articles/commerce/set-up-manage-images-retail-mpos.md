---
title: Einrichten und Verwalten von Modern POS (MPOS)
description: In diesem Artikel wird beschrieben, welche Schritte beim Einrichten und Verwalten von Bildern für die verschiedenen Entitäten, die in Modern POS (MPOS) erscheinen, erforderlich sind.
author: josaw1
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.custom: 52851
ms.assetid: 5c21385e-64e0-4091-98fa-6a662eb33010
ms.search.industry: Retail
ms.search.form: RetailChannelProfile, RetailMediaGallery, RetailImages,
ms.openlocfilehash: d334701b2865a4f19365a2773641e324326b02e3
ms.sourcegitcommit: 78cbb125f20a33df38bda0546203b8f837cbcd93
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/09/2022
ms.locfileid: "9751939"
---
# <a name="set-up-and-manage-images-for-modern-pos-mpos"></a>Einrichten und Verwalten von Modern POS (MPOS)

[!include [banner](includes/banner.md)]

In diesem Artikel wird beschrieben, welche Schritte beim Einrichten und Verwalten von Bildern für die verschiedenen Entitäten, die in Modern POS (MPOS) erscheinen, erforderlich sind.

## <a name="setting-up-the-media-base-url-and-defining-media-templates-to-configure-the-format-for-image-urls"></a>Die URL für die Medienbasis festlegen und die Medienvorlagen bestimmen, um das Format für die Bild-URL einrichten.

Die Bilder, die in Modern POS (MPOS) angezeigt werden, müssen extern, außerhalb von Commerce, gehostet werden. In der Regel werden sie auf einem Content Management-System, auf einem Content Delivery Network (CDN) oder einem Medienserver gehostet. MPOS ruft dann die Bilder von den entsprechenden Einheiten wie Produkten und Kataloge ab und zeigt sie an, indem es auf die Ziel URL zugreift. Um diese extern gehosteten Bilder abzurufen, braucht MPOS das korrekte URL-Format für die Bilder. Sie können das erforderliche URL-Format für Bilder konfigurieren, indem Sie den Wert für die **medienbasierte URL** im Kanalprofil einrichten und die Funktionen **Medienvorlage definieren** für jede Entität verwenden. Sie können das Format der Standard-URL für eine Teilmenge von Entitäten auch überschreiben, indem Sie dies Funktion **In Excel bearbeiten** verwenden.

> [!IMPORTANT]
> In der aktuellen Version von Commerce können Sie das URL-Format nicht mehr mithilfe des **Image**-Attributs XML für MPOS in der Attributgruppe **Standard** für Entitäten einrichten. Wenn Sie mit Microsoft Dynamics AX 2012 R3 vertraut sind und nun die aktuelle Version von Commerce verwenden, stellen Sie sicher, dass Sie immer die neuen Funktionen **Medienvorlage definieren** zum Einrichten von Bildern benutzen. Verwenden oder ändern Sie auf keinen Fall das Attribut **Bild** in der **Standard**-Attributengruppe für Entitäten, einschließlich Produkte. Änderungen, die Sie direkt in der Attributgruppe **Standard** für Bilder machen, werden nicht abgebildet. Diese Option wird in einer späteren Version deaktiviert.

In den folgenden Verfahren werden Bilder für die Katalogentität als Beispiel genannte. Diese Verfahren helfen sicherzustellen, dass der korrekte Bildzielpfad implizit für alle Katalogbilder festgelegt wird, die einen allgemeinen Pfad folgen. Wenn Sie beispielsweise einen Medienserver oder ein CDN extern eingerichtet haben und möchten, dass die Bilder in MPOS für eine angegebenen Filiale angezeigt werden, wird Ihnen die Funktionalität **Medienvorlage definieren** helfen, den Pfad festzulegen, von dem MPOS Bilder suchen und holen kann.

> [!NOTE]
> Für dieses Demodatenbeispiel wird der Medienserver in der Commerce Scale Unit bereitgestellt. Allerdings können Sie ihn an einer beliebigen Stelle außerhalb von Commerce haben.

### <a name="set-up-the-media-base-url-for-a-channel"></a>Die medienbasierte URL für einen Kanal einrichten

1. Öffnen Sie das Commerce HQ-Portal.
2. Klicken Sie auf **Einzelhandel und Handel** &gt; **Kanaleinrichtung** &gt; **Kanalprofile**.

    [![Navigation.](./media/channel-profile1.png)](./media/channel-profile1.png)

3. Im Kanalprofil, das Ihr Shop für MPOS verwendet, aktualisieren Sie das Feld mit der **Medienbasierten URL** mit der Basis-URL von Ihrem Medienserver oder CDN. Die Basis-URL ist der erste Teil der URL, die von allen Bildordner von andere Entitäten freigegeben wird.

    [![Kanalprofilseite.](./media/channel-profile2.png)](./media/channel-profile2.png)

### <a name="define-the-media-template-for-an-entity"></a>Definieren Sie die Medienvorlage für eine Entität

1. Klicken Sie auf **Einzelhandel und Handel** &gt; **Katalogverwaltung** &gt; **Katalogbilder**.
2. Klicken Sie auf der Seite **Katalogbilder** den Aktivitätsbereich und klicken Sie **Medienvorlage definieren** an. Im Dialogfeld **Medienvorlage definieren** im Feld **Entität** **Katalog** sollte die Option standardmäßig ausgewählt werden.
3. Geben Sie im Inforegister **Medienpfad** den verbleibenden Pfad des Bildlagerplatzes ein. Die Medienpfad unterstützt **LanguageID** als Variable. Sie können beispielswiese für die Demodaten einen Ordner **Kataloge** für alle Katalogbilder unter der medienbasierten URL für Ihren Medienserver erstellen (`https://testax3ret.cloud.test.dynamics.com/RetailServer/MediaServer`). Sie können dann einen Ordner für jede Sprache haben, wie en-US oder fr-FR und dann die entsprechenden Bilder in jedem Ordner entsprechend speichern. Wenn Sie keine verschiedenen Bilder für die unterschiedlichen Sprachen haben, können Sie die Variablen **LanguageID** aus Ihrer Ordnerstruktur übergehen und direkt zum Katalogordner gehen, der die Katalogbilder enthält.

    > [!NOTE]
    > Die aktuelle Version von Commerce unterstützt das Token **{LanguageId}** für Katalog-, Produkt- und Kategorieentitäten. (Der Token **{LanguageID}** wird für Debitoren- und Arbeitskraftentitäten gemäß dem vorhandenen Standard, der seit Microsoft Dynamics AX 6.x. in Kraft war, nicht unterstützt.)

4. Für Bilder wird das Dateinamenformat mit dem Katalognamen fest verbunden und kann nicht geändert werden. Daher benennen Sie Ihre Bilder um, sodass sie entsprechende Katalognamen haben und um sicherzustellen, dass MPOS sie ordnungsgemäß verarbeitet.
5. Wählen Sie im Feld **Dateierweiterung** die erwartete Dateinamenerweiterung abhängig vom Typ der Bilder, die Sie haben. Für die Demodaten werden die Katalogbilder beispielsweise mit der .jpg- Erweiterung festgelegt. (Die Bilddateien werden auch umbenannt, sodass sie Katalognamen haben).
6. Klicken Sie auf **OK**.
7. Um zu überprüfen, ob die Medienvorlage für Bilder ordnungsgemäß gespeichert wurde, klicken Sie auf der Seite **Katalogbilder**, erneut auf **Medienvorlage definieren**. Um die Vorlage ohne das Dialogfeld **Medienvorlage definieren** zu schließen zu validieren, können Sie das Inforegister **Bild-URL für Excel erstellen** verwenden. Überprüfen Sie die Darstellung der Bild URL, und verifizieren Sie, ob die URL mit dem Vorlagenstandard übereinstimmt, der weiter oben erwähnt wurde. Das Dialogfeld **Medienvorlage definieren** hat nun den Bildpfad implizit für alle Katalogbilder festgelegt, die diesen Pfad mit der allgemeinen URL verwenden. Dieser URL-Pfad gilt für alle Katalogbilder, es sei denn, diese werden überschrieben. Der erste Teil des Bildpfads wird von der medienbasierten URL genommen, die Sie im Kanalprofil definiert haben. Der Rest des Pfades wird dem Pfad entnommen, den Sie in der Medienvorlage definiert haben. Die zwei Teile werden verkettet, um die vollständige URL des Bildlagerplatzes bereitzustellen. Beispielsweise erhält ein Katalog in den Demodaten Fabrikam-Basiskatalog. Daher muss der Bildname Fabrikam-Basiskatalog.jpg lauten, damit er den Katalognamen und die .jpg- Dateinamenerweiterung verwendet, die in der Vorlage konfiguriert ist. In diesem Fall wird nach der Verkettung die URL `https://testax3ret.cloud.test.dynamics.com/RetailServer/MediaServer/Catalogs/en-US/Fabrikam Base Catalog.jpg` Base Catalog.jpg sein.
8. Aktivieren Sie die Synchronisierungsvorgänge, um die neue Vorlage zur Kanaldatenbank hinzuzufügen, damit MPOS die Vorlage verwenden kann, um auf die Bilder zuzugreifen.
9. Um die Medienvorlage für Katalogbilder auf der Kanalseite zu aktualisieren, müssen Sie sicherstellen, dass Sie **Katalogvorgang 1150** von **Einzelhandel und Handel-IT** &gt; **Vertriebsplan** ausführen.

    [![Medienvorlagen-Dialogfeld definieren.](./media/catalog1.png)](./media/catalog1.png)

## <a name="previewing-an-image-from-the-entity-level"></a>Zeigen Sie ein Bild auf Entitätsebene in der Vorschau an

1. Über die Seite für den Entitätsartikel in HQ, können Sie das Bild in der Vorschau anzeigen, das die Bild URL verwendet, die von der Medienvorlage geholt wird. Gehen Sie für dieses Beispiel auf den entsprechenden Katalog und dann auf Aktivitätsbereich. Klicken Sie **Medien** &gt; **Bilder** an. Verwenden Sie die Auswahlliste, um verschiedene Filialen auszuwählen, die möglicherweise verschiedene Kanalprofile haben.
2. Um die implizite Medien Vorlage zu bearbeiten oder zu entfernen, müssen Sie zum Dialogfeld **Medienvorlage definieren** auf der Seite **Bilder katalogisieren** zurückkehren.
3. Sie können die Schaltflächen **Hinzufügen** und **Entfernen** verwenden, um den Pfad zu ändern, der auf der impliziten Vorlage basiert und für ein bestimmtes Bild verwendet wird. Weitere Informationen finden Sie im Abschnitt [Überschreiben der Medienvorlage für Entitätsartikel](#overwriting-the-media-template-for-entity-items) weiter unten in diesem Artikel.
4. Nachdem Sie ein Bild in der Vorschau anzeigt und die gewünschten Änderungen vorgenommen haben, starten Sie die MPOS-Instanz um zum entsprechenden Shop zu gelangen und zu sehen, ob die Katalogbilder angezeigt werden.

    [![Bilder-Dialogfeld.](./media/catalog4.png)](./media/catalog4.png)

> [!NOTE]
> Sie können dasselbe Verfahren für alle fünf Entitäten verwenden, die unterstützt werden: Arbeitskraft, Debitor, Katalog, Kategorie und Produkte. "Katalog-Produkte" (Produkte, die auf Katalogebene festgelegt werden) und "Kanalprodukte "( Produkte, die auf der Kanalstufe festgelegt werden), verwenden die Medienvorlage, die für die Produktentität festgelegt ist. Für die Produktmedienvorlage können Sie die Anzahl von Produktbildern auswählen, um das Produkt darzustellen. Sie können das standardmäßige Bild für ein bestimmtes Produkt auch festlegen. Auf diese Weise können Sie leere Bilder in MPOS verhindern und steuern, welches Bild als standardmäßiges Bild für einen Produktionsartikel verwendet wird. Im folgenden Beispiel verfügt jedes Produkt fünf Bilder, und das erste Bild wird als standardmäßiges Bild festgelegt. Verschiedenen Produkte werden gleiche Weise wie Vorlagenprodukte behandelt. Der Dateiname der Bilddatei soll auf der Produktnummer basieren. Einige Zeichen werden auch weggelassen, während der Dateiname generiert wird. Daher ist es gut, den Dateinamen zu überprüfen. Dies tun Sie mithilfe des Bereichs **Bild URL für Excel erstellen**. Siehe [Mit in Excel bearbeiten überschreiben](#overwrite-by-using-edit-in-excel) weiter unten in diesem Artikel.

## <a name="synchronization-jobs-to-send-a-media-template-to-the-channel-side"></a>Synchronisierungsvorgänge, um eine Medienvorlage an die Kanalseite zu senden

Stellen Sie für alle fünf unterstützten Entitäten (Arbeitskraft, Kunde, Katalog, Kategorie und Produkte) bei der Aktualisierung des Dialogs **Medienvorlage definieren** sicher, dass Sie den Katalogvorgang (1150) aus **Einzelhandel und Handel-IT** &gt; **Vertriebszeitplan** ausführen. Dieser Einzelvorgang aktiviert die aktualisierte Medienvorlage und sorgt dafür, dass sie im Kanal synchronisiert und von MPOS verwendet wird. Aktivieren des Katalogeinzelvorgang (1150 ), nachdem Sie folgenden Änderungen vornehmen:

- Aktualisieren Sie die Katalogbild-Medienvorlage von **Bilder katalogisieren** &gt; **Medienvorlage definieren**.
- Aktualisieren Sie Mitarbeiter-Bild-Medienvorlage von **Mitarbeiter-Bilder** &gt; **Medienvorlage definieren**.
- Aktualisieren Sie die Kundenbild-Medienvorlage von **Kundenbilder** &gt; **Medienvorlage definieren**.
- Aktualisieren Sie die Produktbilder-Medienvorlage von **Produktbilder** &gt; **Medienvorlage definieren**.
- Aktualisieren Sie die Katalogbild-Medienvorlage von **Kategorienbilder** &gt; **Medienvorlage definieren**. Sie müssen den Kanal auch veröffentlichen.

## <a name="overwriting-the-media-template-for-entity-items"></a>Überschreiben Sie die Medienvorlage für die Entitätsartikel

Wie Sie im vorherigen Abschnitt lernten, unterstützt die Medienvorlage für eine bestimmte Entität nur einen allgemeinen Pfad. Dieser Pfad basiert auf der medienbasierten URL, die konfiguriert ist und dem definierten Medienpfad. In vielen Fällen möchte ein Einzelhändler aber in der Lage sein, Bilder aus verschiedenen Quellen für eine Untergruppe von Artikeln in einer Entität zu verwenden. Beispielsweise verwendet ein Shop den selbst gehostet Medienserver für einen Satz Katalogbilder, verwendet aber die CDN URLs für einen anderen Satz. Um Bild URLs, die auf einer Medienvorlage für Entitätsbilder auf Entitätsebene basieren zu überschreiben, können Sie die Funktion "In Excel bearbeiten und die Funktion "manuell bearbeiten" von der Seite **Vorschau** verwenden.

### <a name="overwrite-by-using-edit-in-excel"></a>Mit in Excel bearbeiten überschreiben

1. Klicken Sie auf **Einzelhandel und Handel** &gt; **Katalogverwaltung** &gt; **Katalogbilder**.
2. Klicken Sie auf der Seite **Katalogbilder** auf **Medienvorlage definieren**. Im Dialogfeld **Medienvorlage definieren** im Feld **Entität** sollte die Option **Katalog** ausgewählt werden.
3. Merken Sie sich im Inforegister **Medienpfad** den Bildlagerplatz.
4. Klicken Sie im Inforegister **Bild URLs für Excel erstellen** und klicken auf **erstellen**.

    > [!IMPORTANT]
    > Sobald die Medienvorlage geändert wird, müssen Sie auf **Erstellen** klicken, bevor Sie die Funktion in Excel bearbeiten verwenden können.

    Sie sehen nun eine Vorschau der Bild URLs, die basierend auf der letzten gespeicherten Medienvorlage erstellt wurden.

    [![Bild-URLs für Excel-Inforegister generieren, nachdem „Generieren“ ausgewählt ist.](./media/excel2.png)](./media/excel2.png)

    > [!NOTE]
    > Die von Excel erstellten URLS verwenden den Pfad und die Konventionen der Medienvorlage, die definiert ist. Diese Konventionen umfassen die Konventionen für Dateinamen. Die Erwartung ist, dass Sie die physischen Bilder außerhalb von Commerce eingerichtet haben, und Bilder von den URL abgerufen werden können, die von der Medienvorlage stammen, die Sie ebenfalls bereits definiert haben. Sie können dieses abgeleitete URL überschreiben, indem Sie die Funktion Bearbeiten in Excel verwenden.

5. Klicken Sie auf **In Excel bearbeiten**.
6. Nachdem das Microsoft Excel-Arbeitsblatt geöffnet ist, klicken Sie auf **Bearbeiten aktivieren**, wenn Sie dazu aufgefordert werden.
7. Wenn Sie aufgefordert werden, klicken Sie im rechten Bereich auf **Diesem Add-In vertrauen**, um die Installation abzuschließen.

    [![Diesem Add-In vertrauen.](./media/excel4.jpg)](./media/excel4.jpg)

8. Wenn Sie aufgefordert werden, sich anzumelden, geben Sie die diese Anmeldeinformationen ein die Sie verwendeten, um sich bei HQ anzumelden.

    [![Anmeldeaufforderung.](./media/excel5.png)](./media/excel5.png)

9. Nachdem Sie sich angemeldet haben, sollten Sie in der Lage sein, die Liste der Bild URLs für die verschiedenen Katalogeinträge zu sehen.
10. Sie bearbeiten, ergänzen und entfernen die Bild URLs für verschiedene Entitätsartikel.
11. Für alle Entitäten außer Produkte können Sie die Bild URL überschreiben. Ändern Sie dies vorhandene Bild URL, damit sie die neue Ziel URL des Bilds verwendet und aktualisieren Sie den Dateinamen mit dem neuen Dateinamen für die Bilddatei. Der Dateiname muss eindeutig sein, um sicherzustellen, dass der Datensatz eindeutig ist.

    [![Bild URLs in Excel überschreiben.](./media/excel6.jpg)](./media/excel6.jpg)

    > [!NOTE]
    > Wenn Sie Bild URL für Produktentitäten überschreiben, indem Sie die Funktion "Bearbeiten" in Excel-Funktionen oder die Seite "Entitätsartikel" verwenden, sollten MPOS immer alle Medienvorlagenbild-URLs zusammen mit den überschriebenen Bild-URLs anzeigen.

12. Nachdem Sie die Änderungen vorgenommen haben, klicken Sie auf **In Excel veröffentlichen**, um einen neuen expliziten Zuordnungseintrags zu erstellen.
13. An HQ zurückgeben und **OK** klicken.
14. Lassen Sie die entsprechenden Synchronisierungsvorgänge für die Entität laufen und überprüfen Sie die Vorschau auf der Entitätsseite oder in MPOS.

#### <a name="creating-new-records"></a>Neue Einträge erstellen

Sie können in Excel neue Datensätze erstellen. Sie müssen aber sicherstellen, dass Sie die richtigen Informationen bereitstellen. Um beispielsweise einen neuen Eintrag für einen Katalog zu erstellen, vergewissern Sie sich, dass die Katalog-Kennung und der Katalogname korrekt sind und Sie einen eindeutigen Dateinamen angeben. Der eindeutige Dateiname ist außerordentlich wichtig, da die Eindeutigkeit der Datensätze in Excel für die Veröffentlichung geprüft wird. Kopieren Sie zuerst die Details aus dem Katalog, für den Sie einen neuen Datensatz erstellen möchten und kopieren Sie den Datensatz. Sie müssen den Dateinamen und die URL aktualisieren, weil die übrigen Daten gleich sind. Um neue Datensätze für Produktentitätsartikel zu erstellen, verwenden Sie das gleiche Grundverfahren. Kopieren Sie vom Excel-Arbeitsblatt einen vorhandenen Datensatz für das Produkt, für das Sie einen neuen Datensatz erstellen und ersetzen Sie die Bild URL und den Dateinamen. Überprüfen Sie, ob der Dateiname eindeutig ist.

#### <a name="deleting-an-existing-record"></a>Löschen Sie bestehenden Datensatz

Nur der überschriebenen Bild URL-Datensätze können gelöscht werden. Nachdem ein Bild gelöscht wird und die Synchronisierung abgeschlossen ist, erscheint das Bild nicht mehr auf der **Vorschau** Seite oder in MPOS. Datensätze der Bild URL, die von der Medienvorlage abgerufen werden, können nicht gelöscht werden, da diese Datensätze jedes Mal von der Medienvorlage abgerufen werden.

### <a name="overwrite-from-the-entity-level-preview-page"></a>Die Vorschauseite auf Entitätsebene überschreiben

Für alle Entitäten außer für Produkte können Sie die Bild URL für einen angegebenen Entitätsartikel auf Entitätsebene auf der Seite **Vorschau** überschreiben. Für Produkte können Sie die "Katalog-Produkt" Entitätsseite verwenden. Dieses Beispiel verdeutlicht, wie ein Katalogbild überschrieben wird.

1. Klicken Sie auf **Kataloge** &gt; **Medien** &gt; **Bilder** und wählen Sie das Katalogbild aus, das aktualisiert werden soll.
2. Klicken Sie auf **Hinzufügen** und geben Sie die Bild URL ein, die in der Medienvorlagen URL überschrieben werden soll.
3. Wenn Sie dieses Bild in MPOS für den Katalog anzeigen möchten, können Sie es als Standardbild festlegen.
4. Klicken Sie auf **OK**. Die Bild URL wird für dieses Katalogbild aktualisiert und eine Vorschau wird angezeigt.

    [![URL aktualisiert im Dialogfeld „Neues Bild“.](./media/preview3.png)](./media/preview3.png)

5. Sie können die Bildvorschau für alle überschriebenen Bild URLs auch auf der Katalogseite **Katalogbilder** ansehen.

    [![Katalogbilder-Katalogseite.](./media/preview-4.png)](./media/preview-4.png)

> [!NOTE]
> Nur öffentlich und anonym zugängliche Bilder werden am POS gerendert. POS unterstützt das Rendern von Bildern, die extern gehostet werden, mit der Anforderung, dass die Bilder als Inline-Oktettstrom ohne Header an GET-Anforderungen zurückgegeben werden. Mit anonymer Zugriffsrichtlinie, speziell für SharePoint-gehostete Bilder, die erfordern, dass Anforderungsheader sowohl Host- als auch User-Agent-Header enthalten, wird eine „Forbidden“-Antwort zurückgegeben. Daher Bildverwaltung mit SharePoint da der Host derzeit nicht standardmäßig unterstützt wird. Die **Katalogbilder** Gallerieseite zeigt keine Bildvorschauen für Medienvorlagenbild URLs an. Da Commerce Scale Unit (CSU) Client nur ein Bild pro Katalog, Kunde, Arbeitskraft, und Kategorieentität anzeigen, wenn Sie explizit eine URL durch diese Seite für Katalog-, Arbeitskraft-, Kunden- und Kategorieentitäten explizit eine URL über diese Seite bereitstellt, empfehlen wir, dass Sie angeben, welches das Standardbild ist. Wenn Sie kein Standardbild angeben, bestimmt das System das standardmäßige Bild und sendet es an den Commerce Service-Aufrufer (MPOS oder E-Commerce).

### <a name="overwrite-the-image-url-for-catalog-product-images-from-the-preview-page"></a>Die Bild URL für Katalogproduktbilder aus der Vorschauseite überschreiben

Um Bild URLs für Katalogproduktbilder zu überschreiben, müssen Sie die Seite **Vorschau** verwenden. Sie können in der Excel-Funktionalität Bearbeiten nicht verwenden.

1. Um Produktbilder auf einer Katalogebene zu überschreiben, wählen Sie einen Katalog aus und wählen anschließend das Produkt, für das das Bild überschrieben werden soll.
2. Klicken Sie auf **Attribute**.
3. Wählen Sie auf der nächsten Seite **Bild** und klicken dann auf **Bearbeiten**. Die Seite **Vorschau** öffnet sich als angleichendes Dialogfeld.
4. Klicken Sie auf **Hinzufügen** und überschreiben Sie die Bild URL mit einer neuen URL.
5. Klicken Sie auf **OK**. Sie sehen nun eine Vorschau des neuen Bilds und können es als Standardbild festlegen.

    [![Bildvorschau im Dialogfeld „Neues Bild“.](./media/cat3.png)](./media/cat3.png)

> [!NOTE]
> Nach der Kategoriebildzuordnung müssen Sie den Kanal veröffentlichen und den Kanaleinzelvorgang aktivieren, um sicherzustellen, dass die Änderungen in der Kanaldatenbank veröffentlicht werden.

## <a name="setting-up-images-to-appear-in-offline-mode-for-mpos"></a>Produktbilder definieren, die im MPOS Offline-Modus angezeigt werden

MPOS kann im Onlinemodus (wenn MPOS mit der Commerce Scale Unit verbunden ist) oder im Offlinemodus (wenn keine Commerce Scale Unit oder Netzwerkverbindung vorhanden ist und die Transaktionen in einer lokalen Offline-Datenbank gespeichert werden) betrieben werden. Wenn MPOS im Offline-Modus ausgeführt wird, kann er keine Bilder vom externen Bildserver zur Anzeige aus der Commerce Scale Unit abrufen, weil die Verbindung verloren ging. Allerdings können Sie Bilder dennoch einrichten, damit sie angezeigt werden, wenn MPOS im Offlinemodus ausgeführt wird.

### <a name="set-up-product-images-to-appear-in-offline-mode-for-mpos"></a>Produktbilder definieren, die im MPOS Offlinemodus angezeigt werden

Die Produktbilder, die im Offlinemodus verwendet werden müssen, können eingerichtet werden, indem die erforderliche physischen Bild in das Basisproduktbild hochgeladen werden.

1. Klicken Sie auf **Produktinformationsmanagement** &gt; **Produkte** &gt; **Produkte**.
2. Wählen Sie das Produkt aus, für das das Offlineimage festgelegt werden soll.
3. Klicken Sie auf **Bearbeiten** und dann auf den Pfeil in der rechten Ecke, um den rechten Bereich anzuzeigen.
4. Wählen Sie aus dem Inforegister **Produktbild** und klicken auf **Bild ändern**, um das physische Bild hochzuladen, das für das ausgewählte Produkt im Offlinemodus verwendet werden soll.
5. Seite speichern und schließen
6. Während sich MPOS im Offlinemodus befindet., führen Sie den Katalogeinzelvorgang in HQ aus, um sicherzustellen, dass die Daten mindestens einmal an die Offline-Datenbank gesendet werden.
7. Setzen Sie MPOS in in Offline-Betrieb. Sie sollten das Bild sehen, das Sie für das bestimmte Produkt in HQ hochgeladen haben.

    [![Produktbild im Offline-Modus.](./media/offline1.png)](./media/offline1.png)

### <a name="set-up-catalog-category-employee-and-customer-images-to-appear-in-offline-mode-for-mpos"></a>Katalog, Kategorie, Mitarbeiter und Debitorenbilder einrichten, damit sie im Offline-Modus für MPOS angezeigt werden

Die Katalog-, Kategorie-, Mitarbeiter sowie die Debitorenbilder, die im Offline-Modus verwendet werden müssen, können aufgesetzt werden, indem der erforderliche Ziellink des Bilds im Katalog hinzugefügt wird und das Bild als Standardbild für die ausgewählte Entität festlegt wird.

1. Klicken Sie zum Katalog und klicken Sie im Aktivitätsbereich auf **Medien** &gt; **Bilder**.
2. Folgen Sie den Schritte im Abschnitt [Vorschauseite auf Entitätsebene überschreiben](#overwrite-from-the-entity-level-preview-page), um die externe Bild-URL hinzuzufügen.
3. Aktivieren Sie dieses Bild als standardmäßiges Bild für den Katalog, indem Sie das Kontrollkästchen für das Bild auswählen, das im Raster aufgeführt ist.
4. Führen Sie den Katalogvorgang aus. Dieses Bild wird jetzt als Offlinebild für den Katalog in MPOS verwendet.
5. Führen Sie einen ähnlichen Prozess für andere Entitäten, wie Kategorie, Mitarbeiter und Debitor durch.

    [![Offline-Bild.](./media/offline2.png)](./media/offline2.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
