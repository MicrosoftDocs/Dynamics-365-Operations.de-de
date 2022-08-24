---
title: Mediengaleriemodul
description: Dieser Artikel befasst sich mit Mediengaleriemodulen und beschreibt, wie diese Seiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 5e2d0a4422341badee906c71bebdd491e18a38cc
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273457"
---
# <a name="media-gallery-module"></a>Mediengaleriemodul

[!include [banner](includes/banner.md)]

Dieser Artikel befasst sich mit Mediengaleriemodulen und beschreibt, wie diese Seiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.

Mediengaleriemodule zeigen ein oder mehrere Bilder in einer Katalogansicht. Mediengaleriemodule unterstützen Miniaturansichten, die horizontal (als Zeile unter dem Bild) oder vertikal angeordnet werden (als Spalte neben dem Bild). Mediengaleriemodule bieten auch Funktionen, mit denen Bilder gezoomt (vergrößert) oder im Vollbildmodus angezeigt werden können. Um in einem Mediengaleriemodul gerendert zu werden, muss ein Bild in der Medienbibliothek des Commerce Site Builder verfügbar sein. Derzeit unterstützen Mediengaleriemodule nur Bilder.

Im Standardmodus verwendet ein Mediengaleriemodul zum Rendern der entsprechenden Produktbilder die Produkt-ID, die im Seitenkontext einer Produktdetailseite (PDP) verfügbar ist. Im Commerce Headquarters muss für alle Produkte ein Mediendateipfad festgelegt werden. Die Bilder sollten dann gemäß dem Dateipfad, der für die Produkte im Commerce Headquarters festgelegt wurde, in die Site-Builder-Medienbibliothek hochgeladen werden. Zu diesen Bildern gehören Bilder für Produkte und alle Produktvarianten. Weitere Informationen zum Hochladen von Bildern in die Site-Builder-Medienbibliothek finden Sie unter [Bilder hochladen](dam-upload-images.md).

Alternativ kann ein Mediengaleriemodul einen vollständig kuratierten Bildersatz auf einer Bildergalerieseite hosten. In diesem Fall bestehen keine Abhängigkeiten von der Produkt-ID oder dem Seitenkontext. In diesem Fall müssen Bilder in die Medienbibliothek des Site Builders hochgeladen und dort spezifiziert werden.

Hier sind einige Anwendungsbeispiele für Mediengaleriemodule:

- Rendern von Produktbildern auf einer PDP
- Rendern von Produktbildern auf einer Produktmarketingseite
- Anzeigen eines kuratierten Bildersatzes auf einer Marketingseite, z. B. einer Galerieseite

In dem Beispiel der folgenden Abbildung werden in einem Kauffeld auf einer PDP Produktbilder mithilfe eines Mediengaleriemoduls gehostet.

![Beispiel für ein Kauffeld auf einer Produktdetailseite, auf der Produktbilder mithilfe eines Mediengaleriemoduls gehostet werden.](./media/ecommerce-pdp-buybox.PNG)

## <a name="media-gallery-properties"></a>Eigenschaften der Mediengalerie

