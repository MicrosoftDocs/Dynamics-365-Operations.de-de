---
title: Video-Player-Modul
description: Dieses Thema enthält Video-Player-Module und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e94658eed12b12d6666e63d2c06b86646c81a120
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025646"
---
# <a name="video-player-module"></a>Video-Player-Modul


[!include [banner](includes/banner.md)]

Dieses Thema enthält Video-Player-Module und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.

## <a name="overview"></a>Übersicht

Das Video-Player-Module wird verwendet, um die Videowiedergabe zu unterstützen. Es kann zu jeder Seite hinzugefügt werden, vorausgesetzt, der Videoinhalt wird in das Content Management System (CMS) hochgeladen und ist dort verfügbar. Das Video-Player-Modul unterstützt den Medientyp .mp4.

## <a name="video-player-module"></a>Video-Player-Modul

Das Video-Player-Modul kann verwendet werden, um Videos auf einer E-Commerce-Webseite zu zeigen. Es unterstützt alle Wiedergabefunktionen, wie Wiedergabe, Pause, Vollbildmodus, Audiobeschreibungen und Untertitel. Das Video-Player-Modul unterstützt außerdem Anpassung von Untertiteln, um Microsoft-Barrierefreiheitsstandards zu entsprechen. So können Sie die Schriftgröße und die Hintergrundfarbe anpassen.

Das Video-Player-Modul unterstützt auch sekundäre Audiospuren. Beim Hochladen eines Videos in das CMS kann auch eine sekundäre Audiospur hochgeladen werden. Das Video-Player-Modul kann dann die sekundäre Audiospur wiedergeben, wenn ein Benutzer sie auswählt.

### <a name="examples-of-video-player-modules-in-e-commerce"></a>Beispiele für Ambient-Video-Player-Module im E-Commerce

- Instruktionsvideos auf Produktdetailseiten oder Marketings-Seiten
- Werbespots oder Videos zu Richtlinien auf einer Marketings-Seite
- Marketings-Videos, die Produktfunktionen auf Produktdetailseiten oder Marketings-Seiten markieren

### <a name="video-player-module-properties"></a>Video-Player-Moduleigenschaften

| Eigenschaftenname         | Wert                               | Beschreibung |
|-----------------------|-------------------------------------|-------------|
| Automatische Wiedergabe             | **True** oder **False**               | Wenn der Wert auf **Wahr** gesetzt wird, wird das Video automatisch wiedergegeben. |
| Stummschalten                  | **True** oder **False**               | Wenn der Wert auf **Wahr** gesetzt wird, wird der Ton abgeschaltet. Standardmäßig besitzt das Feld für diesen Player den Wert **False**. Im Chrome Browser wird automatische Wiedergabe standardmäßig stumm geschaltet, und die Audiowiedergabe wird nur abgespielt, wenn der Benutzer das Video manuell wiedergibt. |
| Schleife                  | **True** oder **False**               | Wenn der Wert auf **Wahr** gesetzt wird, wird das Video im Loop wiederholt. |
| Medien                 | Videodateipfad und Name | Die Videodatei, die der Video-Player wiedergibt. |
| Vollbildmodus       | **True** oder **False**               | Wenn der Wert auf **True** gesetzt wird, wird das Video im Vollbildmodus wiedergegeben. |
| Trigger für Wiedergabe/Anhalten    | **True** oder **False**               | Wenn der Wert auf **Wahr** gesetzt wird, wird eine Wiedergabe-/Pausenschaltfläche im Video angezeigt. |
| Videoplayer-Steuerungen | **True** oder **False**               | Wenn der Wert auf **True** gesetzt wird, werden alle Steuerungen des Video-Players angezeigt. Zu diesen Steuerelementen gehören Wiedergabe- und Pausenschaltflächen, ein Fortschrittsbalken und Untertiteloptionen. |
| Posterbild ausblenden     | **True** oder **False**               | Ein Videodatei kann einen Plakatrahmen haben. Wenn der Wert dieser Eigenschaft auf **Wahr** festgelegt wurde, wird der Plakatrahmen ausgeblendet. |
| Maske festlegen            | Eine Nummer aus **0** bis **100** | Die Maske, die für die Videodatei für die Formatierung angewendet wird. |

## <a name="add-a-video-player-module-to-a-page"></a>Hinzufügen eines Video-Player-Moduls zu einer Seite

> [!NOTE] 
> Bevor Sie ein Video-Player-Modul erstellen, müssen Sie zuerst ein Video in die Medienbibliothek hochladen.

Um ein Video-Player-Modul einer neuen Seite hinzuzufügen und die erforderlichen Eigenschaften festzulegen, führen Sie die folgenden Schritte aus.

1. Erstellen Sie eine Seitenvorlage, die mit **Video-Player-Vorlage** bezeichnet ist.
1. Im **Haupt-** Slot der Standardseite fügen Sie ein Containermodul hinzu.
1. Im Containermodul fügen Sie Video-Player- und Ambient Video-Player-Modul hinzu.
1. Beenden Sie die Bearbeitung der Vorlage und veröffentlichen Sie sie.
1. Verwenden Sie die Video-Player-Vorlage, die Sie soeben erstellt haben, um die Seite zu erstellen, die die Bezeichnung **Video-Player-Seite** hat.
1. Im **Haupt-** Slot der neuen Seite fügen Sie ein Ambient Video-Player-Modul hinzu.
1. Wählen Sie im Eigenschaftenfenster für das Videoplayer-Modul **Video hinzufügen** aus.
1. Wählen Sie im Dialogfeld **Medienauswahl** ein Video und anschließend **Neues Medienelement hochladen** aus.
1. Seite speichern und Vorschau anzeigen. Sie sollten das Videomodul auf der Seite sehen. Sie können zusätzliche Einstellungen ändern, um das Verhalten des Moduls anzupassen.
1. Beenden Sie die Bearbeitung der Seite und veröffentlichen Sie sie.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Starterkit-Übersicht](starter-kit-overview.md)

[Werbebanner-Modul](add-alert.md)

[Karussellmodul](add-carousel.md)

[Textblock-Modul](add-content-rich-block.md)

[Inhaltsblockmodul](add-hero-module.md)
