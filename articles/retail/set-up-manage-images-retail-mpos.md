---
title: "Bilder für Retail Modern POS einrichten und verwalten"
description: "In diesem Artikel wird beschrieben welche Schritte beim Einrichten und Verwalten von Bildern für verschiedene Retail Modern POS erforderlich sind."
author: athinesh99
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailChannelProfile, RetailMediaGallery, RetailImages,
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 52851
ms.assetid: 5c21385e-64e0-4091-98fa-6a662eb33010
ms.search.region: global
ms.search.industry: Retail
ms.author: athinesh
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: ed4a7044b577ed6af86f6803f6abd4f9b500b4e7
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-and-manage-images-for-retail-modern-pos"></a>Bilder für Retail Modern POS einrichten und verwalten

[!INCLUDE [banner](includes/banner.md)]

In diesem Artikel wird beschrieben welche Schritte beim Einrichten und Verwalten von Bildern für verschiedene Retail Modern POS erforderlich sind.

<a name="setting-up-the-media-base-url-and-defining-media-templates-to-configure-the-format-for-image-urls"></a>Die URL für die Medienbasis festlegen und die Medienvorlagen bestimmen, um das Format für die Bild-URL einrichten.
-------------------------------------------------------------------------------------------------

Die Bilder, die im Retail Modern POS (MPOS) angezeigt werden, müssen extern, außerhalb von Microsoft Dynamics 365 for Retail gehostet werden. In der Regel werden sie auf einem Content Management-System, auf einem Content Delivery Network (CDN) oder einem Medienserver gehostet. MPOS ruft dann die Bilder von den entsprechenden Einheiten wie Produkten und Kataloge ab und zeigt sie an, indem es auf die Ziel URL zugreift. Um diese extern gehosteten Bilder abzurufen, braucht MPOS das korrekte URL-Format für die Bilder. Sie können das erforderliche URL-Format für Bilder konfigurieren, indem Sie den Wert für die **medienbasierte URL** im Kanalprofil einrichten und die Funktionen **Medienvorlage definieren** für jede Entität verwenden. Sie können das Format der Standard-URL für eine Teilmenge von Entitäten auch überschreiben, indem Sie dies Funktion **In Excel bearbeiten** verwenden. **Wichtiger Hinweis:** In der aktuellen Version von Dynamics 365 for Retail können Sie das URL-Format nicht mehr mithilfe des **Bild** Attributs XML für MPOS unter **Standard** Attribut für Gruppenentitäten einrichten. Wenn Sie mit Microsoft Dynamics AX 2012 R3 vertraut sind und nun die aktuelle Version von Dynamics 365 for Retail verwenden, überprüfen Sie, ob Sie immer die neuen Funktionen **Medienvorlage definieren**, um Bilder einzurichten. Verwenden oder ändern Sie auf keinen Fall das Attribut **Bild** in der **Standard**-Attributengruppe für Entitäten, einschließlich Produkte. Änderungen, die Sie direkt in der Attributgruppe **Standard** für Bilder machen, werden nicht abgebildet. Diese Option wird in einer späteren Version deaktiviert. In den folgenden Verfahren werden Bilder für die Katalogentität als Beispiel genannte. Diese Verfahren helfen sicherzustellen, dass der korrekte Bildzielpfad implizit für alle Katalogbilder festgelegt wird, die einen allgemeinen Pfad folgen. Wenn Sie beispielsweise einen Medienserver oder ein CDN extern eingerichtet haben und möchten, dass die Bilder in MPOS für eine angegebenen Filiale angezeigt werden, wird Ihnen die Funktionalität **Medienvorlage definieren** helfen, den Pfad festzulegen, von dem MPOS Bilder suchen und holen kann. **Hinweis:** Für dieses Demodatenbeispiel wird der Medienserver im Retail-Server bereitgestellt. Allerdings können Sie ihn an einer beliebigen Stelle außerhalb von Dynamics 365 for Retail haben.

### <a name="set-up-the-media-base-url-for-a-channel"></a>Die medienbasierte URL für einen Kanal einrichten

