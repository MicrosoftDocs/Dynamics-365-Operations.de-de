---
title: "Bildschirmlayouts für die Verkaufsstelle (POS)"
description: "Dieses Thema enthält Informationen zu Bildschirmlayouts für Microsoft Dynamics 365 for Retail -POS-Erfahrungen."
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailTillLayout
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 90573
ms.assetid: a6868f93-02ed-4928-9f6a-3b7383e7e399
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: dda9c8cb7f3da99fb2e7df0372e59769cfaf77d1
ms.openlocfilehash: ced27adb8fe481270cb008e187693cda96773339
ms.contentlocale: de-de
ms.lasthandoff: 11/13/2018

---

# <a name="screen-layouts-for-the-point-of-sale-pos"></a>Bildschirmlayouts für die Verkaufsstelle (POS)

[!include [banner](includes/banner.md)]

Dieses Thema enthält Informationen zu Bildschirmlayouts für Microsoft Dynamics 365 for Retail -POS-Erfahrungen.

Die Retail-POS-Benutzeroberfläche (UI) kann mithilfe einer Kombination von visuellen Profilen und Bildschirmlayouts konfiguriert werden, die Shops, Kassen und/oder den Benutzern zugewiesen sind.

Die folgende Abbildung zeigt die Beziehungen zwischen den unterschiedlichen Entitäten, die die konfigurierbare POS-Benutzeroberfläche bilden.

![Entität für POS-Bildschirmlayout](../retail/media/POS-layout-configuration-entities-diagram.png)

## <a name="visual-profile"></a>Visuelles Profil
Visuelle Profile werden für die Kassen zugewiesen und werden verwendet, um die Sichtelementen anzugeben, die kassenspezifisch sind und gemeinsam genutzt werden. Jeder Benutzer, der sich an der Kasse anmeldet, sieht dasselbe Thema, Farben und Bilder.

![POS-Begrüßungsbildschirm mit hellem Thema](../retail/media/POS-Welcome-Screen-with-Light-theme.png)

![POS-Buchungs-Bildschirm mit dunklem Thema](../retail/media/POS-Transaction-Screen-with-Dark-theme.png)

- **Profilnummer** Die Profilnummer für die eindeutige Kennung für das visuelle Profil.
- **Beschreibung** - Die Beschreibung ermöglicht es Ihnen, einen beschreibenden Namen angeben, der Ihnen hilft, das richtige Profil für in Ihrer Situation zu identifizieren.
- **Thema** - Sie können zwischen den hellen oder dunklen Anwendungsdesigns auswählen. Das Thema betrifft die gewünschten Schrift- und Hintergrundfarben in der Anwendung.
- **Akzentfarbe** - Die Akzentfarbe wird im POS verwendet, um bestimmte Sichtelemente wie Kacheln, Befehlsschaltflächen oder Links zu unterscheiden oder hervorzuheben. Diese Elemente sind in der Regel aktiv.
- **Kopffarbe** – Sie können die Farbe der Kopfzeile konfigurieren, um die Brandingbedingungen des Einzelhändlers zu erfüllen. Diese Funktion ist nur in Microsoft Dynamics 365 for Retail, Version 1611, verfügbar.
- **Anmeldungs-Hintergrund** - Sie können ein Hintergrundbild für die Bildschirm-Anmeldung angeben. Die Dateigröße von Hintergrundbildern sollte so gering wie möglich gehalten werden, da das Speichern und Hochladen großer Dateien Auswirkungen auf das Anwendungsverhalten und die Leistung haben kann.
- **Anwendungshintergrund**- Sie können einen Hintergrund in der gesamten Anwendung anstelle der ausgefüllten Themenfarbe definieren. Für den Anmelde-Hintergrund sollte die Dateigröße so gering wie möglich gehalten werden.

## <a name="screen-layouts"></a>Bildschirmlayouts
Bildschirmlayoutkonfiguration bestimmt die Aktivitäten, Inhalte und die Platzierung von Benutzeroberflächen-Steuerelementen im POS-Begrüßungsbildschirm- und -**Buchungs**-Bildschirm.

![POS-Bildschirmlayout anzeigen](../retail/media/POS-Screen-Layout-View.png)

- **Begrüßungsbildschirm**- In den meisten Fällen ist der Begrüßungsbildschirm die Seite, die den Benutzern angezeigt wird, wenn sie sich in POS anmelden. Der Begrüßungsbildschirm kann aus einem Brandingbild und Schaltflächenrastern bestehen, die Zugriff auf POS-Arbeitsgänge bilden. In der Regel werden Arbeitsgänge, die nicht für die aktuelle Buchung bestimmt sind, hier platziert.

    ![POS-Willkommensbildschirm](../retail/media/POS-Welcome-Screen.png)

