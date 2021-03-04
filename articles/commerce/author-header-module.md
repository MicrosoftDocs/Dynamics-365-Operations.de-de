---
title: Kopfzeilenmodul
description: In diesem Thema werden Kopfzeilenmodule behandelt und die Erstellung von Kopfzeilen in Microsoft Dynamics 365 Commerce beschrieben.
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
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
ms.dyn365.ops.version: ''
ms.openlocfilehash: 52069af5ca2211473d4a096ad850b5be1290bba1
ms.sourcegitcommit: eee3523be26369aecdb36c0143a6ee3dab4b7966
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "4412700"
---
# <a name="header-module"></a>Kopfzeilenmodul

[!include [banner](includes/banner.md)]

In diesem Thema werden Kopfzeilenmodule behandelt und die Erstellung von Kopfzeilen in Microsoft Dynamics 365 Commerce beschrieben.

## <a name="overview"></a>Übersicht

In Dynamics 365 Commerce wird eine Seitenkopfzeile als Seitenfragment konfiguriert, das die Module Kopfzeile, Werbebanner und Cookie-Zustimmung enthält. 

Das Kopfzeilenmodul enthält ein Site-Logo, Links zur Navigationshierarchie, Links zu anderen Seiten der Site, ein Warenkorbsymbolmodul, ein Wunschliste-Symbol, Anmeldeoptionen und die Suchleiste. Ein Kopfmodul wird automatisch für das Gerät optimiert, auf dem die Site angezeigt wird (anders ausgedrückt für ein Desktopgerät oder ein mobiles Gerät). Beispiel wird auf einem mobilen Gerät die Navigationsleiste in einer Schaltfläche **Menü** verringert (mitunter auch als *Hamburgermenü* bezeichnet).

Das folgende Bild zeigt ein Beispiel eines Kopfzeilenmoduls, das auf einer Startseite verwendet wird.

![Beispiel eines Kopfzeilenmoduls](./media/ecommerce-header.png)

## <a name="properties-of-a-header-module"></a>Eigenschaften eines Kopfmoduls

Ein Kopfmodul unterstützt die Eigenschaften **Logo-Bild**, **Logo-Link** und **Meine Kontolinks**. 

Die Eigenschaften **Logo-Bild** und **Logo-Link** werden verwendet, um ein Logo auf der Seite zu definieren. Weitere Informationen finden Sie in [Hinzufügen eines Logos](add-logo.md). 

Die Eigenschaft **Meine Kontolinks** kann verwendet werden, um Kontoseiten zu bestimmen, für die der Websitebesitzer Quicklinks in der Kopfzeile anzeigen möchte.

## <a name="modules-that-are-available-within-a-header-module"></a>Module, die in einem Kopfzeilenmodul verfügbar sind

Die folgenden Module können im Kopfzeilenmodul verwendet werden:

- **Navigationsmenü** – Das Navigationsmenü stellt die Kanalnavigationshierarchie und anderen statischen Navigationslinks dar. Weitere Informationen finden Sie unter [Navigationsmenümodul](nav-menu-module.md).

- **Suche** – Das Suchmodul ermöglicht es Benutzern, Suchbegriffe einzugeben, sodass sie nach Produkten suchen können. Die URL der Standardsuchseite und die Suchabfrageparameter müssen unter **Seiteneinstellungen \> Erweiterungen** angegeben werden. Das Suchmodul verfügt über Eigenschaften, mit denen Sie die Suchschaltfläche oder -Bezeichnung nach Bedarf unterdrücken können. Das Suchmodul unterstützt auch automatische Vorschlagsoptionen wie Produkt-, Keyword- und Kategoriesuchergebnisse.

- **Warenkorbsymbol** – Das Warenkorbsymbolmodul stellt das Warenkorbsymbol dar, das die Anzahl der Artikel im Warenkorb zu einem bestimmten Zeitpunkt anzeigt. Weitere Informationen finden Sie unter [Warenkorb-Symbolmodul](cart-icon-module.md).

- **Site-Selektor** – Mit dem Site-Auswahlmodul können Benutzer verschiedene vordefinierte Sites durchsuchen, basierend auf Markt, Regionen und Gebietsschemas. Weitere Informationen finden Sie unter [Site-Auswahl-Modul](site-selector.md).

- **Selektor speichern** – Das Store Selector-Modul kann in den Store Selector-Slot eines Header-Moduls aufgenommen werden. Hier können Benutzer Geschäfte in der Nähe durchsuchen und finden. Benutzer können auch einen bevorzugten Store angeben. Dieser Store wird dann in der Kopfzeile angezeigt. Wenn das Store-Selector-Modul im Header-Modul enthalten ist, wird die **Modus** Eigenschaft auf **Store finden** festgelegt. Weitere Informationen finden Sie unter [Store-Auswahl-Modul](store-selector.md).

