---
title: Karussellmodul
description: Dieses Thema behandelt Karussellmodule und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: cfbe254d225366f89779ffeef410bb0b1a29056e51a4719106e9bc495b898161
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6721054"
---
# <a name="carousel-module"></a>Karussellmodul

[!include [banner](includes/banner.md)]

Dieses Thema behandelt Karussellmodule und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.

Ein Karussellmodul wird verwendet, um mehrere Werbeartikel (einschließlich Rich-Bilder) in ein rotierenden Karussellbanner einzusetzen, den Debitoren durchsuchen können. So kann beispielsweise ein Einzelhänder ein Karussellmodul auf eine Startseite verwenden, um mehrere neue Produkte oder Promotionen zu veröffentlichen.

Sie können Inhaltsblockmodule innerhalb eines Karussellmoduls hinzufügen. Die Eigenschaften des Karussellmoduls definieren dann, wie diese Module angezeigt werden.

## <a name="examples-of-carousel-modules-in-e-commerce"></a>Beispiele für Containermodulen in E-Commerce

- Ein Karussell, das mehrere Promotionsmodule hat, kann auf einer Startseite verwendet werden.
- Ein Karussell, das mehrere Promotionsmodule hat, kann auf einer Produktetailseite verwendet werden.
- Ein Karussell kann auf einer beliebigen Marketings-Seite verwendet werden, um mehrere Aktionen oder Produkte zu bewerben.

Das folgende Bild zeigt ein Beispiel eines Karussellmoduls, das auf einer Homepage verwendet wird. Dieses Karussellmodul enthält mehrere Inhaltsblockelemente.

![Beispiel eines Karussell-Moduls.](./media/Hero.PNG)

## <a name="carousel-module-properties"></a>Karussellmoduleigenschaften

| Eigenschaftenname             | Wert                 | Beschreibung |
|---------------------------|-----------------------|-------------|
| Automatische Wiedergabe                  | **True** oder **False** | Wenn der Wert auf **Wahr** gesetzt wird, erfolgt der Übergangs zwischen Artikeln innerhalb des Karussells automatisch. Wenn der Wert auf **Falsch** gesetzt wird, erfolgt kein Übergang, es sei denn, der Debitor nutzt die Tastatur oder den Mauszeiger, um von einem Artikel zum nächsten Schritt zu gehen. |
| Folienübergangsintervall | Ein Wert in Sekunden    | Das Intervall für Übergänge zwischen Artikeln. |
| Übergangstyp           | **Anzeigen** oder **Ausblenden** | Der Übergangseffekt zwischen Elementen. |
| Karussellflipper ausblenden     | **True** oder **False** | Wenn der Wert auf **Wahr** gesetzt ist, sind der Karussellflipper und die Sequenzanzeige ausgeblendet. |
| Karussell ablehnen zulassen    | **True** oder **False** | Wenn der Wert auf **True** gesetzt wird, können Benutzer das Karussell ablehnen. |

## <a name="add-a-carousel-module-to-a-page"></a>Ein Karussellmodul einer neuen Seite hinzufügen

Um ein Karussellmodul einer neuen Seite hinzuzufügen und die erforderlichen Eigenschaften festzulegen, führen Sie die folgenden Schritte aus.

1. Wechseln Sie zu **Vorlagen** und wählen Sie **Neu** aus, um eine neue Vorlage zu erstellen.
1. Im Dialogfeld **Neue Vorlage** unter **Vorlagenname** geben Sie **Karussellvorlage** ein und wählen **OK**.
1. Fügen Sie im Slot **Text** das Modul **Standardseite** hinzu.
1. Wählen **Bearbeiten beenden**, um die Vorlage einzuchecken, und wählen Sie dann **Veröffentlichen**, um sie zu veröffentlichen.  
1. Verwenden Sie die Karoussellvorlage, die Sie soeben erstellt haben, um die Seite zu erstellen, die die Bezeichnung **Karussellseite** hat.
1. Im **Haupt-** Slot der neuen Seite fügen Sie ein Containermodul hinzu. 
1. Stellen Sie im rechten Bereich den Wert **Breite** auf **Bildschirm füllen** ein.
1. Fügen Sie unter **Seitengliederung** dem Karussellmodul ein Werbebanner-Modul hinzu.
1. Fügen Sie dem Karussellmodul ein Inhaltsblockmodul hinzu. Legen Sie die Eigenschaften des Inhaltsblockmoduls fest, indem Sie **Überschrift**, **Verknüpfung**, **Layout** und andere Eigenschaften bereitstellen.
1. Fügen Sie ein weiteres Inhaltsblockmodul hinzu und konfigurieren Sie es.
1. Legen Sie nach Bedarf weitere Eigenschaften für das Karussellmodul fest.
1. Wählen **Speichern** und dann **Vorschau** aus, um eine Vorschau der Seite anzuzeigen. Die Seite sollte ein Karussell anzeigen, das zwei Module darin hat (ein Heromodul und ein Funktionsmodul). Sie können zusätzliche Eigenschaften für das Karussell, den Hero und Funktionsmodule ändern, um den gewünschten Effekt zu erreichen.
1. Wählen **Bearbeiten beenden**, um die Seite einzuchecken, und wählen Sie dann **Veröffentlichen**, um sie zu veröffentlichen.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Übersicht über die Modulbibliothek](starter-kit-overview.md)

[Werbebannermodul](add-alert.md)

[Textblockmodul](add-content-rich-block.md)

[Inhaltsblockmodul](add-hero-module.md)

[Video-Player-Modul](add-video-player.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]