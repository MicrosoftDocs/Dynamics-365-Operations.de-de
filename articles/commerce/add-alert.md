---
title: Werbebanner-Modul
description: Dieses Thema behandelt Werbebanner-Module und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
ms.date: 07/08/2021
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
ms.openlocfilehash: f781ed22852cb2108850e7dc6762aa6a9ba0db97574cb0dcc7959f8926e47a08
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6718779"
---
# <a name="promo-banner-module"></a>Werbebannermodul

[!include [banner](includes/banner.md)]

Dieses Thema behandelt Werbebanner-Module und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.

Werbebanner-Module werden verwendet, um Informationsmeldungen auf einer Seite anzeigen. Sie können verwendet werden, um Standort-weite Aktionen anzuzeigen, die auf allen Seiten einer E-Commerce-Webseite verwendet werden. 

Werbebanner-Modul unterstützen eine Textnachricht und einen Link. Wenn einem Werbebanner-Modul mehrere Nachrichten hinzugefügt werden, wird es zu einem rotierenden Karussell-Banner, mit dem Kunden alle Nachrichten durchlaufen können. 

Werbebanner-Module werden nach Daten des Content Management-System (CMS) gesteuert und können für jede beliebige Seite eingelagert werden.

## <a name="usage-examples-of-promo-banners-in-e-commerce"></a>Anwendungsbeispiele für Werbebanner im E-Commerce

Werbebanner können im Site-Header verwendet werden, um Site-weite Werbeaktionen oder Nachrichten anzuzeigen, wie in den folgenden Beispielen dargestellt.

„Jahresendverkauf endet in 10 Tagen“

„Mit den Aktionen zum Schulbeginn viel sparen. Jetzt shoppen.“

Für Thanksgiving SALE! shoppen 

Das folgende Bild zeigt ein Beispiel für eine Werbeanzeige.

![Beispiel eines Werbeanzeigenmoduls.](./media/ecommerce-Promobanner.PNG)

## <a name="promo-banner-module-properties"></a>Eigenschaften von Werbebanner-Modulen

| Eigenschaftenname             | Wert                              | Beschreibung |
|---------------------------|------------------------------------|-------------|
| Bannernachrichten           | Text und Links                     | Eine Reihe von Texten und Links. |
| Automatische Wiedergabe                  | **True** oder **False**              | Ein Wert, der angibt, ob Nachrichten automatisch durchlaufen werden, wenn mehrere Nachrichten konfiguriert sind. |
| Folienübergangsintervall | Eine Anzahl von Millisekunden (ms)      | Das Intervall, in dem Nachrichten durchlaufen werden. |
| Ausblenden zulassen             | **True** oder **False**              | Wenn der Wert auf **True** gesetzt wird, können Debitoren die Warnung ablehnen. |
| Karussellflipper anzeigen     | **True** oder **False**              | Ein Wert, der angibt, ob die Karussellflipper angezeigt werden sollen, damit Debitoren mehrere Bannerelemente manuell durchlaufen können. |
| Textausrichtung            | **Rechts** **Links** **Zentriert** | Die Textausrichtung im Werbebanner-Modul. |
| Verknüpfen                      | Eine URL                              | Die URL für einen optionalen Link. |
|Textausrichtung             | **Rechts** **Links** **Zentriert** | Diese Eigenschaft ist als Designerweiterung im Adventure Works-Design verfügbar. Es erlaubt einem Benutzer, die Textausrichtung in der Werbeanzeige festzulegen. |

> [!IMPORTANT]
> Das Adventure Works-Design steht ab der Dynamics 365 Commerce-Version 10.0.20 zur Verfügung.

## <a name="add-a-promo-banner-module-to-a-page"></a>Ein Werbebanner-Modul einer neuen Seite hinzufügen 

Um ein Werbebanner-Modul einer neuen Seite hinzuzufügen und die erforderlichen Eigenschaften festzulegen, führen Sie die folgenden Schritte aus.

1. Wechseln Sie zu **Vorlagen** und wählen Sie **Neu** aus, um eine neue Vorlage zu erstellen.
1. Im Dialogfeld **Neue Vorlage** unter **Vorlagenname** geben Sie **Werbebanner-Vorlage** ein und wählen **OK**.
1. Unter **Seitengliederung** fügen Sie ein Modul **Standardseite** zum Slot **Text** hinzu. 
1. Wählen **Bearbeiten beenden**, um die Vorlage einzuchecken, und wählen Sie dann **Veröffentlichen**, um sie zu veröffentlichen. 
1. Verwenden Sie die Vorlage, die Sie soeben erstellt haben, um die Seite zu erstellen, die die Bezeichnung **Werbebanner-Seite** hat. 
1. Im **Haupt-** Slot der neuen Seite fügen Sie ein Containermodul hinzu. 
1. Stellen Sie im rechten Bereich den Wert **Breite** auf **Behälter füllen** ein.
1. Fügen Sie unter **Seitengliederung** dem Containermodul ein Werbebanner-Modul hinzu.
1. Fügen Sie in den Einstellungen für das Banner-Modul eine oder mehrere Banner-Nachrichten hinzu. Jede Nachricht kann Text zusammen mit einem Link enthalten. Sie können die anderen Eigenschaften bearbeiten, um das Modul weiter anzupassen.
1. Wählen **Speichern** und dann **Vorschau** aus, um eine Vorschau der Seite anzuzeigen. Am oberen Rand der Seite sollten Sie eine Warnung sehen, die den von Ihnen hinzugefügten Text anzeigt.
1. Wählen **Bearbeiten beenden**, um die Seite einzuchecken, und wählen Sie dann **Veröffentlichen**, um sie zu veröffentlichen.

> [!NOTE]
> Ein Werbebanner wird normalerweise im Seitenkopf- oder Untertitel-Slot verwendet.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Übersicht über die Modulbibliothek](starter-kit-overview.md)

[Karussellmodul](add-carousel.md)

[Textblockmodul](add-content-rich-block.md)

[Inhaltsblockmodul](add-hero-module.md)

[Video-Player-Modul](add-video-player.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
