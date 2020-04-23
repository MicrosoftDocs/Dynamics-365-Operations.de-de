---
title: Visuelle Konfigurationen der POS-Benutzeroberfläche
description: Dieses Thema enthält Informationen zu Bildschirmlayouts für Dynamics 365 Commerce-Verkaufsstellen (POS)-Umgebungen.
author: boycezhu
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTillLayout
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 90573
ms.assetid: a6868f93-02ed-4928-9f6a-3b7383e7e399
ms.search.region: global
ms.search.industry: Retail
ms.author: boycezhu
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 3a84318f7156ef42f7e00f1e89228f541b1634ce
ms.sourcegitcommit: ac966ea3a6c557fb5f9634b187b0e788d3e82d4d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261466"
---
# <a name="pos-user-interface-visual-configurations"></a>Visuelle Konfigurationen der POS-Benutzeroberfläche

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Die Benutzeroberfläche (UI) der Microsoft Dynamics 365 Commerce Verkaufsstelle (POS) kann mithilfe einer Kombination von visuellen Profilen und Bildschirmlayouts konfiguriert werden, die Shops, Kassen und/oder den Benutzern zugewiesen sind. Dieses Thema enthält Links zu weiteren Informationen über diese Konfigurationsoptionen.

Die folgende Abbildung zeigt die Beziehungen zwischen den unterschiedlichen Entitäten, die die konfigurierbare POS-Benutzeroberfläche bilden.

![Entität für POS-Bildschirmlayout](../commerce/media/POS-layout-configuration-entities-diagram.png)

## <a name="visual-profile"></a>Visuelles Profil

Visuelle Profile werden für die Kassen zugewiesen und werden verwendet, um die Sichtelementen anzugeben, die kassenspezifisch sind und gemeinsam genutzt werden. Jeder Benutzer, der sich an der Kasse anmeldet, sieht dasselbe Thema, Layout, Farben und Bilder.

![POS-Begrüßungsbildschirm mit hellem Thema](../commerce/media/POS-Welcome-Screen-with-Light-theme.png)

![POS-Buchungs-Bildschirm mit dunklem Thema](../commerce/media/POS-Transaction-Screen-with-Dark-theme.png)

- **Profilnummer** Die Profilnummer für die eindeutige Kennung für das visuelle Profil.
- **Beschreibung** - Die Beschreibung ermöglicht es Ihnen, einen beschreibenden Namen angeben, der Ihnen hilft, das richtige Profil für in Ihrer Situation zu identifizieren.
- **Thema** - Sie können zwischen den **hellen** und **dunklen** Anwendungsdesigns auswählen. Das Thema betrifft die gewünschten Schrift- und Hintergrundfarben in der Anwendung.
- **Akzentfarbe** - Die Akzentfarbe wird im POS verwendet, um bestimmte Sichtelemente wie Kacheln, Befehlsschaltflächen oder Links zu unterscheiden oder hervorzuheben. Diese Elemente sind in der Regel aktiv.
- **Kopffarbe** – Sie können die Farbe der Kopfzeile konfigurieren, um die Brandingbedingungen des Einzelhändlers zu erfüllen.
- **Schriftschema** – Sie können zwischen den **Standard** und **Groß** Schriftschemata auswählen. Das Schriftschema wirkt sich auf die Schriftgröße in der gesamten Anwendung aus. Die Standardauswahl ist **Standard**.
- **Zeigen Sie immer Beschriftungen der Anwendungsleiste an** – Wenn diese Option aktiviert ist, ist der Beschriftungstext immer unter den Schaltflächen der Anwendungsleiste sichtbar.
- **Layout** – Sie können zwischen den Layouts **Zentriert** und **Rechts** auswählen. Das Layout wirkt sich auf die Ausrichtung des Anmeldefelds auf dem Anmeldebildschirm aus. Die Standardauswahl ist **Zentriert**.
- **Datum/Uhrzeit anzeigen** – Wenn diese Option aktiviert ist, werden das aktuelle Datum und die aktuelle Uhrzeit im POS-Kopf und auf dem Anmeldebildschirm angezeigt.
- **Tastatur** – Sie können zwischen **Standardmäßiger Betriebssystemtastatur** und **Nummernblock anzeigen** auswählen, um die Standardtastatur anzugeben, die für die Eingabe auf dem Anmeldebildschirm verwendet wird. Der Nummernblock ist eine virtuelle Tastatur, die hauptsächlich für berührungsbasierte Geräte verwendet wird. Die Standardauswahl ist **Standardmäßige Betriebssystemtastatur**.
- **Logo Bild** – Sie können ein Logo-Bild angeben, das auf dem Anmeldebildschirm angezeigt wird. Wir empfehlen, ein Bild mit transparentem Hintergrund zu verwenden. Die Dateigröße von Hintergrundbildern sollte so gering wie möglich gehalten werden, da das Speichern und Hochladen großer Dateien Auswirkungen auf das Anwendungsverhalten und die Leistung haben könnte.
- **Anmeldungs-Hintergrund** – Sie können ein Hintergrundbild für die Bildschirm-Anmeldung angeben. Für das Hintergrundbild sollte die Bilddateigröße so gering wie möglich gehalten werden.
- **Hintergrund**- Sie können einen Hintergrund in der gesamten Anwendung anstelle der ausgefüllten Themenfarbe definieren. Bei Hintergrundbildern für den Anmeldebildschirm sollte die Dateigröße so klein wie möglich gehalten werden.