| Eigenschaftenname | Werte | Beschreibung |
|---------------|--------|-------------|
| Bildquelle | **Seitenkontext** oder **Produkt ID** | Der Standardwert ist **Seitenkontext**. Wenn **Seitenkontext** ausgewählt ist, erwartet das Modul, dass die Seite die Produkt-ID bereitstellt. Wenn **Produkt ID** ausgewählt ist, muss die Produkt-ID für ein Bild als Wert für die **Produkt ID**-Eigenschaft angegeben werden. Diese Funktion steht in der Commerce-Version 10.0.12 zur Verfügung. |
| Produktkennung | Produkt-ID | Diese Eigenschaft gilt nur, wenn der Wert der Eigenschaft **Bildquelle** ist **Produkt-ID**. |
| Bildvergrößerung | **Inline** oder **Container** | Mit dieser Eigenschaft kann der Benutzer Bilder im Mediengaleriemodul zoomen. Ein Bild kann entweder inline oder in einem separaten Container neben dem Bild gezoomt werden. Diese Funktionalität ist in 10.0.12 verfügbar. |
| Vergrößerungsfaktor | Eine Dezimalzahl | Diese Eigenschaft gibt den Skalierungsfaktor für das Zoomen von Bildern an. Wenn zum Beispiel der Wert auf **2,5** gesetzt ist, werden Bilder um das 2,5-Fache vergrößert. |
| Vollbild | **True** oder **False** | Diese Eigenschaft gibt an, ob Bilder im Vollbildmodus angezeigt werden können. Im Vollbildmodus können Bilder auch weiter vergrößert werden, wenn die Funktionalität des Zooms eingeschaltet ist. Diese Funktionalität ist in der Commerce-Version 10.0.13 verfügbar. |
| Gezoomte Bildqualität | Eine Zahl von 1 bis 100, die einen Prozentsatz darstellt und die mit einem Steuerelement ausgewählt wird | Diese Eigenschaft definiert die Bildqualität für vergrößerte Bilder. Es kann auf 100 Prozent festgelegt werden, um sicherzustellen, dass ein gezoomtes Bild immer die höchstmögliche Auflösung verwendet. Diese Eigenschaft ist nicht auf PNG-Dateien anwendbar, da diese ein verlustfreies Format verwenden. Diese Funktionalität ist ab der Commerce-Version 10.0.19 verfügbar. |
| Bilder | Bilder, die aus der Site-Builder-Medienbibliothek ausgewählt wurden | Bilder können nicht nur aus einem Produkt gerendert, sondern auch für ein Mediengaleriemodul kuratiert werden. Diese Bilder werden an alle verfügbaren Produktbilder angehängt. Diese Funktion steht in der Commerce-Version 10.0.12 zur Verfügung. |
| Ausrichtung der Miniaturansicht | **Vertikal** oder **horizontal** | Diese Eigenschaft gibt an, ob Miniaturansichten in einem vertikalen oder horizontalen Streifen angezeigt werden sollen. |
| Master-Produktbilder für Variante ausblenden | **True** oder **False** | Wenn diese Eigenschaft auf **True** festgelegt ist, werden bei Auswahl einer Variante die Bilder des Masterprodukts ausgeblendet, es sei denn, die Variante hat keine Bilder. Diese Eigenschaft wirkt sich nicht auf Produkte aus, die keine Varianten haben. |
| Medien bei Dimensionsauswahl aktualisieren | **True** oder **False** | Wenn diese Eigenschaft auf **Wahr** gesetzt ist, werden Bilder in der Medienbibliothek aktualisiert, wenn irgendeine Dimension (wie Farbe, Stil oder Größe) ausgewählt wird und ein Bild verfügbar ist. Diese Eigenschaft trägt dazu bei, das Browsing-Erlebnis zu vereinfachen, da nicht jede Produktvariantendimension ausgewählt werden muss, damit das entsprechende Bild aktualisiert wird. Diese Eigenschaft ist auf der Registerkarte **Erweitert** verfügbar. |

> [!IMPORTANT]
> Die Eigenschaft **Medien bei Dimensionsauswahl aktualisieren** ist ab dem Release der Commerce-Version 10.0.21 verfügbar. Es erfordert, dass das Commerce-Modulbibliothekspaket in der Version 9.31 installiert ist.

Die folgende Abbildung zeigt ein Beispiel eines Mediengaleriemoduls, in dem die Vollbild- und Zoomoptionen verfügbar sind.

![Beispiel eines Mediengaleriemoduls, in dem die Vollbild- und Zoomoptionen verfügbar sind.](./media/ecommerce-media-zoom.png)

Die folgende Abbildung zeigt ein Beispiel eines Mediengaleriemoduls mit kuratierten Bildern (d. h. die angegebenen Bilder hängen nicht von der Produkt-ID oder dem Seitenkontext ab).

![Beispiel eines Mediengaleriemoduls mit kuratierten Bildern.](./media/ecommerce-media-curated.PNG)

## <a name="commerce-scale-unit-interaction"></a>Commerce Scale Unit-Interaktion