1.  Öffnen des Dynamics 365 for Retail-HQ-Portals
2.  Klicken Sie auf **Einzelhandel** &gt; **Kanaleinstellung** &gt; **Kanalprofile**. [![channel-profile1](./media/channel-profile1.png)](./media/channel-profile1.png)
3.  Im Kanalprofil, das Ihr Shop für MPOS verwendet, aktualisieren Sie das Feld mit der **Medienbasierten URL** mit der Basis-URL von Ihrem Medienserver oder CDN. Die Basis-URL ist der erste Teil der URL, die von allen Bildordner von andere Entitäten freigegeben wird.[![channel-profile2](./media/channel-profile2.png)](./media/channel-profile2.png)

### <a name="define-the-media-template-for-an-entity"></a>Definieren Sie die Medienvorlage für eine Entität

1.  Klicken Sie auf **Einzelhandel** &gt; **Katalogverwaltung** &gt; **Katalogbilder**.
2.  Klicken Sie auf der Seite **Katalogbilder** den Aktivitätsbereich und klicken Sie **Medienvorlage definieren** an. Im Dialogfeld **Medienvorlage definieren** im Feld **Entität** **Katalog** sollte die Option standardmäßig ausgewählt werden.
3.  Geben Sie im Inforegister **Medienpfad** den verbleibenden Pfad des Bildlagerplatzes ein. Die Medienpfad unterstützt **LanguageID** als Variable. Sie können beispielswiese für die Demodaten einen Ordner **Kataloge** für alle Katalogbilder unter der medienbasierten URL für Ihren Medienserver erstellen (https://testax3ret.cloud.test.dynamics.com/RetailServer/MediaServer). Sie können dann einen Ordner für jede Sprache haben, wie en-US oder fr-FR und dann die entsprechenden Bilder in jedem Ordner entsprechend speichern. Wenn Sie keine verschiedenen Bilder für die unterschiedlichen Sprachen haben, können Sie die Variablen **LanguageID** aus Ihrer Ordnerstruktur übergehen und direkt zum Katalogordner gehen, der die Katalogbilder enthält. **Hinweis:** Die aktuelle Version von Dynamics 365 for Retail unterstützt den Token **{LanguageID}** für Katalog-, Produkt- und Kategorieentitäten. (Der Token **{LanguageID}** wird für Debitoren- und Arbeitskraftentitäten gemäß dem vorhandenen Standard, der seit Microsoft Dynamics AX 6.x. in Kraft war, nicht unterstützt.)
4.  Für Bilder wird das Dateinamenformat mit dem Katalognamen fest verbunden und kann nicht geändert werden. Daher benennen Sie Ihre Bilder um, sodass sie entsprechende Katalognamen haben und um sicherzustellen, dass MPOS sie ordnungsgemäß verarbeitet.
5.  Wählen Sie im Feld **Dateierweiterung** die erwartete Dateinamenerweiterung abhängig vom Typ der Bilder, die Sie haben. Für die Demodaten werden die Katalogbilder beispielsweise mit der .jpg- Erweiterung festgelegt. (Die Bilddateien werden auch umbenannt, sodass sie Katalognamen haben).
6.  Klicken Sie auf **OK**.
7.  Um zu überprüfen, ob die Medienvorlage für Bilder ordnungsgemäß gespeichert wurde, klicken Sie auf der Seite **Katalogbilder**, erneut auf **Medienvorlage definieren**. Um die Vorlage ohne das Dialogfeld **Medienvorlage definieren** zu schließen zu validieren, können Sie das Inforegister **Bild-URL für Excel erstellen** verwenden. Überprüfen Sie die Darstellung der Bild URL, und verifizieren Sie, ob die URL mit dem Vorlagenstandard übereinstimmt, der weiter oben erwähnt wurde. Das Dialogfeld **Medienvorlage definieren** hat nun den Bildpfad implizit für alle Katalogbilder festgelegt, die diesen Pfad mit der allgemeinen URL verwenden. Dieser URL-Pfad gilt für alle Katalogbilder, es sei denn, diese werden überschrieben. Der erste Teil des Bildpfads wird von der medienbasierten URL genommen, die Sie im Kanalprofil definiert haben. Der Rest des Pfades wird dem Pfad entnommen, den Sie in der Medienvorlage definiert haben. Die zwei Teile werden verkettet, um die vollständige URL des Bildlagerplatzes bereitzustellen. Beispielsweise erhält ein Katalog in den Demodaten Fabrikam-Basiskatalog. Daher muss der Bildname Fabrikam-Basiskatalog.jpg lauten, damit er den Katalognamen und die .jpg- Dateinamenerweiterung verwendet, die in der Vorlage konfiguriert ist. In diesem Fall lautet nach der Verkettung die URL https://testax3ret.cloud.test.dynamics.com/RetailServer/MediaServer/Catalogs/en-US/Fabrikam Base Catalog.jpg.
8.  Aktivieren Sie die Synchronisierungsvorgänge, um die neue Vorlage zur Kanaldatenbank hinzuzufügen, damit MPOS die Vorlage verwenden kann, um auf die Bilder zuzugreifen.
9.  Um die Medienvorlage für Katalogbilder auf der Kanalseite zu aktualisieren, müssen Sie sicherstellen, dass Sie **Katalogvorgang 1150** von **Retail IT** &gt; **Distributionszeitplan** laufen lassen.[![catalog1](./media/catalog1.png)](./media/catalog1.png)

## <a name="previewing-an-image-from-the-entity-level"></a>Zeigen Sie ein Bild auf Entitätsebene in der Vorschau an
1.  Über die Seite für den Entitätsartikel in HQ, können Sie das Bild in der Vorschau anzeigen, das die Bild URL verwendet, die von der Medienvorlage geholt wird. Gehen Sie für dieses Beispiel auf den entsprechenden Katalog und dann auf Aktivitätsbereich. Klicken Sie **Medien** &gt; **Bilder** an. Verwenden Sie die Auswahlliste, um verschiedene Filialen auszuwählen, die möglicherweise verschiedene Kanalprofile haben.
2.  Um die implizite Medien Vorlage zu bearbeiten oder zu entfernen, müssen Sie zum Dialogfeld **Medienvorlage definieren** auf der Seite **Bilder katalogisieren** zurückkehren.
3.  Sie können die Schaltflächen **Hinzufügen** und **Entfernen** verwenden, um den Pfad zu ändern, der auf der impliziten Vorlage basiert und für ein bestimmtes Bild verwendet wird. Weitere Informationen finden Sie im Abschnitt "Überschreiben der Medienvorlage für Entitätsartikel" weiter unten in diesem Artikel.
4.  Nachdem Sie ein Bild in der Vorschau anzeigt und die gewünschten Änderungen vorgenommen haben, starten Sie die MPOS-Instanz um zum entsprechenden Shop zu gelangen und zu sehen, ob die Katalogbilder angezeigt werden.[![catalog4](./media/catalog4.png)](./media/catalog4.png)

**Hinweis:** Sie können dasselbe Verfahren für alle fünf Entitäten verwenden, die unterstützt werden: Arbeitskraft, Debitor, Katalog, Kategorie und Produkte. "Katalog-Produkte" (Produkte, die auf Katalogebene festgelegt werden) und "Kanalprodukte "( Produkte, die auf der Kanalstufe festgelegt werden), verwenden die Medienvorlage, die für die Produktentität festgelegt ist. Für die Produktmedienvorlage können Sie die Anzahl von Produktbildern auswählen, um das Produkt darzustellen. Sie können das standardmäßige Bild für ein bestimmtes Produkt auch festlegen. Auf diese Weise können Sie leere Bilder in MPOS verhindern und steuern, welches Bild als standardmäßiges Bild für einen Produktionsartikel verwendet wird. Im folgenden Beispiel verfügt jedes Produkt fünf Bilder, und das erste Bild wird als standardmäßiges Bild festgelegt. Verschiedenen Produkte werden gleiche Weise wie Vorlagenprodukte behandelt. Der Dateiname der Bilddatei soll auf der Produktnummer basieren. Einige Zeichen werden auch weggelassen, während der Dateiname generiert wird. Daher ist es gut, den Dateinamen zu überprüfen. Dies tun Sie mithilfe des Bereichs **Bild URL für Excel erstellen**. [![prods](./media/prods.png)](./media/prods.png)  

## <a name="synchronization-jobs-to-send-a-media-template-to-the-channel-side"></a>Synchronisierungsvorgänge, um eine Medienvorlage an die Kanalseite zu senden
Stellen Sie für alle fünf unterstützten Entitäten (Arbeiter, Debitor, Katalog, Kategorie und Produkte) bei der Aktualisierung des Dialogs **Medienvorlage definieren** sicher, dass Sie den Katalogeinzelvorgang (1150) aus **Retail IT** &gt; **Vertriebszeitplan**. Dieser Einzelvorgang aktiviert die aktualisierte Medienvorlage und sorgt dafür, dass sie im Kanal synchronisiert und von MPOS verwendet wird. Aktivieren des Katalogeinzelvorgang (1150 ), nachdem Sie folgenden Änderungen vornehmen:

-   Aktualisieren Sie die Katalogbild-Medienvorlage von **Bilder katalogisieren** &gt; **Medienvorlage definieren**.
-   Aktualisieren Sie Mitarbeiter-Bild-Medienvorlage von **Mitarbeiter-Bilder** &gt; **Medienvorlage definieren**.
-   Aktualisieren Sie die Kundenbild-Medienvorlage von **Kundenbilder** &gt; **Medienvorlage definieren**.
-   Aktualisieren Sie die Produktbilder-Medienvorlage von **Produktbilder** &gt; **Medienvorlage definieren**.
-   Aktualisieren Sie die Katalogbild-Medienvorlage von **Kategorienbilder** &gt; **Medienvorlage definieren**. Sie müssen den Kanal auch veröffentlichen.

## <a name="overwriting-the-media-template-for-entity-items"></a>Überschreiben Sie die Medienvorlage für die Entitätsartikel
Wie Sie im vorherigen Abschnitt lernten, unterstützt die Medienvorlage für eine bestimmte Entität nur einen allgemeinen Pfad. Dieser Pfad basiert auf der medienbasierten URL, die konfiguriert ist und dem definierten Medienpfad. In vielen Fällen möchte ein Einzelhändler aber in der Lage sein, Bilder aus verschiedenen Quellen für eine Untergruppe von Artikeln in einer Entität zu verwenden. Beispielsweise verwendet ein Shop den selbst gehostet Medienserver für einen Satz Katalogbilder, verwendet aber die CDN URLs für einen anderen Satz. Um Bild URLs, die auf einer Medienvorlage für Entitätsbilder auf Entitätsebene basieren zu überschreiben, können Sie die Funktion "In Excel bearbeiten und die Funktion "manuell bearbeiten" von der Seite **Vorschau** verwenden.

### <a name="overwrite-by-using-edit-in-excel"></a>Mit in Excel bearbeiten überschreiben

1.  Klicken Sie auf **Einzelhandel** &gt; **Katalogverwaltung** &gt; **Katalogbilder**.
2.  Klicken Sie auf der Seite **Katalogbilder** auf **Medienvorlage definieren**. Im Dialogfeld **Medienvorlage definieren** im Feld **Entität** sollte die Option **Katalog** ausgewählt werden.
3.  Merken Sie sich im Inforegister **Medienpfad** den Bildlagerplatz.
4.  Klicken Sie im Inforegister **Bild URLs für Excel erstellen** und klicken auf **erstellen**. **Wichtig:** Sobald die Medienvorlage geändert wird, müssen Sie auf **Erstellen** klicken, bevor Sie die Funktion in Excel bearbeiten verwenden können. [![excel1](./media/excel1.jpg)](./media/excel1.jpg) Sie sehen nun eine Vorschau der Bild URLs, die basierend auf der letzten gespeicherten Medienvorlage erstellt wurden. [![excel2](./media/excel2.png)](./media/excel2.png) **Hinweis:** Die von Excel erstellten URLS verwenden den Pfad und die Konventionen der Medienvorlage, die definiert ist. Diese Konventionen umfassen die Konventionen für Dateinamen. Die Erwartung ist, dass Sie die physischen Bilder außerhalb Dynamics 365 for Retail eingerichtet haben, und Bilder von den URL abgerufen werden können, die von der Medienvorlage stammen, die Sie ebenfalls bereits definiert haben. Sie können dieses abgeleitete URL überschreiben, indem Sie die Funktion Bearbeiten in Excel verwenden.
5.  Klicken Sie auf **In Excel bearbeiten**.
6.  Nachdem das Microsoft Excel-Arbeitsblatt geöffnet ist, klicken Sie auf **Bearbeiten aktivieren**, wenn Sie dazu aufgefordert werden.
7.  Wenn Sie aufgefordert werden, klicken Sie im rechten Bereich auf **Diesem Add-In vertrauen**, um die Installation abzuschließen. [![Diesem Add-In vertrauen](./media/excel4.jpg)](./media/excel4.jpg)
8.  Wenn Sie aufgefordert werden, sich anzumelden, geben Sie die diese Anmeldeinformationen ein die Sie verwendeten, um sich bei HQ anzumelden. [![Anmeldeaufforderung](./media/excel5.png)](./media/excel5.png)
9.  Nachdem Sie sich angemeldet haben, sollten Sie in der Lage sein, die Liste der Bild URLs für die verschiedenen Katalogeinträge zu sehen.
10. Sie bearbeiten, ergänzen und entfernen die Bild URLs für verschiedene Entitätsartikel.
11. Für alle Entitäten außer Produkte können Sie die Bild URL überschreiben. Ändern Sie dies vorhandene Bild URL, damit sie die neue Ziel URL des Bilds verwendet und aktualisieren Sie den Dateinamen mit dem neuen Dateinamen für die Bilddatei. Der Dateiname muss eindeutig sein, um sicherzustellen, dass der Datensatz eindeutig ist. [![Bild URLs in Excel überschreiben](./media/excel6.jpg)](./media/excel6.jpg) **Hinweis:** Wenn Sie Bild URL für Produktentitäten überschreiben, indem Sie die Funktion Bearbeiten in Excel-Funktionen oder die Seite Entitätsartikel verwenden, sollten MPOS immer alle Medienvorlagenbild URLs zusammen mit den überschriebenen Bild URLs anzeigen.
12. Nachdem Sie die Änderungen vorgenommen haben, klicken Sie auf **In Excel veröffentlichen**, um einen neuen expliziten Zuordnungseintrags zu erstellen.
13. An HQ zurückgeben und **OK** klicken.
14. Lassen Sie die entsprechenden Synchronisierungsvorgänge für die Entität laufen und überprüfen Sie die Vorschau auf der Entitätsseite oder in MPOS.

#### <a name="creating-new-records"></a>Neue Einträge erstellen

Sie können in Excel neue Datensätze erstellen. Sie müssen aber sicherstellen, dass Sie die richtigen Informationen bereitstellen. Um beispielsweise einen neuen Eintrag für einen Katalog zu erstellen, vergewissern Sie sich, dass die Katalog-Kennung und der Katalogname korrekt sind und Sie einen eindeutigen Dateinamen angeben. Der eindeutige Dateiname ist außerordentlich wichtig, da die Eindeutigkeit der Datensätze in Excel für die Veröffentlichung geprüft wird. Kopieren Sie zuerst die Details aus dem Katalog, für den Sie einen neuen Datensatz erstellen möchten und kopieren Sie den Datensatz. Sie müssen den Dateinamen und die URL aktualisieren, weil die übrigen Daten gleich sind. Um neue Datensätze für Produktentitätsartikel zu erstellen, verwenden Sie das gleiche Grundverfahren. Kopieren Sie vom Excel-Arbeitsblatt einen vorhandenen Datensatz für das Produkt, für das Sie einen neuen Datensatz erstellen und ersetzen Sie die Bild URL und den Dateinamen. Überprüfen Sie, ob der Dateiname eindeutig ist.

#### <a name="deleting-an-existing-record"></a>Löschen Sie bestehenden Datensatz

Nur der überschriebenen Bild URL-Datensätze können gelöscht werden. Nachdem ein Bild gelöscht wird und die Synchronisierung abgeschlossen ist, erscheint das Bild nicht mehr auf der **Vorschau** Seite oder in MPOS. Datensätze der Bild URL, die von der Medienvorlage abgerufen werden, können nicht gelöscht werden, da diese Datensätze jedes Mal von der Medienvorlage abgerufen werden.

### <a name="overwrite-from-the-entity-level-preview-page"></a>Die Vorschauseite auf Entitätsebene überschreiben

Für alle Entitäten außer für Produkte können Sie die Bild URL für einen angegebenen Entitätsartikel auf Entitätsebene auf der Seite **Vorschau** überschreiben. Für Produkte können Sie die "Katalog-Produkt" Entitätsseite verwenden. Dieses Beispiel verdeutlicht, wie ein Katalogbild überschrieben wird.

1.  Klicken Sie auf **Kataloge** &gt; **Medien** &gt; **Bilder** und wählen Sie das Katalogbild aus, das aktualisiert werden soll.
2.  Klicken Sie auf **Hinzufügen** und geben Sie die Bild URL ein, die in der Medienvorlagen URL überschrieben werden soll.
3.  Wenn Sie dieses Bild in MPOS für den Katalog anzeigen möchten, können Sie es als Standardbild festlegen.
4.  Klicken Sie auf **OK**. Die Bild URL wird für dieses Katalogbild aktualisiert und eine Vorschau wird angezeigt. [![preview3](./media/preview3.png)](./media/preview3.png)
5.  Sie können die Bildvorschau für alle überschriebenen Bild URLs auch auf der Katalogseite **Katalogbilder** ansehen.

**[![preview-4](./media/preview-4.png)](./media/preview-4.png)Hinweis:** Zurzeit werden in der Bildübersicht die Bildvorschauen für Medienvorlagenbild URLs nicht angezeigt. Wenn der Benutzer für Katalog-, Arbeitskraft-, Debitoren- und Kategorieentitäten explizit eine URL über diese Seite bereitstellt, empfehlen wir, dass Sie angeben, welches das Standardbild ist, weil Retail Server Clients nur ein Bild pro Katalog, Debitor, Arbeitskraft und Kategorie anzeigen. Wenn der Benutzer kein Standardbild angibt, bestimmt das System das standardmäßige Bild und sendet es an den Retail Service Client (MPOS oder elektronischer Geschäftsverkehr).

### <a name="overwrite-the-image-url-for-catalog-product-images-from-the-preview-page"></a>Die Bild URL für Katalogproduktbilder aus der Vorschauseite überschreiben

Um Bild URLs für Katalogproduktbilder zu überschreiben, müssen Sie die Seite **Vorschau** verwenden. Sie können in der Excel-Funktionalität Bearbeiten nicht verwenden.

1.  Um Produktbilder auf einer Katalogebene zu überschreiben, wählen Sie einen Katalog aus und wählen anschließend das Produkt, für das das Bild überschrieben werden soll.
2.  Klicken Sie auf **Attribute**.
3.  Wählen Sie auf der nächsten Seite **Bild** und klicken dann auf **Bearbeiten**. Die Seite **Vorschau** öffnet sich als angleichendes Dialogfeld.
4.  Klicken Sie auf **Hinzufügen** und überschreiben Sie die Bild URL mit einer neuen URL.
5.  Klicken Sie auf **OK**. Sie sehen nun eine Vorschau des neuen Bilds und können es als Standardbild festlegen.

**[![cat3](./media/cat3.png)](./media/cat3.png)Hinweis:** Nach der Kategoriebildzuordnung müssen Sie den Kanal veröffentlichen und den Kanaleinzelvorgang aktivieren, um sicherzustellen, dass die Änderungen in der Kanaldatenbank veröffentlicht werden.

## <a name="setting-up-images-to-appear-in-offline-mode-for-mpos"></a>Produktbilder definieren, die im MPOS Offline-Modus angezeigt werden
MPOS kann im Onlinemodus (wenn MPOS mit dem Retail Server verbunden ist) oder im Offlinemodus (wenn kein Retail Server oder Netzwerkverbindung vorhanden ist und die Transaktionen in einer lokalen Offline-Datenbank gespeichert werden) betrieben werden. Wenn MPOS im Offline-Modus ausgeführt wird, kann er keine Bilder vom externen Bildserver abrufen, um im Retail Server anzuzeigen, weil die Retail Server Verbindung verloren ging. Allerdings können Sie Bilder dennoch einrichten, damit sie angezeigt werden, wenn MPOS im Offlinemodus ausgeführt wird.

### <a name="set-up-product-images-to-appear-in-offline-mode-for-mpos"></a>Produktbilder definieren, die im MPOS Offlinemodus angezeigt werden

Die Produktbilder, die im Offlinemodus verwendet werden müssen, können eingerichtet werden, indem die erforderliche physischen Bild in das Basisproduktbild hochgeladen werden.

1.  Klicken Sie auf **Produktinformationsmanagement** &gt; **Produkte** &gt; **Produkte**.
2.  Wählen Sie das Produkt aus, für das das Offlineimage festgelegt werden soll.
3.  Klicken Sie auf **Bearbeiten** und dann auf den Pfeil in der rechten Ecke, um den rechten Bereich anzuzeigen.
4.  Wählen Sie aus dem Inforegister **Produktbild** und klicken auf **Bild ändern**, um das physische Bild hochzuladen, das für das ausgewählte Produkt im Offlinemodus verwendet werden soll.
5.  Seite speichern und schließen
6.  Während sich MPOS im Offlinemodus befindet., führen Sie den Katalogeinzelvorgang in HQ aus, um sicherzustellen, dass die Daten mindestens einmal an die Offline-Datenbank gesendet werden.
7.  Setzen Sie MPOS in in Offline-Betrieb. Sie sollten das Bild sehen, das Sie für das bestimmte Produkt in HQ hochgeladen haben. [![offline1](./media/offline1.png)](./media/offline1.png)



### <a name="set-up-catalog-category-employee-and-customer-images-to-appear-in-offline-mode-for-mpos"></a>Katalog, Kategorie, Mitarbeiter und Debitorenbilder einrichten, damit sie im Offline-Modus für MPOS angezeigt werden

Die Katalog-, Kategorie-, Mitarbeiter sowie die Debitorenbilder, die im Offline-Modus verwendet werden müssen, können aufgesetzt werden, indem der erforderliche Ziellink des Bilds im Katalog hinzugefügt wird und das Bild als Standardbild für die ausgewählte Entität festlegt wird.

1.  Klicken Sie zum Katalog und klicken Sie im Aktivitätsbereich auf **Medien** &gt; **Bilder**.
2.  Folgen Sie den Schritte im Abschnitt **Vorschauseite auf Entitätsebene überschreiben**, um die externe Bild-URL hinzuzufügen.
3.  Aktivieren Sie dieses Bild als standardmäßiges Bild für den Katalog, indem Sie das Kontrollkästchen für das Bild auswählen, das im Raster aufgeführt ist.
4.  Führen Sie den Katalogvorgang aus. Dieses Bild wird jetzt als Offlinebild für den Katalog in MPOS verwendet.
5.  Führen Sie einen ähnlichen Prozess für andere Entitäten, wie Kategorie, Mitarbeiter und Debitor durch.

[![offline2](./media/offline2.png)](./media/offline2.png)    




