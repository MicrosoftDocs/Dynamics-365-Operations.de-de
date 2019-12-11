---
title: Video-Player-Modul
description: Dieses Thema enthält Video-Player-Module und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: 32504351f712c83ba8f593c17d2e51c532374311
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785328"
---
# <a name="video-player-module"></a>Video-Player-Modul

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Dieses Thema enthält Video-Player-Module und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.

## <a name="overview"></a>Übersicht

Video-Player-Module werden verwendet, um Videowiedergabe zu unterstützen. Zwei Video-Player-Module werden im Shop-Starter-Kit bereitgestellt: das Ambient-Video-Player-Modul und das Video-Player-Modul. Beide Player unterstützen den Medientyp .mp4.

## <a name="ambient-video-player-module"></a>Hinzufügen eines Ambient-Video-Player-Moduls

Das Ambient-Video-Player-Modul unterstützt informatorische kurze Videos. Dieses sollte für Videos verwendet werden, die nicht länger als fünf Sekunden sind. Dieser Player unterstützt nur eingeschränkte Videoplaybackfunktionen, wie abspielen und Pause.

### <a name="examples-of-ambient-video-player-modules-in-e-commerce"></a>Beispiele für Ambient-Video-Player-Modulen im E-Commerce

- Kurze informatorische Videos, die neue Produkte auf der Startseite bekannt machen
- Kurze informatorische Videos, die Produktfunktionen auf einer Produktdetailseite markieren

### <a name="ambient-video-player-module-properties"></a>Hinzufügen einer Ambient-Video-Player-Moduleigenschaft

| Eigenschaftenname     | Wert                 | Beschreibung |
|-------------------|-----------------------|-------------|
| Automatische Wiedergabe          | **True** oder **False** | Wenn der Wert auf **Wahr** gesetzt wird, wird das Video automatisch wiedergegeben. |
| Stummschalten              | **True** oder **False** | Wenn der Wert auf **Wahr** gesetzt wird, wird der Ton abgeschaltet. Standardmäßig besitzt das Feld für diesen Player den Wert **True**. Im Google Chrome Browser wird automatische Wiedergabe standardmäßig stumm geschaltet, und die Audiowiedergabe wird nur abgespielt, wenn der Benutzer das Video manuell wiedergibt. |
| Schleife              | **True** oder **False** | Wenn der Wert auf **Wahr** gesetzt wird, wird das Video im Loop wiederholt. |
| Medien             |  Videodateipfad und Name | Die Videodatei, die vom Video-Player wiedergegeben wird. |
| Wiedergabesteuerelemente | **True** oder **False** | Wenn der Wert auf **Wahr** gesetzt wird, wird eine Wiedergabe-/Pausenschaltfläche im Video angezeigt. Wenn der Wert auf **Falsch** gesetzt wird, wird die Wiedergabel-/Pausenschaltfläche nicht angezeigt, doch Benutzer können das Videodatei anhalten und fortsetzen, indem sie die Tastatur verwenden. |

## <a name="video-player-module"></a>Video-Player-Modul

Das Video-Player-Modul kann verwendet werden, um Videos auf einer E-Commerce-Webseite zu zeigen. Es unterstützt alle Playbackfunktionen, wie Wiedergabe, Pause, Vollbildmodus und Untertitel. Das Video-Player-Modul unterstützt außerdem Anpassung von Untertiteln, um Microsoft-Barrierefreiheitsstandards zu entsprechen. So können Sie die Schriftgröße und die Hintergrundfarbe anpassen.

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
| Wiedergabesteuerelemente     | **True** oder **False**               | Wenn der Wert auf **Wahr** gesetzt wird, wird eine Wiedergabe-/Pausenschaltfläche im Video angezeigt. Wenn der Wert auf **Falsch** gesetzt wird, wird die Wiedergabel-/Pausenschaltfläche nicht angezeigt, doch Benutzer können das Videodatei anhalten und fortsetzen, indem sie die Tastatur verwenden. |
| Vollbildmodus       | **True** oder **False**               | Wenn der Wert auf **True** gesetzt wird, wird das Video im Vollbildmodus wiedergegeben. |
| Steuerungen              | **True** oder **False**               | Wenn der Wert auf **True** gesetzt wird, werden alle Steuerungen angezeigt. Zu diesen Steuerelementen gehören Spiel- und Pausenschaltflächen, ein Statusbalken und Untertitel. |
| Posterrahmen verbergen     | **True** oder **False**               | Ein Videodatei kann einen Plakatrahmen haben. Wenn der Wert dieser Eigenschaft auf **Wahr** festgelegt wurde, wird der Plakatrahmen ausgeblendet. |
| Maske festlegen            | Eine Nummer aus **0** bis **100** | Die Maske, die für die Videodatei für die Formatierung angewendet wird. |
| Vollbildschirmsymbol | **Quadrat** oder **Pfeil**             | Der Stil des Vollbildsymbols, das im Video-Player angezeigt wird. |

## <a name="add-a-video-player-module-to-a-page"></a>Hinzufügen eines Video-Player-Moduls zu einer Seite

Um ein Video-Player-Modul einer neuen Seite hinzuzufügen und die erforderlichen Eigenschaften festzulegen, führen Sie die folgenden Schritte aus.

1. Erstellen Sie eine Seitenvorlage, die mit **Video-Player-Vorlage** bezeichnet ist.
1. Im **Haupt-** Slot der Standardseite fügen Sie ein Containermodul hinzu.
1. Im Containermodul fügen Sie Video-Player- und Ambient Video-Player-Modul hinzu.
1. Überprüfen Sie in die Vorlage, und veröffentlichen Sie sie.
1. Verwenden Sie die Video Player Vorlage, die Sie soeben erstellt haben, um die Seite zu erstellen, die die Bezeichnung **Video Player Seite** hat.
1. Im **Haupt-** Slot der neuen Seite fügen Sie ein Ambient Video-Player-Modul hinzu.
1. In den Einstellungen für das Ambient Video-Player-Modul, gehen Sie zu **Medien** und laden eine Videodatei hoch. Sie können die Eigenschaften **Automatische Wiedergabe**, **Loop** und andere Eigenschaften ändern, wie Sie diese benötigen.
1. Seite speichern und Vorschau anzeigen.
1. Im **Haupt-** Slot der neuen Seite fügen Sie ein Ambient Video-Player-Modul hinzu.
1. In den Einstellungen für das Video-Player-Modul, gehen Sie zu **Medien** und laden eine Videodatei hoch.
1. Seite speichern und Vorschau anzeigen. Sie können beide Videomodule auf der Seite finden. Sie können zusätzliche Einstellungen ändern, um das Verhalten der einzelnen Module anzupassen.
1. Laden Sie die Seite hoch und veröffentlichen Sie sie.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Starterkit-Überblick](starter-kit-overview.md)

[Warnmmodul](add-alert.md)

[Karussellmodul](add-carousel.md)

[Umfangreiches Inhaltsblockmodul](add-content-rich-block.md)

[Inhaltsplatzierungsmodul](add-content-placement-modules.md)

[Funktionsmodul](add-feature-module.md)

[Hero-Modul](add-hero-module.md)
