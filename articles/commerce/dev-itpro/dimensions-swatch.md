---
title: Konfigurieren Sie Produktdimensionswerte so, dass sie als Farbfelder angezeigt werden
description: In diesem Artikel wird beschrieben, wie Sie Produktdimensionswerte als Farbfelder in der Microsoft Dynamics 365 Commerce Zentralverwaltung konfigurieren.
author: anupamar-ms
ms.date: 08/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2020-09-20
ms.dyn365.ops.version: Retail 10.0.20 update
ms.custom: ''
ms.search.industry: Retail
ms.openlocfilehash: e81c1f03eb6387176ca5ce8f751ce53aa0261679
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9271989"
---
# <a name="configure-product-dimension-values-to-appear-as-swatches"></a>Konfigurieren Sie Produktdimensionswerte so, dass sie als Farbfelder angezeigt werden

[!include [banner](../../includes/banner.md)]

In diesem Artikel wird beschrieben, wie Sie Produktdimensionswerte als Farbfelder in der Microsoft Dynamics 365 Commerce Zentralverwaltung konfigurieren. Weitere Informationen über Produktdimensionen finden Sie unter [Produktdimensionen](../../supply-chain/pim/product-dimensions.md).

Dynamics 365 Commerce unterstützt die Verwendung von Größe, Stil und Farbabmessungen zur Darstellung von Produktvarianten. Produktabmessungen haben Anzeigenamen, die auf Produktdetailseiten (PDPs) angezeigt werden, damit Produktvarianten ausgewählt werden können. Beispiele für diese Anzeigenamen sind Klein, Mittel und Groß für Größen und Schwarz und Braun für Farben. Wenn ein Produkt jedoch viele Variationen unterstützt, sind mehrere Auswahlen erforderlich, um das Bild für jede Produktvariante anzuzeigen. Daher kann es für Kunden langsam und mühsam sein, Produktvarianten zu durchsuchen und auszuwählen.

Wenn Abmessungen auf PDPs als Farbfelder angezeigt werden, erhalten Kunden eine visuelle Vorschau der Produktvarianten. Sie können problemlos eine Vielzahl von Farben, Mustern und Texturen durchsuchen und schnell verschiedene Kombinationen von Produktvarianten anzeigen.

Mit der Funktion Abmessungen als Farbfelder anzeigen kann Commerce hexadezimale (hex) Codes und Bilder verwenden, um Abmessungen als Farbfelder anzuzeigen. Darüber hinaus können ähnliche Abmessungen, z. B. Farben, auf Produktlistenseiten gruppiert werden. Ein Kunde sucht beispielsweise nach blauen Produkten. Wenn die verschiedenen blauen Bemaßungswerte zusammengefasst sind, werden auf der Seite mit der Suchergebnisliste Produkte mit unterschiedlichen Blautönen angezeigt. Die Gruppierung von Dimensionen verbessert das Produktverfeinerungserlebnis erheblich und hilft Kunden, durch eine einzige Produktsuchabfrage mehr Produkte zu finden.

> [!NOTE]
> Die Funktion Anzeigeabmessungen als Farbfelder ist ab Dynamics 365 Commerce Version 10.0.20 Release verfügbar.

Die folgende Abbildung zeigt ein Beispiel, in dem Farben auf einem Commerce-PDP als Farbfelder angezeigt werden.

![Beispiel für Farben, die auf einer Produktdetailseite als Farbfelder angezeigt werden.](../dev-itpro/media/swatch_pdp.png)

Die folgende Abbildung zeigt ein Beispiel, in dem Farben auf einer Commerce Suchergebnis-Listenseite als Farbfelder angezeigt werden.

![Beispiel für Farben, die auf einer Suchergebnislistenseite als Farbfelder angezeigt werden.](../dev-itpro/media/swatch_searchresults.PNG)

## <a name="enable-the-display-dimensions-as-swatches-feature-in-commerce-headquarters"></a>Aktivieren Sie die Anzeigeabmessungen als Farbfelder in der Commerce-Zentralverwaltung

Um die Anzeigeabmessungen als Muster in der Commerce-Zentralverwaltung zu aktivieren, gehen Sie zu **Arbeitsbereiche \> Funktionsverwaltung** und aktivieren Sie die Funktion **Mechanismus zur Darstellung von Dimensionen als Muster aktivieren**. Wenn dieses Funktionsflag aktiviert ist, werden drei neue Felder für jede Dimension in den entsprechenden Tabellen in der Commerce-Zentraverwaltung hinzugefügt: **Hexcode**, **URL** (für Bilder) und **RefinerGroup**.