> [!NOTE]
> Das Layout **Rechts** und die Datums-/Uhrzeitanzeige gelten nicht für den Anmeldebildschirm in kompakter Ansicht.

## <a name="screen-layouts"></a>Bildschirmlayouts

Bildschirmlayoutkonfiguration bestimmt die Aktivitäten, Inhalte und die Platzierung von Benutzeroberflächen-Steuerelementen im POS- Bildschirm **Begrüßung** und **Transaktion**.

![POS-Bildschirmlayout anzeigen](../commerce/media/POS-Screen-Layout-View.png)

- **Begrüßungsbildschirm**- In den meisten Fällen ist der Begrüßungsbildschirm die Seite, die den Benutzern angezeigt wird, wenn sie sich in POS anmelden. Der Begrüßungsbildschirm kann aus einem Brandingbild und Schaltflächenrastern bestehen, die Zugriff auf POS-Arbeitsgänge bilden. In der Regel werden Arbeitsgänge, die nicht für die aktuelle Buchung bestimmt sind, hier platziert.

    ![POS-Willkommensbildschirm](../commerce/media/POS-Welcome-Screen.png)

- **Buchungsbildschirm** - Der **Buchungsbildschirm** ist der Hauptbildschirm in POS zur Verarbeitung von Verkaufsbuchungen und Aufträgen. Der Inhalt und das Layout werden mithilfe dem Bildschirmlayoutdesigner konfiguriert.

    ![POS-Transaktionsbildschirm](../commerce/media/POS-Transaction-Screen.png)

- **Standardanfangsbildschirm** - Einige Einzelhändler bevorzugen, dass der Kassierer direkt zum **Buchungsbildschirm** navigiert, nachdem er sich angemeldet hat. Mit der Einstellung **Standardanfangsbildschirm** können Sie den Standardbildschirm angeben, der nach der Anmeldung für jedes Bildschirmlayout angezeigt wird.

### <a name="assignment"></a>Zuweisung

Bildschirmlayouts können Unternehmen, Kassen oder Benutzern zugeweisen werden. Die Benutzer-Zuweisung setzt die Kassen- und Shopzuweisung außer Kraft, und die Kassen-Zuweisung setzt die Shopzuweisung außer Kraft. In einem einfachen Szenario, wo alle Benutzer das gleiche Layout unabhängig von der Kasse oder Rolle verwenden, kann das Bildschirmlayout nur für den Shop festgelegt werden. In Fällen, in denen bestimmte Kassen oder Benutzer spezielle Layouts erfordern, können sie ihnen zugeordnet werden.

### <a name="layout-sizes"></a>Layoutgrößen