> [!NOTE]
> - Hilfe für das Modul Warenkorbsymbol im Header-Modul finden Sie in Dynamics 365 Commerce Release 10.0.11.
> - Hilfe für das Modul Site-Selektor im Header-Modul finden Sie in Dynamics 365 Commerce Release 10.0.14.
> - Hilfe für das Modul Store-Selektor im Header-Modul finden Sie in Dynamics 365 Commerce Release 10.0.15.

## <a name="create-a-header-fragment-for-a-page"></a>Erstellen eines Kopfzeilenfragment für eine Seite

Um ein neues Kopfzeilenfragment zu erstellen, befolgen Sie diese Schritte.

1. Wechseln Sie zu **Fragmente** und wählen Sie **Neu** aus, um ein neues Fragment zu erstellen.
1. Wählen Sie im Dialogfeld **Neues Fragment** das Modul **Container** aus, geben Sie einen Namen für das Fragment ein und wählen Sie dann **OK** aus.
1. Wählen Sie den **Standardcontainer**-Slot aus und wählen Sie im Eigenschaftenfenster rechts die Eigenschaft **Breite** auf **Bildschirm ausfüllen**.
1. Wählen Sie im Slot **Standard-Container** die Ellipsen-Schaltfläche (**...**) und wählen Sie **Modul hinzufügen**.
1. Im Dialogfeld **Modul hinzufügen** wählen Sie die Module **Cookie-Zustimmung**, **Kopfzeile** und **Werbebanner** und dann **OK** aus.
1. Im Eigenschaftenbereich des **Werbebanner**-Moduls wählen Sie **Nachricht hinzufügen** und dann **Nachricht** aus.
1. Fügen Sie im Dialogfeld **Nachricht** dem Werbeinhalt Text und Links hinzu und wählen anschließend **OK** aus.
1. Im Eigenschaftenbereich des **Cookie-Zustimmung**-Moduls fügen Sie der Datenschutzseite der Website Text und einen Link hinzu und konfigurieren diese.
1. Im Slot **Navigationsmenü** wählen Sie das Kopfzeilenmodul, wählen die Ellipsen (**...**) und wählen **Modul hinzufügen**.
1. Im Dialogfeld **Modul hinzufügen** wählen Sie das Modul **Navigationsmenü** und wählen Sie dann **OK**.
1. Im Eigenschaftenbereich für das Navigationsmenümodul wählen Sie unter **Quelle für das Navigationsmenü** **Retail Server** aus.
1. Im Eigenschaftenbereich für das Navigationsmenümodul wählen Sie unter **Statische Menüpunkte** **Menüpunkt hinzufügen** und dann **Menüpunkt** aus. 
1. In dem **Menüpunkt**-Dialogfeld geben Sie unter **Menüelementtext** „Kontakt“ ein.
1. In dem **Menüpunkt**-Dialogfeld wählen Sie unter **Ziel des Menüelement-Links** **Link hinzufügen** aus.
1. Im Dialogfeld **Link hinzufügen** wählen Sie die URL für die „Kontakt“-Seite der Webite und dann **OK** aus.  
1. Wählen Sie im Dialogfeld **Menüelement** die Option **OK** aus.
1. Im Slot **Suchen** wählen Sie das Kopfzeilenmodul, wählen die Ellipsen (**...**) und wählen **Modul hinzufügen**.
1. Wählen Sie im Dialogfeld **Modul hinzufügen** das Modul **Suchen** und dann **OK** aus.
1. Konfigurieren Sie im Eigenschaftenbereich für das Suchmodul die Eigenschaften des Navigationsmenümoduls nach Bedarf.
1. Im Slot **Einkaufswagensymbol** wählen Sie das Kopfzeilenmodul, wählen die Ellipsen (**...**) und wählen **Modul hinzufügen**.
1. Wählen Sie im Dialogfeld **Modul hinzufügen** das Modul **Einkaufswagen**-Modul und dann **OK** aus.
1. Konfigurieren Sie im Eigenschaftenbereich für das Warenkorbsymbol-Modult die Eigenschaften nach Bedarf. Wenn das Warenkorbsymbol eine Warenkorbübersicht (auch als Minikorb bezeichnet) anzeigen soll, wenn Benutzer den Mauszeiger darüber halten, wählen Sie **Mini-Wagen anzeigen**.
1. Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um das Fragment einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.

Um Sicherzustellen, dass eine Kopfzeile auf jeder Seite angezeigt wird, führen Sie die folgenden Schritte für jede Seitenvorlage aus, die für die Site erstellt wird.

1. Im Slot **Kopfzeile** wählen Sie das Modul **Standardseite** und fügen das Fußzeilenfragment hinzu, das Sie erstellt haben.
1. Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um die Vorlage einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Übersicht über die Modulbibliothek](starter-kit-overview.md)

[Containermodul](add-container-module.md)

[Modul für Einkaufswagensymbol](cart-icon-module.md)

[Werbebannermodul](add-alert.md)

[Navigationsmenümodul](nav-menu-module.md) 

[Cookie-Einwilligung](cookie-consent-module.md)

[Fußzeilenmodul](author-footer-module.md)

[Siteauswahlmodul](site-selector.md)

[Shopauswahlmodul](store-selector.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]