- **Buchungsbildschirm** - Der **Buchungsbildschirm** ist der Hauptbildschirm in POS zur Verarbeitung von Verkaufsbuchungen und Aufträgen. Der Inhalt und das Layout werden mithilfe dem Bildschirmlayoutdesigner konfiguriert.

    ![POS-Transaktionsbildschirm](../retail/media/POS-Transaction-Screen.png)

- **Standardanfangsbildschirm** - Einige Einzelhändler bevorzugen, dass der Kassierer direkt zum **Buchungsbildschirm** navigiert, nachdem er sich angemeldet hat. Mit der Einstellung **Standardanfangsbildschirm** können Sie den Standardbildschirm angeben, der nach der Anmeldung für jedes Bildschirmlayout angezeigt wird.

### <a name="assignment"></a>Zuweisung

Bildschirmlayouts können Unternehmen, Kassen oder Benutzern zugeweisen werden. Die Benutzer-Zuweisung setzt die Kassen- und Shopzuweisung außer Kraft, und die Kassen-Zuweisung setzt die Shopzuweisung außer Kraft. In einem einfachen Szenario, wo alle Benutzer das gleiche Layout unabhängig von der Kasse oder Rolle verwenden, kann das Bildschirmlayout nur für den Shop festgelegt werden. In Fällen, in denen bestimmte Kassen oder Benutzer spezielle Layouts erfordern, können sie ihnen zugeordnet werden.

### <a name="layout-sizes"></a>Layoutgrößen

Die meisten Aspekte der POS-Benutzeroberfläche sind reagierend, und das Layout wird automatisch basierend auf dem Bildumfang und der Ausrichtung der Größe geändert und angepasst. Zuvor müssen der Bildschirm POS **Buchung** für jede Bildschirmauflösung konfiguriert werden, die erwartet wird.

Die POS-Anwendung wählt automatisch die nächste Layoutgröße für das Gerät zum Zeitpunkt des Starts aus. Ein Bildschirmlayout kann für Konfigurationen Querformat und Hochformate und für die maximierten und kompakten Geräte angeben werden. Diese Konfiguration ermöglicht es, ein einzelnes Bildschirmlayout einem Benutzer zuzuordnen, der mit verschiedene Größen und Formularfaktoren im Shop arbeitet.

![POS_Layoutgrößen](../retail/media/POS-Screen-Layout-Sizes.png)

- **Name** – Sie können einen aussagekräftigen Namen eingebem, um den Bildumfang zu identifizieren.
- **Layouttyp** – Die POS-Bewerbung kann eine Benutzeroberfläche in verschiedenen Arten anzeigen, um die beste Benutzerfreundlichkeit auf einem gegebenen Gerät bereitzustellen.

    - **Moderner POS - Vollständig** - Vollständige Layouts werden verwendet für große PC-Bildschirme oder Tablets. Benutzer können die Benutzeroberflächenelemente auswählen, die das Layout umfasst, die Größe und die Position dieser Elemente definieren und die detaillierten Eigenschaften anzeigen.. Vollständige Layouts unterstützen Hochformat- und Querformatkonfigurationen.
    - **Moderner POS - Kompakt** - Kompakte Layouts werden verwendet für kleine Telefone oder Tablets. Designmöglichkeiten werden für kompakte Geräte beschränkt. Benutzer können die Spalten und Felder für die Bereiche Empfang und Summen konfigurieren.

- **Breite/Höhe** – Diese Werte enthalten den tatsächlichen Bildumfang in Pixel, der für das Layout erwartet wird. Bedenken Sie, dass einige Skalierung Betriebssysteme für hochauflösende Anzeigen verwenden.

> [!TIP]
> Sie können die Layoutgröße ermitteln, die für einen POS-Bildschirm erforderlich ist, indem die Lösung in der Zeit-App angezeigt wird. POS starten und zu **Einstellungen \> Einstellungsinformationen** wechseln. POS zeigt das Bildschirmlayout, das gerade geladen wird, die Layoutgröße und die Auflösung des Apps-Fensters.

![POS-Layoutgrößen](../retail/media/POS-Session-Information.png)

### <a name="button-grids"></a>Schaltflächenraster
Für jede Layoutgröße in einem Bildschirmlayout können Sie den POS-Begrüßungsbildschirm und den Bildschirm **Buchung** konfigurieren und zuweisen. Schaltflächenraster für den Begrüßungsbildschirm werden automatisch von links nach rechts, von der niedrigsten Nummer (Begrüßungsbildschirm 1) zur höchsten Nummer angezeigt.

Im vollständig POS-Layout wird die Position der Schaltflächenraster im Bildschirmlayoutdesigner angegeben.

