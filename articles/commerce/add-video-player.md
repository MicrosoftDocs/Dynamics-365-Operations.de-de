---
title: Video-Player-Modul
description: Dieses Thema behandelt Video-Player-Module und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 48d7a047a739420fa4aaa3f520c774854f254ef9
ms.sourcegitcommit: 7e976059118938b0089e40bef948029a8c088b38
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "6479279"
---
# <a name="video-player-module"></a>Video-Player-Modul

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Dieses Thema behandelt Video-Player-Module und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.

Das Video-Player-Module wird verwendet, um die Videowiedergabe zu unterstützen. Es kann zu jeder Seite hinzugefügt werden, vorausgesetzt, der Videoinhalt wird in das Content Management System (CMS) hochgeladen und ist dort verfügbar. Das Video-Player-Modul unterstützt den Medientyp .mp4.

## <a name="video-player-module"></a>Video-Player-Modul

Das Video-Player-Modul kann verwendet werden, um Videos auf einer E-Commerce-Webseite zu zeigen. Es unterstützt alle Wiedergabefunktionen, wie Wiedergabe, Pause, Vollbildmodus, Audiobeschreibungen und Untertitel. Das Video-Player-Modul unterstützt außerdem Anpassung von Untertiteln, um Microsoft-Barrierefreiheitsstandards zu entsprechen. So können Sie die Schriftgröße und die Hintergrundfarbe anpassen.

Das Video-Player-Modul unterstützt auch sekundäre Audiospuren. Beim Hochladen eines Videos in das CMS kann auch eine sekundäre Audiospur hochgeladen werden. Das Video-Player-Modul kann dann die sekundäre Audiospur wiedergeben, wenn ein Benutzer sie auswählt.

### <a name="examples-of-video-player-modules-in-e-commerce"></a>Beispiele für Ambient-Video-Player-Module im E-Commerce

- Instruktionsvideos auf Produktdetailseiten oder Marketings-Seiten
- Werbespots oder Videos zu Richtlinien auf einer Marketings-Seite
- Marketings-Videos, die Produktfunktionen auf Produktdetailseiten oder Marketings-Seiten markieren

Das folgende Bild zeigt ein Beispiel eines Videoplayermoduls, das auf einer Homepage verwendet wird.

![Beispiel eines Video-Player-Moduls.](./media/ecommerce-videoplayer.PNG)

### <a name="video-player-module-properties"></a>Video-Player-Moduleigenschaften

| Eigenschaftenname         | Wert                               | Beschreibung |
|-----------------------|-------------------------------------|-------------|
| Überschrift               | Überschriftentext und Überschriftsmarkierung (**H1**, **H2**, **H3**, **H4**, **H5** oder **H6**) | Standardmäßig wird für die Überschrift die **H2**-Überschriftsmarkierung verwendet, aber die Markierung kann nach Bedarf geändert werden, um die Zugangsanforderungen zu erfüllen. |
| Rich Text             | Absatztext | Das Modul unterstützt Absatztext im Rich-Text-Format. Einige grundlegende Rich-Text-Funktionen werden unterstützt, wie Hyperlinks, fett und kursiv formatierte sowie unterstrichene Texte. Einige dieser Funktionen können vom Seitenthema überschrieben werden, das im Modul verwendet wird. |
| Verknüpfung                  | Link-Text, Link-URL, Accessible Rich Internet Applications-Beschriftung (ARIA) und Auswahl **Link in neuer Registerkarte öffnen** | Das Modul unterstützt mindestens einen oder mehrere „Handlungsaufruf“-Links. Wenn ein Link hinzugefügt wird, sind der Linktext, eine URL und eine ARIA-Beschriftung erforderlich. ARIA-Beschriftungen sollen beschreibend sein, um Barrierefreiheitsbedingungen zu erfüllen. Links können konfiguriert werden, sodass sie auf einer neuen Registerkarte geöffnet werden. |
| Untertext              | Überschrift, Text oder Links | Es kann zusätzlicher Kontext für das Video-Player-Modul hinzugefügt werden, z. B. ein Autoren- oder Designername oder Links zu persönlichen Blogs. |
| Automatische Wiedergabe             | **True** oder **False**               | Wenn der Wert auf **Wahr** gesetzt wird, wird das Video automatisch wiedergegeben. |
| Stummschalten                  | **True** oder **False**               | Wenn der Wert auf **Wahr** gesetzt wird, wird der Ton abgeschaltet. Standardmäßig besitzt das Feld für diesen Player den Wert **False**. Im Chrome Browser wird automatische Wiedergabe standardmäßig stumm geschaltet, und die Audiowiedergabe wird nur abgespielt, wenn der Benutzer das Video manuell wiedergibt. |
| Schleife                  | **True** oder **False**               | Wenn der Wert auf **Wahr** gesetzt wird, wird das Video im Loop wiederholt. |
| Medien                 | Videodateipfad und Name | Die Videodatei, die der Video-Player wiedergibt. |
| Vollbildmodus       | **True** oder **False**               | Wenn der Wert auf **True** gesetzt wird, wird das Video im Vollbildmodus wiedergegeben. |
| Trigger für Wiedergabe/Anhalten    | **True** oder **False**               | Wenn der Wert auf **Wahr** gesetzt wird, wird eine Wiedergabe-/Pausenschaltfläche im Video angezeigt. |
| Videoplayer-Steuerungen | **True** oder **False**               | Wenn der Wert auf **True** gesetzt wird, werden alle Steuerungen des Video-Players angezeigt. Zu diesen Steuerelementen gehören Wiedergabe- und Pausenschaltflächen, ein Fortschrittsbalken und Untertiteloptionen. |
| Posterbild ausblenden     | **True** oder **False**               | Ein Videodatei kann einen Plakatrahmen haben. Wenn der Wert dieser Eigenschaft auf **Wahr** festgelegt wurde, wird der Plakatrahmen ausgeblendet. |
| Maske festlegen            | Eine Nummer aus **0** bis **100** | Die Maske, die für die Videodatei für die Formatierung angewendet wird. |