Die meisten Aspekte der POS-Benutzeroberfläche sind reagierend, und das Layout wird automatisch basierend auf dem Bildumfang und der Ausrichtung der Größe geändert und angepasst. Zuvor müssen der Bildschirm POS **Buchung** für jede Bildschirmauflösung konfiguriert werden, die erwartet wird.

Die POS-Anwendung wählt automatisch die nächste Layoutgröße für das Gerät zum Zeitpunkt des Starts aus. Ein Bildschirmlayout kann für Konfigurationen Querformat und Hochformate und für die maximierten und kompakten Geräte angeben werden. Diese Konfiguration ermöglicht es, ein einzelnes Bildschirmlayout einem Benutzer zuzuordnen, der mit verschiedene Größen und Formularfaktoren im Shop arbeitet.

![POS_Layoutgrößen](../commerce/media/POS-Screen-Layout-Sizes.png)

- **Name** – Sie können einen aussagekräftigen Namen eingebem, um den Bildumfang zu identifizieren.
- **Layouttyp** – Die POS-Bewerbung kann eine Benutzeroberfläche in verschiedenen Arten anzeigen, um die beste Benutzerfreundlichkeit auf einem gegebenen Gerät bereitzustellen.

    - **Moderner POS - Vollständig** - Vollständige Layouts werden verwendet für große PC-Bildschirme oder Tablets. Benutzer können die Benutzeroberflächenelemente auswählen, die das Layout umfasst, die Größe und die Position dieser Elemente definieren und die detaillierten Eigenschaften anzeigen.. Vollständige Layouts unterstützen Hochformat- und Querformatkonfigurationen.
    - **Moderner POS - Kompakt** - Kompakte Layouts werden verwendet für kleine Telefone oder Tablets. Designmöglichkeiten werden für kompakte Geräte beschränkt. Benutzer können die Spalten und Felder für die Bereiche Empfang und Summen konfigurieren.

- **Breite/Höhe** – Diese Werte enthalten den tatsächlichen Bildumfang in Pixel, der für das Layout erwartet wird. Bedenken Sie, dass einige Skalierung Betriebssysteme für hochauflösende Anzeigen verwenden.

> [!TIP]
> Sie können die Layoutgröße ermitteln, die für einen POS-Bildschirm erforderlich ist, indem die Lösung in der Zeit-App angezeigt wird. POS starten und zu **Einstellungen \> Einstellungsinformationen** wechseln. POS zeigt das Bildschirmlayout, das gerade geladen wird, die Layoutgröße und die Auflösung des Apps-Fensters.

![POS-Layoutgrößen](../commerce/media/POS-Session-Information.png)

### <a name="button-grids"></a>Schaltflächenraster

Für jede Layoutgröße in einem Bildschirmlayout können Sie den POS-Begrüßungsbildschirm und den Bildschirm **Buchung** konfigurieren und zuweisen. Schaltflächenraster für den Begrüßungsbildschirm werden automatisch von links nach rechts, von der niedrigsten Nummer (Begrüßungsbildschirm 1) zur höchsten Nummer angezeigt.

Im vollständig POS-Layout wird die Position der Schaltflächenraster im Bildschirmlayoutdesigner angegeben.

Schaltflächenraster für den POS-Begrüßungsbildschirm werden automatisch von oben nach unten, von der niedrigsten Nummer (Transaktionsbildschirm 1) zur höchsten Nummer angezeigt. Sie können im Menü **Aktivitäten** darauf zugreifen.

![Kompakte Layoutschaltflächenraster](../commerce/media/Compact-View-Button-Grids.png)

### <a name="images"></a>Bilder

Für jede Layoutgröße in einem Bildschirmlayout, können Sie angeben, Bildern in der POS-Benutzeroberfläche einzubeziehen. Für POS-Layouts kann nur ein Bild für den Begrüßungsbildschirm angegeben werden. Das Bild wird als das erste Benutzeroberflächenelement auf der linken Seite angezeigt. Im Feld **Buchung** können Bilder als Registerkartenbilder oder als Logo verwendet werden. Kompakte POS-Layouts verwenden diese Bilder.

### <a name="screen-layout-designer"></a>Designer für Bildschirmlayout