Schaltflächenraster für den POS-Begrüßungsbildschirm werden automatisch von oben nach unten, von der niedrigsten Nummer (Transaktionsbildschirm 1) zur höchsten Nummer angezeigt. Sie können im Menü **Aktivitäten** darauf zugreifen.

![Kompakte Layoutschaltflächenraster](../retail/media/Compact-View-Button-Grids.png)

### <a name="images"></a>Bilder
Für jede Layoutgröße in einem Bildschirmlayout, können Sie angeben, Bildern in der POS-Benutzeroberfläche einzubeziehen. Für POS-Layouts kann nur ein Bild für den Begrüßungsbildschirm angegeben werden. Das Bild wird als das erste Benutzeroberflächenelement auf der linken Seite angezeigt. Im Feld **Buchung** können Bilder als Registerkartenbilder oder als Logo verwendet werden. Kompakte POS-Layouts verwenden diese Bilder.

### <a name="screen-layout-designer"></a>Designer für Bildschirmlayout

Mit dem Bildschirmlayoutdesigner können Sie verschiedene Aspekte des Bildschirms POS **Buchung** für jede Layoutgröße, im Hochformat und imn Querformat und für vollständige und kompakte Layouts konfigurieren. Der Bildschirmlayoutdesigner verwendet ClickOnce, um die neueste Version der Anwendung herunterzuladen, zu installieren und zu starten, wenn der Benutzer darauf zugreift. Stellen Sie sicher, dass Sie die ClickOnce Browseranforderungen überprüfen. Einige Browser wie beispielsweise Google Chrome, benötigen Erweiterungen.

> [!IMPORTANT]
> Sie müssen eine Layoutgröße für jedes Bildschirmlayout konfigurieren, das definiert ist und vom POS verwendet wird.

### <a name="full-layout-designer"></a>Vollständiger Layout-Designer

Mit dem vollständigen Layoutbereich können Benutzer Benutzeroberflächen-Kontrollen auf dem Bildschirm POS **Buchung** und die Einstellungen dieser Kontrollen konfigurieren.

![Voller POS-Layoutbereich (Querformat)](../retail/media/POS-Full-Layout-Designer-Landscape.png)

- **Importlayout/Exportlayout** – Sie können POS-Bildschirmlayoutdesigns als XML-Dateien exportieren und importieren, damit Sie diese leicht wiederverwenden und innerhalb der Umgebungen gemeinsam verwenden können. Es ist wichtig, dass Sie Layoutdesigns für die richtigen Layoutgrößen importieren. Andernfalls haben möglicherweise Benutzeroberflächenelemente, die nicht ordnungsgemäß auf den Bildschirm passen.
- **Querformat/Hochformat** – Wenn das POS-Gerät das Umschalten zwischen Quer- und Hochformaten zulässt, müssen Sie für jedes Bildschirmlayout einen Modus definieren. Der POS erkennt automatisch Bildschirmrotation und zeigt das gewünschte Layout an.
- **Layoutraster** – Der POS-Layoutdesigner verwendet ein Raster mit 4 Bilder. Benutzeroberflächen-Kontrollen "legen" sich am Raster aus, um Ihnen zu helfen, den Inhalt einwandfrei auszurichten.
- **Designerzoom** – Sie können die Designeransicht in ihrem Bericht vergrößern und verkleinern, um den Inhalt auf dem POS-Bildschirm besser anzuzeigen. Diese Funktion ist hilfreich, wenn die Bildschirmauflösung im POS sich extrem von der Auflösung des Monitors unterscheidet, der im Designer verwendet wird.
- **Navigationsleiste anzeigen/verbergen** – Für volle POS-Layouts können Sie auswählen, ob die linke Navigationsleiste auf dem Bildschirm **Buchung** angezeigt wird. Diese Funktion ist hilfreich für Anzeigen, die eine niedrigere Auflösung haben. Um die Sichtbarkeit festzulegen, klicken Sie auf die Navigationsleiste im Designer mit der rechten Maustaste und aktivieren oder deaktivieren das Kontrollkästchen **Immer angezeigt**. Wenn Die Navigationsleiste ausgeblendet wird, können POS-Benutzer trotzdem darauf zugreifen, indem sie das Menü im oberen linken Bereich verwenden.

    ![Navigationsleiste ein- oder ausblenden](../retail/media/Navigation-Bar.PNG)

- **POS-Kontrollen** – Der POS-Layoutdesigner unterstützt die folgenden Kontrollen. Sie können eine Vielzahl von Steuerelementen konfigurieren, indem Sie auf das Kontextmenü mit der rechten Maustaste klicken und verwenden.

    ![POS-Steuerelemente](../retail/media/POS-UI-Controls.png)

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

![Kompakter Layoutdesigner](../retail/media/Compact-Layout-Designer.png)