## <a name="configure-dimension-values-in-commerce-headquarters"></a>Konfigurieren Sie Dimensionswerte in der Commerce-Zentralverwaltung

Die Funktion Anzeigeabmessungen als Farbfelder wird für Größe, Stil und Farbabmessungen unterstützt. Hexadezimalcode- und Bild-URL-Werte für die entsprechenden Abmessungen können in der Commerce-Zentralverwaltung angegeben werden. Wenn für eine Dimension keine Hexadezimalcode- und Bild-URL-Werte angegeben sind, zeigt das System standardmäßig den Text des Anzeigenamens der Dimension an.

Die Konfiguration kann auf einer der folgenden Ebenen erfolgen:

- **Abmessungen** – Öffnen Sie in der Commerce-Zentralverwaltung die Seite für eine Dimension, indem Sie nach **Farbe**, **Größe**, oder **Stil** suchen. Auf jeder Seite führt ein Raster die Dimensionswerte auf. Sie können die Anzeigereihenfolge, den Hexadezimalcode und die Bild-URL-Werte verwalten. Die folgende Abbildung zeigt eine Beispielkonfiguration der Seite **Farben**.

    ![Beispiel für die Bemessungskonfiguration auf der Seite Farben.](../dev-itpro/media/swatch_Color.PNG)

- **Dimensionsgruppe** – In Dynamics 365 Commerce können Sie die Eigenschaft **RefinerGroup** verwenden, um die Dimensionsgruppen zu erstellen. Wenn Dimensionsgruppen definiert sind, öffnen Sie die entsprechende Seite, indem Sie nach **Farbgruppe**, **Größengruppe** oder **Stilgruppe** suchen. Auf jeder Seite können Sie Hexadezimalcode, Bild-URL und Refiner-Gruppenwerte verwalten. Die folgende Abbildung zeigt eine Beispielkonfiguration der Seite **Farbgruppen**.

    ![Beispiel für die Bemessungskonfiguration auf der Seite Farbgruppen.](../dev-itpro/media/swatch_colorGroup.PNG)

- **Produktdimension (während der Produkterstellung)** – Wenn Sie ein neues Produkt erstellen, können Sie die Seite **Produktabmessungen** verwenden, um die Bemeßungswerte einzugeben. Für bestehende Produkte sind die Felder **Hexcode**, **URL** (für Bilder) und **RefinerGroup** möglicherweise bereits festgelegt. Allerdings können Sie die Werte in diesem Feld ändern. Die folgende Abbildung zeigt eine Beispielkonfiguration der Seite **Produktdimensionen**.

    ![Beispiel für die Bemessungskonfiguration auf der Seite Produktdimensionen.](../dev-itpro/media/swatch_product_dimensions.PNG)

> [!NOTE]
> Der Prozess zum Verwalten von Hexadezimalcode- und Bild-URL-Konfigurationen folgt demselben Muster, das zum Verwalten der Anzeigereihenfolge von Dimensionen verwendet wird.

## <a name="configure-dimension-values-by-using-hex-codes"></a>Konfigurieren Sie Bemeßungswerte mithilfe von Hexadezimalcodes

Für die meisten Farbdimensionen sollte auf den Dimensionsseiten in der Commerce-Zentralverwaltung ein Hexadezimalcode-Farbwert angegeben werden. Zum Beispiel sollte die Farbe Schwarz einen Hexadezimalcode-Wert von **#00000** haben. Wenn Commerce eine Site-Seite rendert, wird der Hexadezimalcode durch ein farbiges Farbfeld dargestellt.

Die folgende Abbildung zeigt ein Beispiel, in dem Farbabmessungen mithilfe von Hexadezimalcode-Werten konfiguriert werden.

![Beispiel für die Bemessungskonfiguration, die Hexcodes verwendet.](../dev-itpro/media/swatch_color_hexcode.png)

## <a name="configure-dimension-values-by-using-image-urls"></a>Konfigurieren Sie Bemeßungswerte mithilfe der Bild-URLs

Einige Farbabmessungen repräsentieren Muster, keine ausgefüllten Farben. Zum Beispiel könnte eine Farbdimension als Leopard beschrieben werden. In diesen Fällen können Sie die Farbabmessungen effektiver darstellen, indem Sie veröffentlichte Bilder anstelle von Hexadezimalcodes für Farbfelder verwenden.