Mit dem Bildschirmlayoutdesigner können Sie verschiedene Aspekte des Bildschirms POS **Buchung** für jede Layoutgröße, im Hochformat und imn Querformat und für vollständige und kompakte Layouts konfigurieren. Der Bildschirmlayoutdesigner verwendet ClickOnce, um die neueste Version der Anwendung herunterzuladen, zu installieren und zu starten, wenn der Benutzer darauf zugreift. Stellen Sie sicher, dass Sie die ClickOnce Browseranforderungen überprüfen. Einige Browser wie beispielsweise Google Chrome, benötigen Erweiterungen.

> [!IMPORTANT]
> Sie müssen eine Layoutgröße für jedes Bildschirmlayout konfigurieren, das definiert ist und vom POS verwendet wird.

### <a name="full-layout-designer"></a>Vollständiger Layout-Designer

Mit dem vollständigen Layoutbereich können Benutzer Benutzeroberflächen-Kontrollen auf dem Bildschirm POS **Buchung** und die Einstellungen dieser Kontrollen konfigurieren.

![Voller POS-Layoutbereich (Querformat)](../commerce/media/POS-Full-Layout-Designer-Landscape.png)

- **Importlayout/Exportlayout** – Sie können POS-Bildschirmlayoutdesigns als XML-Dateien exportieren und importieren, damit Sie diese leicht wiederverwenden und innerhalb der Umgebungen gemeinsam verwenden können. Es ist wichtig, dass Sie Layoutdesigns für die richtigen Layoutgrößen importieren. Andernfalls haben möglicherweise Benutzeroberflächenelemente, die nicht ordnungsgemäß auf den Bildschirm passen.
- **Querformat/Hochformat** – Wenn das POS-Gerät das Umschalten zwischen Quer- und Hochformaten zulässt, müssen Sie für jedes Bildschirmlayout einen Modus definieren. Der POS erkennt automatisch Bildschirmrotation und zeigt das gewünschte Layout an.
- **Layoutraster** – Der POS-Layoutdesigner verwendet ein Raster mit 4 Bilder. Benutzeroberflächen-Kontrollen "legen" sich am Raster aus, um Ihnen zu helfen, den Inhalt einwandfrei auszurichten.
- **Designerzoom** – Sie können die Designeransicht in ihrem Bericht vergrößern und verkleinern, um den Inhalt auf dem POS-Bildschirm besser anzuzeigen. Diese Funktion ist hilfreich, wenn die Bildschirmauflösung im POS sich extrem von der Auflösung des Monitors unterscheidet, der im Designer verwendet wird.
- **Navigationsleiste anzeigen/verbergen** – Für volle POS-Layouts können Sie auswählen, ob die linke Navigationsleiste auf dem Bildschirm **Buchung** angezeigt wird. Diese Funktion ist hilfreich für Anzeigen, die eine niedrigere Auflösung haben. Um die Sichtbarkeit festzulegen, klicken Sie auf die Navigationsleiste im Designer mit der rechten Maustaste und aktivieren oder deaktivieren das Kontrollkästchen **Immer angezeigt**. Wenn Die Navigationsleiste ausgeblendet wird, können POS-Benutzer trotzdem darauf zugreifen, indem sie das Menü im oberen linken Bereich verwenden.

    ![Navigationsleiste ein- oder ausblenden](../commerce/media/Navigation-Bar.PNG)

