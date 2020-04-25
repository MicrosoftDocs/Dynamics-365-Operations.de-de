---
title: Kopfzeilenmodul
description: In diesem Thema werden Kopfzeilenmodule behandelt und die Erstellung von Kopfzeilen in Microsoft Dynamics 365 Commerce beschrieben.
author: anupamar
manager: annbe
ms.date: 04/13/2020
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
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: cec138ebefbd2beb2f1cf6302ce58d8bbc5c4bbd
ms.sourcegitcommit: ac966ea3a6c557fb5f9634b187b0e788d3e82d4d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261443"
---
# <a name="header-module"></a>Kopfzeilenmodul


[!include [banner](includes/banner.md)]

In diesem Thema werden Kopfzeilenmodule behandelt und die Erstellung von Kopfzeilen in Microsoft Dynamics 365 Commerce beschrieben.

## <a name="overview"></a>Übersicht

Im Dynamics 365 Commerce umfasst ein Seitenkopf mehrere Module, z. B. die Module Kopfzeile, Navigationsmenü, Suche, Werbebanner und Cookie-Einwilligung. 

Das Kopfzeilenmodul enthält ein Site-Logo, Links zur Navigationshierarchie, Links zu anderen Seiten der Site, ein Warenkorbsymbol, ein Wunschliste-Symbol, Anmeldeoptionen und die Suchleiste. Ein Kopfmodul wird automatisch für das Gerät optimiert, auf dem die Site angezeigt wird (anders ausgedrückt für ein Desktopgerät oder ein mobiles Gerät). Beispiel wird auf einem mobilen Gerät die Navigationsleiste in einer Schaltfläche **Menü** verringert (mitunter auch als *Hamburgermenü* bezeichnet).

## <a name="properties-of-a-header-module"></a>Eigenschaften eines Kopfmoduls

Ein Kopfmodul unterstützt die Eigenschaften **Logo-Bild**, **Logo-Link** und **Meine Kontolinks**. 

Die Eigenschaften **Logo-Bild** und **Logo-Link** werden verwendet, um ein Logo auf der Seite zu definieren. Weitere Informationen finden Sie in [Hinzufügen eines Logos](add-logo.md). 

Die Eigenschaft **Meine Kontolinks** kann verwendet werden, um Kontoseiten zu bestimmen, für die der Websitebesitzer Quicklinks in der Kopfzeile anzeigen möchte.

## <a name="modules-that-are-available-in-a-header-module"></a>Module, die in einem Kopfzeilenmodul verfügbar sind

Die folgenden Module können im Kopfzeilenmodul verwendet werden:

- **Navigationsmenü** – Das Navigationsmenü stellt die Kanalnavigationshierarchie und anderen statischen Navigationslinks dar. Die Kanalnavigationshierarchie kann in Dynamics 365 Commerce konfiguriert werden. Das Navigationsmenü hat eine Eigenschaft **Navigationsquelle**, mit der die Retail Server-Navigationsmenüelemente und statische Menüelemente als Quelle angegeben werden. Wenn statische Menüelemente als Quelle angegeben werden, können relative Links zu anderen Seiten auf der Site bereitgestellt werden. Konfigurierte Artikel werden dann als Kopfzeilennavigation angezeigt. 
- **Suche** – Das Suchmodul ermöglicht es Benutzern, Suchbegriffe einzugeben, sodass sie nach Produkten suchen können. Die URL der Standardsuchseite und die Suchabfrageparameter müssen unter **Seiteneinstellungen \> Erweiterungen** angegeben werden. Das Suchmodul verfügt über Eigenschaften, mit denen Sie die Suchschaltfläche oder -Bezeichnung nach Bedarf unterdrücken können. Das Suchmodul unterstützt auch automatische Vorschlagsoptionen wie Produkt-, Keyword- und Kategoriesuchergebnisse.
- **Warenkorbsymbol** – Das Warenkorbsymbolmodul stellt das Warenkorbsymbol dar, das die Anzahl der Artikel im Warenkorb zu einem bestimmten Zeitpunkt anzeigt. Weitere Informationen finden Sie unter [Warenkorb-Symbolmodul](cart-icon-module.md).

## <a name="create-a-header-module-for-a-page"></a>Erstellen eines Kopfzeilenmoduls für eine Seite

Um ein neues Kopfzeilenmodul zu erstellen, befolgen Sie diese Schritte.

1. Erstellen Sie ein Fragment, das **Kopfzeilenfragment** heißt, und fügen Sie ein Containermodul hinzu.
1. Legen Sie im Eigenschaftsfenster für das Containermodul die Eigenschaft **Breite** auf **Container füllen** fest.
1. Fügen Sie dem Containermodul ein Werbebanner- und Cookie-Zustimmungsmodul hinzu.
1. Fügen Sie dem Fragment ein weiteres Containermodul hinzu und legen Sie die Eigenschaft **Breite** auf **Container füllen** fest.
1. Fügen Sie dem zweiten Containermodul ein Kopfzeilenmodul hinzu.
1. Fügen Sie im Slot **Navigationsmenü** des Kopfzeilenmoduls ein Navigationsmenümodul hinzu. 
1. Konfigurieren Sie im Eigenschaftenbereich für das Navigationsmenümodul die Eigenschaften des Navigationsmenümoduls.
1. Fügen Sie im Slot **Suche** des Kopfzeilenmoduls ein Suchmodul hinzu. 
1. Konfigurieren Sie im Eigenschaftenbereich für das Suchmodul die Eigenschaften des Suchmoduls. 
1. In dem Slot **Warenkorbsymbol** fügen Sie im Steckplatz des Header-Moduls ein Warenkorbsymbol-Modul hinzu. 
1. Konfigurieren Sie im Eigenschaftenbereich für das Warenkorbmodul die Eigenschaften des Warenkorbmoduls. Wenn das Warenkorbsymbol beim Bewegen des Mauszeigers einen Mini-Warenkorb anzeigen soll, wählen Sie **Wahr**, um **Mini-Warenkorb anzuzeigen**.
1. Speichern Sie das Seitenfragment, beenden Sie die Bearbeitung und veröffentlichen Sie diese. 


Um Sicherzustellen, dass eine Kopfzeile auf jeder Seite angezeigt wird, führen Sie die folgenden Schritte für jede Seitenvorlage aus, die für die Site erstellt wird.

1. Fügen Sie im Slot **Haupt** auf der Standardseite das Kopfzeilenseitenfragment hinzu, das das Kopfzeilenmodul der Kopfzeile enthält.
1. Speichern Sie die Vorlage, beenden Sie die Bearbeitung und veröffentlichen Sie diese.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Starterkit-Übersicht](starter-kit-overview.md)

[Containermodul](add-container-module.md)

[Kauffeldmodul](add-buy-box.md)

[Einkaufswagenmodul](add-cart-module.md)

[Symbol Einkaufswagenmodul](cart-icon-module.md)

[Auschecken-Modul](add-checkout-module.md)

[Auftragsbestätigungsmodul](order-confirmation-module.md)

[Kopfzeilenmodul](author-header-module.md)

[Fußzeilenmodul](author-footer-module.md)