Sie müssen jedes Bild in den Commerce Site Builder hochladen und veröffentlichen. Geben Sie dann die Bild-URL für das veröffentlichte Bild auf den entsprechenden Dimensionsseiten in der Commerce-Zentralverwaltung ein. Wenn eine Dimension für die Anzeige als Farbfeld ausgewählt wurde, aber kein Hexadezimalcode definiert ist, führt Commerce beim Rendern der Seite eine Bildsuche durch. Wenn die Bildsuche fehlschlägt, zeigt Commerce den Text des Anzeigenamens der Dimension an.

Die folgende Abbildung zeigt eine Beispielkonfiguration, bei der Bild-URLs für die Konfiguration auf der Seite **Farben** verwendet wird.

![Beispiel für die Bemessungskonfiguration, die Bild-URLs verwendet.](../dev-itpro/media/swatch_color_urls.PNG)

Sie können eine Medienvorlage verwenden, um Bild-URLs zu definieren, genau wie Sie es für Produkt- und Kategoriebilder tun können. Wenn Sie Bilder in den Site Builder hochladen, müssen die Dateinamenkonventionen und Dateipfade konsistent sein.

Die folgende Abbildung zeigt eine Beispielkonfiguration, bei der Bild-URLs für die Konfiguration von Medienvorlagen verwendet werden.

![Beispiel für die Konfiguration von Medienvorlagen.](../dev-itpro/media/swatch_media_template.PNG)

## <a name="configure-dimension-values-by-using-both-hex-codes-and-image-urls"></a>Konfigurieren Sie Bemeßungswerte mithilfe von Hexadezimalcodes und Bild-URLs

Für die meisten Farbabmessungen können Sie sowohl Hexadezimalcodes als auch Bild-URLs konfigurieren. Die Commerce-Rendering-Fallback-Logik sucht automatisch nach einem Hexadezimalcode oder einer Bild-URL, um ein Farbfeld anzuzeigen. Indem Sie zum Konfigurieren der Farbabmessungen sowohl Hexadezimalcodes als auch Bild-URLs verwenden, vereinfachen Sie die Bildverwaltung, wenn die Anzahl der Farben groß ist.

Die folgende Abbildung zeigt eine Beispielkonfiguration, bei der Hexadezimalcodes und Bild-URLs für die Konfiguration auf der Seite **Farben** verwendet wird.

![Beispiel für die Bemessungskonfiguration, die Bild-URLs und Hexcodes verwendet.](../dev-itpro/media/swatch_color_hexandimage.png)

## <a name="configure-refiner-groups"></a>Konfigurieren Sie Verfeinerungs-Gruppen

Wenn Sie einen Hexadezimalcode oder eine Bild-URL für einen Dimensionswert definieren, können Sie auch einen Wert für das Feld **Verfeinerungsgruppe** definieren. Dieses Feld definiert die Dimension, die verwendet werden soll, um ähnliche Dimensionswerte in der Verfeinerungs-Erfahrung zu gruppieren.

Wenn Ihre Farbdimensionswerte beispielsweise blau, blau kariert, blau gewaschen und dunkelblau sind, wird jeder Wert einem anderen Hexadezimalcode oder einer anderen Bild-URL zugeordnet. Daher wird jeder Wert auf PDPs und Produktkarten für die entsprechenden Produkte in einer anderen Farbe angezeigt. Wenn Sie jedoch alle diese Farbbemaßungswerte einem Wert **RefinerGroup** von **Blau** zuordnen, werden bei einer Suche nach blauen Produkten Suchergebnisse für Listenseiten für Produkte mit den Dimensionsfarbwerten blau, blau kariert, blaue Waschung und dunkelblau generiert.

Das Beispiel in der folgenden Abbildung zeigt die Beziehung zwischen den Eigenschaften **Farbe** und **RefinerGroup** in der Commerce Zentralverwaltung.

![Beispiel für die Verwaltung von Verfeinerungsgruppen.](../dev-itpro/media/swatch_refiner_group.png)

## <a name="manage-images-in-commerce-site-builder"></a>Bilder im Commerce-Website-Generator verwalten

Wenn Bild-URLs für Dimensionswerte verwendet werden, müssen die entsprechenden Bilder in den Commerce Website-Generator hochgeladen werden. Der Speicherort jedes Bildes sollte mit dem Dateinamen und dem Ordnerpfad übereinstimmen, der für das Bild in der Commerce-Zentralverwaltung definiert ist. Bilddateien müssen an die entsprechenden Speicherorte der Kategorie im Website-Generator hochgeladen werden. Beispielsweise müssen Farbbilder auf die Website in den Kategorienordner **Farbe** hochgeladen werden. Weitere Informationen zum Hochladen von Bildern in die Website-Generator-Medienbibliothek finden Sie unter [Bilder hochladen](../dam-upload-images.md).

