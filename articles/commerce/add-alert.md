---
title: Werbebanner-Modul
description: Dieses Thema enthält Werbebanner-Module und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: da5e220e4578d1064eb7b627b441d3f585b3c095
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025619"
---
# <a name="promo-banner-module"></a>Werbebanner-Modul


[!include [banner](includes/banner.md)]

Dieses Thema enthält Werbebanner-Module und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.

## <a name="overview"></a>Übersicht

Werbebanner-Module werden verwendet, um Informationsmeldungen auf einer Seite anzeigen. Sie können verwendet werden, um Standort-weite Aktionen anzuzeigen, die auf allen Seiten einer E-Commerce-Webseite verwendet werden. 

Werbebanner-Modul unterstützen eine Textnachricht und einen Link. Wenn einem Werbebanner-Modul mehrere Nachrichten hinzugefügt werden, wird es zu einem rotierenden Karussell-Banner, mit dem Kunden alle Nachrichten durchlaufen können. 

Werbebanner-Module werden nach Daten des Content Management-System (CMS) gesteuert und können für jede beliebige Seite eingelagert werden.

## <a name="usage-examples-of-promo-banners-in-e-commerce"></a>Anwendungsbeispiele für Werbebanner im E-Commerce

Werbebanner können im Site-Header verwendet werden, um Site-weite Werbeaktionen oder Nachrichten anzuzeigen, wie in den folgenden Beispielen dargestellt.

„Jahresendverkauf endet in 10 Tagen“

„Mit den Aktionen zum Schulbeginn viel sparen. Jetzt shoppen.“

## <a name="promo-banner-module-properties"></a>Eigenschaften von Werbebanner-Modulen

| Eigenschaftenname             | Value                              | Beschreibung |
|---------------------------|------------------------------------|-------------|
| Bannernachrichten           | Text und Links                     | Eine Reihe von Texten und Links. |
| Automatische Wiedergabe                  | **True** oder **False**              | Ein Wert, der angibt, ob Nachrichten automatisch durchlaufen werden, wenn mehrere Nachrichten konfiguriert sind. |
| Folienübergangsintervall | Eine Anzahl von Millisekunden (ms)      | Das Intervall, in dem Nachrichten durchlaufen werden. |
| Ausblenden zulassen             | **True** oder **False**              | Wenn der Wert auf **True** gesetzt wird, können Debitoren die Warnung ablehnen. |
| Karussellflipper anzeigen     | **True** oder **False**              | Ein Wert, der angibt, ob die Karussellflipper angezeigt werden sollen, damit Debitoren mehrere Bannerelemente manuell durchlaufen können. |
| Textausrichtung            | **Rechts** **Links** **Zentriert** | Die Textausrichtung im Werbebanner-Modul. |
| Verknüpfung                      | Eine URL                              | Die URL für einen optionalen Link. |

## <a name="add-a-promo-banner-module-to-a-page"></a>Ein Werbebanner-Modul einer neuen Seite hinzufügen 

Um ein Werbebanner-Modul einer neuen Seite hinzuzufügen und die erforderlichen Eigenschaften festzulegen, führen Sie die folgenden Schritte aus.

1. Erstellen Sie eine Seitenvorlage mit dem Namen **Werbebanner-Vorlage**.
1. Unter **Seitengliederung** fügen Sie ein Modul **Standardseite** zum Slot **Text** hinzu. 
1. Überprüfen Sie in die Vorlage, und veröffentlichen Sie sie. 
1. Verwenden Sie die Vorlage, die Sie soeben erstellt haben, um die Seite zu erstellen, die die Bezeichnung **Werbebanner-Seite** hat. 
1. Im **Haupt-** Slot der neuen Seite fügen Sie ein Containermodul hinzu. 
1. Stellen Sie im rechten Bereich den Wert **Breite** auf **Behälter füllen** ein.
1. Fügen Sie unter **Seitengliederung** dem Containermodul ein Werbebanner-Modul hinzu.
1. Fügen Sie in den Einstellungen für das Banner-Modul eine oder mehrere Banner-Nachrichten hinzu. Jede Nachricht kann Text zusammen mit einem Link enthalten. Sie können die anderen Eigenschaften bearbeiten, um das Modul weiter anzupassen.
1. Seite speichern und Vorschau anzeigen. Am oberen Rand der Seite sollten Sie eine Warnung sehen, die den von Ihnen hinzugefügten Text anzeigt.
1. Beenden Sie die Bearbeitung der Seite und veröffentlichen Sie sie. 

> [!NOTE]
> Ein Werbebanner wird normalerweise im Seitenkopf- oder Untertitel-Slot verwendet.


## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Starterkit-Übersicht](starter-kit-overview.md)

[Karussellmodul](add-carousel.md)

[Textblock-Modul](add-content-rich-block.md)

[Inhaltsblockmodul](add-hero-module.md)

[Video-Player-Modul](add-video-player.md)