Wenn die Bildquelle aus dem Seitenkontext abgeleitet wird, wird die Produkt-ID von der PDP zum Abrufen der Bilder verwendet. Das Mediengaleriemodul ruft Bilddateipfade für Produkte mithilfe der Commerce Scale Unit-Anwendungsprogrammschnittstellen (APIs) ab. Die Bilder werden dann aus der Medienbibliothek abgerufen, damit sie im Modul gerendert werden können.

## <a name="add-a-media-gallery-module-to-a-page"></a>Hinzufügen eines Mediengaleriemoduls zu einer Seite

Gehen Sie folgendermaßen vor, um ein Mediengaleriemodul einer Marketingseite hinzuzufügen.

1. Wechseln Sie zu **Vorlagen** und wählen Sie **Neu** aus, um eine neue Vorlage zu erstellen.
1. Im Dialogfeld **Neue Vorlage** geben Sie unter **Vorlagenname** **Containervorlage** ein und wählen Sie **OK**.
1. Markieren Sie im Slot **Hauptteil** die Auslassungspunkte (**...**) und wählen Sie dann **Modul hinzufügen**.
1. Wählen Sie im Dialogfeld **Modul auswählen** das Modul **Standardseite** und dann **OK** aus.
1. Auf der Standardseite wählen Sie **Haupt**-Slot und dann die Ellipsen (**...**) und **Modul hinzufügen**.
1. Wählen Sie im Dialogfeld **Module auswählen** das Modul **Container** und dann **OK** aus.
1. Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um die Vorlage einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.
1. Wechseln Sie zu **Seiten**, und wählen Sie dann **Neu** aus, um eine neue Seite zu erstellen.
1. In der Dialogbox **Eine neue Seite erstellen** geben Sie unter **Seitenname** **Medienkatalog Seite** ein und wählen Sie dann **Weiter**.
1. Unter **Vorlage auswählen** wähle Sie die **Marketing-Vorlage** aus, die Sie erstellt haben, und Sie wählen dann **Weiter**.
1. Wählen Sie unter **Wählen Sie ein Layout** ein Seitenlayout (z.B. **Flexibles Layout**) und wählen Sie dann **Weiter**.
1. Unter **Prüfen und beenden** überprüfen Sie die Konfiguration der Seite. Wenn Sie die Seiteninformationen bearbeiten müssen, wählen Sie **Zurück**. Wenn die Seiteninformationen korrekt sind, wählen Sie **Seite erstellen**. 
1. Auf der neuen Seite wählen Sie **Haupt**-Slot und wählen dann die Ellipsen (**...**) und wählen **Modul hinzufügen**.
1. Wählen Sie im Dialogfeld **Module auswählen** das Modul **Container** und dann **OK** aus.
1. Wählen Sie im Slot **Container** die Ellipsen-Schaltfläche (**...**) und wählen Sie **Modul hinzufügen**.
1. Wählen Sie im Dialogfeld **Module auswählen** das Modul **Mediengallerie** und dann **OK** aus.
1. Im Eigenschaftenbereich für das Mediengaleriemodul wählen Sie unter **Bildquelle** **Produkt ID**. Geben Sie dann in das Feld **Produkt-ID** eine Produkt-ID ein.
1. Wählen **Speichern** und dann **Vorschau** aus, um eine Vorschau der Seite anzuzeigen. Sie sollten die Bilder für das Produkt in einer Galerieansicht sehen können.
1. Um nur kuratierte Bilder im Eigenschaftenbereich zu verwenden, wählen Sie unter **Bildquelle** **Produkt ID**. Dann wählen Sie unter **Bilder** so oft wie nötig **Ein Bild hinzufügen**, um Bilder aus der Medienbibliothek hinzuzufügen.
1. Legen Sie alle zusätzlichen Eigenschaften fest, die Sie festlegen möchten, z. B. **Bildzoom**, **Zoomfaktor** und **Ausrichtung der Miniaturansichten**.
1. Wenn Sie fertig sind, wählen Sie **Speichern** und dann **Bearbeiten beenden**, um die Seite einzuchecken, und wählen Sie dann **Veröffentlichen**.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Übersicht über die Modulbibliothek](starter-kit-overview.md)

[Kauffeldmodul](add-buy-box.md)

[Containermodul](add-container-module.md)

[Bilder hochladen](dam-upload-images.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