Die folgende Abbildung zeigt ein Beispiel, in dem das Dialogfeld **Daten hochladen** verwendet wird, um Bilder in die Website-Generator-Medienbibliothek hochzuladen. Es hebt die Kategorien **Größe**, **Farbe** und **Stil** hervor, die zur Auswahl stehen.

![Beispiel für Bilddateikategorien beim Hochladen in die Website-Generator-Medienbibliothek.](../dev-itpro/media/swatch_sitebuilder.png)

## <a name="enable-swatch-display-on-e-commerce-site-pages"></a>Aktivieren Sie die Farbfeldanzeige auf E-Commerce-Webseiten

Bevor Farbfelder auf E-Commerce-Webseiten angezeigt werden können, für die eine Dimensionsauswahl erforderlich ist, z. B. PDPs und Listenseiten, müssen Sie die Einstellungen für Dimensionsstandorte in der Commerce-Zentralverwaltung konfigurieren. Weitere Informationen finden Sie unter [Wenden Sie den Website-Generator für die Abmessungen an](../dimension-settings.md).

Außerdem sollten Sie die Eigenschaft **Produktattribute in Suchergebnisse aufnehmen** für Suchergebnismodule aktivieren. Wenn Ihre Website angepasste Kategorieseiten verwendet, sollten Sie die auf diesen Seiten verwendeten Suchergebnismodule aktualisieren, damit die Eigenschaft **Produktattribute in Suchergebnisse aufnehmen** aktiviert ist. Weitere Informationen finden Sie unter [Modul Suchergebnisse](../search-result-module.md).

## <a name="inventory-awareness-on-swatches"></a>Bestandsinformationen auf Mustern

Muster haben eine optionale Funktion, um die Bestandsverfügbarkeit einer Produktvariantenfarbe oder -dimension anzuzeigen. Zum Beispiel: Ein Produkt wird in mehreren Größen verkauft, einige Größen sind jedoch nicht auf Lager. In diesem Fall werden die Muster für die vergriffenen Produkte anders dargestellt, um anzuzeigen, dass sie nicht verfügbar sind. Diese Funktion trägt dazu bei, die Anzahl der Kundenklicks zu reduzieren, die erforderlich sind, um die Produktverfügbarkeit zu bestimmen.

Die Funktion zur Musterbestandsverfügbarkeit kann für die Verwendung sowohl auf PDPs als auch auf Such- oder Kategorielistenseiten konfiguriert werden, auf denen Muster angezeigt werden. Um es zu aktivieren, müssen Sie die Eigenschaft **Medien bei Dimensionsauswahl aktualisieren** auf **Wahr** im [Mediengaleriemodul](../media-gallery-module.md) setzen. Diese Einstellung ermöglicht die Aktualisierung von Mediengaleriebildern, wenn Dimensionen ausgewählt werden. 

> [!IMPORTANT]
> Die Funktion zur Musterbestandsverfügbarkeit ist ab der Commerce-Version 10.0.21 verfügbar. Es erfordert, dass das Commerce-Modulbibliothekspaket in der Version 9.31 installiert ist.

Die folgende Abbildung zeigt ein Beispiel für die Bestandsinformationen auf den Größenmustern einer PDP.

![Beispiel für Bestandsinformationen auf den Größenmustern eines PDP](../dev-itpro/media/swatch_inventory.png)

## <a name="display-swatches-in-pos-and-other-channels"></a>Zeigen Sie Farbfelder am POS und in anderen Kanälen an

Commerce verfügt derzeit nicht über eine sofort einsatzbereite Implementierung, die die Anzeige von Mustern in Verkaufszellen (POS) und anderen Kanälen unterstützt. Sie können jedoch die Musteranzeigefunktion als Erweiterung implementieren, da Kanal-APIs die Hexadezimalcodes und Bild-URLs zurückgeben, zum Rendern von Mustern erforderlich sind.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Suchergebnismodul](../search-result-module.md)

[Wenden Sie die Website-Einstellungen für die Abmessungen an](../dimension-settings.md)

[Produktdimensionen](../../supply-chain/pim/product-dimensions.md)

[Bild hochladen](../dam-upload-images.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