- **POS-Kontrollen** – Der POS-Layoutdesigner unterstützt die folgenden Kontrollen. Sie können eine Vielzahl von Steuerelementen konfigurieren, indem Sie auf das Kontextmenü mit der rechten Maustaste klicken und verwenden.

    ![POS-Steuerelemente](../commerce/media/POS-UI-Controls.png)

    - **Nummerpad** - Das Nummerpad ist die Hauptbenutzereingabe im POS-**Buchungs**-Bildschirm. Sie können das Steuerelement konfigurieren, sodass das gesamte Nummernpad angezeigt wird. Diese Option ist für Touchscreengeräte ideal. Alternativ können Sie sie konfigurieren, sodass nur das Eingabefeld angezeigt wird. In diesem Fall wird eine physische Tastatur zur Eingabe verwendet. Die Nummerpadeinstellungen sind nur im vollständigen Layout verfügbar. Für kompakte Layouts wird das vollständige Nummernpad immer auf dem Bildschirm **Buchung** angezeigt.
    - **Gesamtbereich** - Der Gesamtbereich kann anschließend in einer oder zwei Spalten so konfiguriert werden, dass Zeilenzähl-Felder wie Rabattbetrag, Gebühren, Steuern Zwischensumme angezeigt werden. Kompakte Layouts unterstützen nur eine einzelne Spalte.
    - **Empfangsbereich** - Der Empfangsbereich enthält die Verkaufspositionen, die Zahlungspositionen und die Lieferinformationen für die Produkte und Dienste, die am POS verarbeitet werden. Sie können Spalten, Breite und Position angeben. In den kompakten Layouts können Sie zusätzliche Informationen konfigurieren, die in der Zeile unter der Hauptlinie angezeigt werden.
    - **Kundenkarte** - Die Kundenkarte zeigt Informationen bezüglich des Kunden an, der momentan der Buchung zugeordnet ist. Die Kundenkarte kann so konfiguriert werden, dass zusätzliche Informationen angezeigt oder ausgeblendet werden.
    - **Registerkartensteuerelement** - Das Registerkartensteuerelement kann einem Bildschirmlayout hinzugefügt werden, um dann andere Steuerelemente wie Nummernpad, Kundenkarte oder Schaltflächenraster innerhalb der Registerkarte zu platzieren. Das Registerkartensteuerelement ist ein Container, der Ihnen hilft, mehr Inhalte im Bildschirm einzupassen. Das Registerkartensteuerelement ist für vollständige Layouts verfügbar.
    - **Bild**- Die Bildsteuerung kann verwendet werden, um das Shoplogo oder andere Brandingbilder im **Buchungs**bildschirm anzuzeigen. Das Bildsteuerelement ist nur für vollständige Layouts verfügbar.
    - **Empfohlene Produkte** - Sofern für die Umgebung konfiguriert, wird das Produktsteuerelement empfohlene Produktvorschläge auf Grundlage von Machine-Learning-Daten angezeigt.
    - **Benuterdefiniertes Steuerelement** - Das benutzerdefinierte Steuerlelement dient als Platzhalter innerhalb des Bildschirmlayouts das die Platzierung von benutzerdefinierten Inhalten zulässt. Das benutzerdefinierte Steuerelement ist hur für volle Layouts verfügbar.

### <a name="compact-layout-designer"></a>Kompaktes Bildschirmlayout

Wie der volle Layoutdesigner kann der kompakte Layoutdesigner POS-Bildschirmlayouts für Telefone und kleine Tablets konfigurieren. Jedoch in diesem Fall ist das Layout fix. Sie können eine Vielzahl von Steuerelementen im Layout konfigurieren, indem Sie auf das Kontextmenü mit der rechten Maustaste klicken und verwenden. Allerdings können Sie Drag & Drop-Vorgänge für zusätzlichen Inhalt nicht verwenden.

![Kompakter Layoutdesigner](../commerce/media/Compact-Layout-Designer.png)

### <a name="button-grid-designer"></a>Designer für Schaltflächenraster

Mit dem Schaltflächenrasterdesigner können Sie Schaltflächenraster konfigurieren, die für den POS-Begrüßungsbildschirm und den Bildschirm **Buchung** für volle und kompakte Layouts verwendet werden können. Der gleiche Schaltflächenraster kann für verschiedene Layouts und Layouttypen verwendet werden. Wie der Bildschirmlayoutdesigner verwendet der Schaltflächenrasterdesigner die ClickOnce Bereitstellung, um die neueste Version der Anwendung herunterzuladen, zu installieren und zu starten, wenn der Benutzer darauf zugreift. Stellen Sie sicher, dass Sie die ClickOnce Browseranforderungen überprüfen. Einige Browser wie beispielsweise Google Chrome, benötigen Erweiterungen.