> [!IMPORTANT]
> Die Eigenschaften **Überschrift**, **Rich-Text**, **Link** und **Untertext** stehen ab der Dynamics 365 Commerce-Version 10.0.20 zur Verfügung.

## <a name="add-a-video-player-module-to-a-page"></a>Hinzufügen eines Video-Player-Moduls zu einer Seite

> [!NOTE] 
> Bevor Sie ein Video-Player-Modul erstellen, müssen Sie zuerst ein Video in die Medienbibliothek hochladen.

Um ein Video-Player-Modul einer neuen Seite hinzuzufügen und die erforderlichen Eigenschaften festzulegen, führen Sie die folgenden Schritte aus.

1. Wechseln Sie zu **Vorlagen** und wählen Sie **Neu** aus, um eine neue Vorlage zu erstellen.
1. Im Dialogfeld **Neue Vorlage** unter **Vorlagenname** geben Sie **Videoplayer-Vorlage** ein und wählen **OK**.
1. Wählen Sie im Slot **Körper** die Ellipsen-Schaltfläche (**...**) und wählen Sie **Modul hinzufügen**.
1. Wählen Sie im Dialogfeld **Modul hinzufügen** das Modul **Standardseite** und dann **OK** aus.
1. Auf der **Standardseite** wählen Sie **Haupt**-Slot und wählen dann die Ellipsen (**...**) und wählen **Modul hinzufügen**.
1. Wählen Sie im Dialogfeld **Modul hinzufügen** wählen Sie das Modul **Container** und dann **OK** aus.
1. Wählen Sie im Slot **Container** die Ellipsen-Schaltfläche (**...**) und wählen Sie **Modul hinzufügen**.
1. Wählen Sie im Dialogfeld **Modul hinzufügen** das Modul **Videoplayer** und dann **OK** aus.
1. Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um die Vorlage einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen. 
1. Wechseln Sie zu **Seiten**, und wählen Sie dann **Neu** aus, um eine neue Seite zu erstellen.
1. In dem Dialogfeld **Wählen Sie eine Vorlage** wählen Sie die von Ihnen erstellte Video-Player-Vorlage aus. Unter **Seitenname** geben Sie **Video-Player-Seite** ein und wählen dann **OK**.
1. Auf der neuen Seite wählen Sie **Haupt**-Slot und wählen dann die Ellipsen (**...**) und wählen **Modul hinzufügen**.
1. Wählen Sie im Dialogfeld **Modul hinzufügen** wählen Sie das Modul **Container** und dann **OK** aus.
1. Wählen Sie im Slot **Container** die Ellipsen-Schaltfläche (**...**) und wählen Sie **Modul hinzufügen**.
1. Wählen Sie im Dialogfeld **Modul hinzufügen** das Modul **Videoplayer** und dann **OK** aus.
1. Wählen Sie im Eigenschaftenfenster des Videoplayer-Moduls **Video hinzufügen** aus.
1. Wählen Sie im Dialogfeld **Medienauswahl** ein Video und anschließend **Neues Medienelement hochladen** aus.
1. Wählen Sie im Datei-Explorer eine oder mehrere Video-Dateien aus und wählen Sie dann **Öffnen**.
1. In dem Dialogfeld **Medienelement hochladen** geben Sie nach Bedarf einen Titel und andere Informationen ein und wählen Sie dann aus **OK**.
1. In dem **Medienauswahl** Dialogfeld wählen Sie **Schließen**.
1. Wählen **Speichern** und dann **Vorschau** aus, um eine Vorschau der Seite anzuzeigen. Sie sollten das Videomodul auf der Seite sehen. Sie können zusätzliche Einstellungen ändern, um das Verhalten des Moduls anzupassen.
1. Wählen **Bearbeiten beenden**, um die Seite einzuchecken, und wählen Sie dann **Veröffentlichen**, um sie zu veröffentlichen. 

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Übersicht über die Modulbibliothek](starter-kit-overview.md)

[Werbebannermodul](add-alert.md)

[Karussellmodul](add-carousel.md)

[Textblockmodul](add-content-rich-block.md)

[Inhaltsblockmodul](add-hero-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