### <a name="button-grid-designer"></a>Designer für Schaltflächenraster
Mit dem Schaltflächenrasterdesigner können Sie Schaltflächenraster konfigurieren, die für den POS-Begrüßungsbildschirm und den Bildschirm **Buchung** für volle und kompakte Layouts verwendet werden können. Der gleiche Schaltflächenraster kann für verschiedene Layouts und Layouttypen verwendet werden. Wie der Bildschirmlayoutdesigner verwendet der Schaltflächenrasterdesigner die ClickOnce Bereitstellung, um die neueste Version der Anwendung herunterzuladen, zu installieren und zu starten, wenn der Benutzer darauf zugreift. Stellen Sie sicher, dass Sie die ClickOnce Browseranforderungen überprüfen. Einige Browser wie beispielsweise Google Chrome, benötigen Erweiterungen.

![Designer für Schaltflächenraster](../retail/media/Button-Grid-Designer.png)

- **Neue Schaltfläche** – Klicken Sie, um eine neue Schaltfläche im Schaltflächenraster hinzuzufügen. Standardmäßig werden neue Schaltflächen in der oberen linken Ecke des Rasters angezeigt. Allerdings können Sie Schaltflächen anordnen, indem Sie sie im Layout ziehen.

    > [!IMPORTANT]
    > Die Inhalte im Schaltflächenraster dürfen sich nicht überschneiden. Wenn Sie Schaltflächen anordnen, prüfen Sie, ob sie keine weiteren Schaltflächen ausblenden.

- **Neues Designf** - Klicken Sie, um automatisch ein Schaltflächenrasterlayouts einzurichten, indem Sie die Anzahl der Schaltflächen pro Zeile und Spalte definieren.
- **Schaltflächeneigenschaften** – Sie können Schaltflächeneigenschaften konfigurieren, indem Sie auf die Schaltfläche mit der rechten Maustaste klicken und das Kontextmenü verwenden.

    > [!IMPORTANT]
    > Einige Schaltflächenrastereinstellungen gelten nur Enterprise POS und nicht für Retail Modern POS oder Cloud POS.

    ![Eigenschaften von Schaltflächenraster](../retail/media/Button-grid-button-properties.png)

    - **Aktivität** – In der Liste der POS-Arbeitsgängen, wählen Sie den entsprechenden Arbeitsgang aus, der aufgerufen wird, wenn im POS auf die Schaltfläche geklickt wird.

        Für die Liste der unterstützten POS-Arbeitsgänge gehen Sie zu [POS-Vorgängen, online oder offline](pos-operations.md).

    - **Aktivitätsparameter** – Einige zusätzliche Parameter der POS-Vorgänge Verwendung zusätzliche Parameter, wenn sie aufgerufen werden. Beispielsweise für das Hinzufügen von Arbeitsgängen können Benutzer das Produkt wählenn, das hinzugefügt werden soll..
    - **Text auf Schaltfläche** - Definieren Sie den Text, der auf der Schaltfläche im POS angezeigt werden soll.
    - **Ausblenden des Schaltflächentext** – Verwenden Sie dieses Kontrollkästchen, um den Schaltflächentext auszublenden oder anzeigen. Schaltflächentext wird häufig für kleine Schaltflächen ausgeblentet, die nur ein Symbol anzeigen.
    - **QuickInfo** – Zusätzlichen Hilfetext definieren, der erscheint, wenn der Benutzer mit der Maus über die Schaltfläche fährt.
    - **Größe in Spalten und Größe in Zeilen** – Sie können wie groß und wie breit die Schaltfläche ist.

        ![POS-Schaltflächengrößen in Zeilen und Spalten](../retail/media/POS-Button-Sizes-In-Rows-And-Columns.png)

    - **Kundenspezifische Schriftart** – Wenn Sie das Kontrollkästchen **Aktivieren von benutzerdefinierter Schriftart für POS** aktivieren, können Sie eine Schriftart definieren, die keine Standardsystemschriftart für POS ist.
    - **Benutzerdefiniertes Thema** – POS-Schaltflächen verwenden standardmäßig die Akzentfarbe des visuellen Profils. Wenn Sie das Kontrollkästchen **Benutzerdefiniertes Design verwenden** aktivieren, können Sie ggf. zusätzliche Farben angeben.

        > [!NOTE]
        > Retail Modern POS und Cloud POS nutzen nur die **Hintergrundfarbe** und die **Schriftfarbe**.

    - **Schaltflächensymbol** – Symbole können Schaltflächen oder Bilder einschließen. Wählen Sie eines der verfügbaren Bilder aus, die als **Einzelhandel \> Kanaleinstellung \> POS-Einstellung \> POS \> Bilder** angegeben werden.

![Beispielsschaltflächenraster im POS](../retail/media/Example-Button-Grid-In-POS.png)

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Den Retail POS-Layout-Designer installieren](install-pos-layout-designer.md)

