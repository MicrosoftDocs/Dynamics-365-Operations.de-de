---
title: Karussellmodul
description: Dieses Thema enthält Karusellmodule und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 35aaf35419a8c5b83b2a3e1136a02200bf347c6b
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411295"
---
# <a name="carousel-module"></a>Karussellmodul

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Dieses Thema enthält Karusellmodule und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.

## <a name="overview"></a>Übersicht

Ein Karussellmodul wird verwendet, um mehrere Werbeartikel (einschließlich Rich-Bilder) in ein rotierenden Karussellbanner einzusetzen, den Debitoren durchsuchen können. So kann beispielsweise ein Einzelhänder ein Karussellmodul auf eine Startseite verwenden, um mehrere neue Produkte oder Promotionen zu veröffentlichen.

Sie können Inhaltsblockmodule innerhalb eines Karussellmoduls hinzufügen. Die Eigenschaften des Karussellmoduls definieren dann, wie diese Module angezeigt werden.

## <a name="examples-of-carousel-modules-in-e-commerce"></a>Beispiele für Containermodulen in E-Commerce

- Ein Karussell, das mehrere Promotionsmodule hat, kann auf einer Startseite verwendet werden.
- Ein Karussell, das mehrere Promotionsmodule hat, kann auf einer Produktetailseite verwendet werden.
- Ein Karussell kann auf einer beliebigen Marketings-Seite verwendet werden, um mehrere Aktionen oder Produkte zu bewerben.

Das folgende Bild zeigt ein Beispiel eines Karussellmoduls, das auf einer Homepage verwendet wird. Dieses Karussellmodul enthält mehrere Inhaltsblockelemente.

![Beispiel eines Karussell-Moduls](./media/Hero.PNG)

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

[Starterkit-Übersicht](starter-kit-overview.md)

[Werbebannermodul](add-alert.md)

[Textblock-Modul](add-content-rich-block.md)

[Inhaltsblockmodul](add-hero-module.md)

[Video-Player-Modul](add-video-player.md)