![Designer für Schaltflächenraster](../commerce/media/Button-Grid-Designer.png)

- **Neue Schaltfläche** – Klicken Sie, um eine neue Schaltfläche im Schaltflächenraster hinzuzufügen. Standardmäßig werden neue Schaltflächen in der oberen linken Ecke des Rasters angezeigt. Allerdings können Sie Schaltflächen anordnen, indem Sie sie im Layout ziehen.

    > [!IMPORTANT]
    > Die Inhalte im Schaltflächenraster dürfen sich nicht überschneiden. Wenn Sie Schaltflächen anordnen, prüfen Sie, ob sie keine weiteren Schaltflächen ausblenden.

- **Neues Designf** - Klicken Sie, um automatisch ein Schaltflächenrasterlayouts einzurichten, indem Sie die Anzahl der Schaltflächen pro Zeile und Spalte definieren.
- **Schaltflächeneigenschaften** – Sie können Schaltflächeneigenschaften konfigurieren, indem Sie auf die Schaltfläche mit der rechten Maustaste klicken und das Kontextmenü verwenden.

    > [!IMPORTANT]
    > Einige Schaltflächenrastereinstellungen gelten nur für Enterprise POS und nicht für Modern POS oder Cloud POS.

    ![Eigenschaften von Schaltflächenraster](../commerce/media/Button-grid-button-properties.png)

    - **Aktivität** – In der Liste der POS-Arbeitsgängen, wählen Sie den entsprechenden Arbeitsgang aus, der aufgerufen wird, wenn im POS auf die Schaltfläche geklickt wird.

        Eine Liste der unterstützten POS-Operationen finden Sie unter [Online- und Offline-Point-of-Sale (POS)-Operationen](pos-operations.md).

    - **Aktivitätsparameter** – Einige zusätzliche Parameter der POS-Vorgänge Verwendung zusätzliche Parameter, wenn sie aufgerufen werden. Beispielsweise für das Hinzufügen von Arbeitsgängen können Benutzer das Produkt wählenn, das hinzugefügt werden soll..
    - **Text auf Schaltfläche** - Definieren Sie den Text, der auf der Schaltfläche im POS angezeigt werden soll.
    - **Ausblenden des Schaltflächentext** – Verwenden Sie dieses Kontrollkästchen, um den Schaltflächentext auszublenden oder anzeigen. Schaltflächentext wird häufig für kleine Schaltflächen ausgeblentet, die nur ein Symbol anzeigen.
    - **QuickInfo** – Zusätzlichen Hilfetext definieren, der erscheint, wenn der Benutzer mit der Maus über die Schaltfläche fährt.
    - **Größe in Spalten und Größe in Zeilen** – Sie können wie groß und wie breit die Schaltfläche ist.

        ![POS-Schaltflächengrößen in Zeilen und Spalten](../commerce/media/POS-Button-Sizes-In-Rows-And-Columns.png)

    - **Kundenspezifische Schriftart** – Wenn Sie das Kontrollkästchen **Aktivieren von benutzerdefinierter Schriftart für POS** aktivieren, können Sie eine Schriftart definieren, die keine Standardsystemschriftart für POS ist.
    - **Benutzerdefiniertes Thema** – POS-Schaltflächen verwenden standardmäßig die Akzentfarbe des visuellen Profils. Wenn Sie das Kontrollkästchen **Benutzerdefiniertes Design verwenden** aktivieren, können Sie ggf. zusätzliche Farben angeben.

        > [!NOTE]
        > Retail Modern POS und Cloud POS nutzen nur die **Hintergrundfarbe** und die **Schriftfarbe**.

    - **Schaltflächensymbol** – Symbole können Schaltflächen oder Bilder einschließen. Wählen Sie eines der verfügbaren Bilder aus, die als **Retail und Commerce \> Kanaleinstellung \> POS-Einstellung \> POS \> Bilder** angegeben werden.

![Beispielsschaltflächenraster im POS](../commerce/media/Example-Button-Grid-In-POS.png)

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Den Retail-Verkaufstellen-(POS)-Layout-Designer installieren](install-pos-layout-designer.md)
