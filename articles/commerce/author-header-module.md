---
title: Kopfzeilenmodul
description: In diesem Thema werden Kopfzeilenmodule behandelt und die Erstellung von Kopfzeilen in Microsoft Dynamics 365 Commerce beschrieben.
author: anupamar
manager: annbe
ms.date: 05/28/2020
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
ms.openlocfilehash: e7dde3ba1ad375b309ae66cc6d31ccad85615e45
ms.sourcegitcommit: 81f162f2d50557d7afe292c8d326618ba0bc3259
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2020
ms.locfileid: "3686621"
---
# <a name="header-module"></a>Kopfzeilenmodul

[!include [banner](includes/banner.md)]

In diesem Thema werden Kopfzeilenmodule behandelt und die Erstellung von Kopfzeilen in Microsoft Dynamics 365 Commerce beschrieben.

## <a name="overview"></a>Übersicht

Im Dynamics 365 Commerce umfasst ein Seitenkopf mehrere Module, z. B. die Module Kopfzeile, Navigationsmenü, Suche, Werbebanner und Cookie-Einwilligung. 

Das Kopfzeilenmodul enthält ein Site-Logo, Links zur Navigationshierarchie, Links zu anderen Seiten der Site, ein Warenkorbsymbol, ein Wunschliste-Symbol, Anmeldeoptionen und die Suchleiste. Ein Kopfmodul wird automatisch für das Gerät optimiert, auf dem die Site angezeigt wird (anders ausgedrückt für ein Desktopgerät oder ein mobiles Gerät). Beispiel wird auf einem mobilen Gerät die Navigationsleiste in einer Schaltfläche **Menü** verringert (mitunter auch als *Hamburgermenü* bezeichnet).

Das folgende Bild zeigt ein Beispiel eines Kopfzeilenmoduls, das auf einer Startseite verwendet wird.

![Beispiel eines Kopfzeilenmoduls](./media/ecommerce-header.png)

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

1. Wechseln Sie zu **Fragmente** und wählen Sie **Neu** aus, um ein neues Fragment zu erstellen.
1. Wählen Sie im Dialogfeld **Neues Seitenfragment** das Modul **Container** aus, geben Sie einen Namen für das Seitenfragment ein und wählen Sie dann **OK** aus.
1. Wählen Sie den **Standardcontainer**-Slot aus und wählen Sie im Eigenschaftenfenster rechts die Option **Breite** aus, um den **Behälter zu füllen**.
1. Wählen Sie im Slot **Standard-Container** die Ellipsen-Schaltfläche (**...**) und wählen Sie **Modul hinzufügen**.
1. Im Dialogfeld **Modul hinzufügen** wählen Sie die Module **Promotionsanzeige** und **Cookie-Zustimmung** und wählen dann **OK** aus.
1. Wählen Sie im Slot **Standard-Container** die Ellipsen-Schaltfläche (**...**) und wählen Sie **Modul hinzufügen**.
1. Wählen Sie im Dialogfeld **Modul hinzufügen** wählen Sie das Modul **Container** und dann **OK** aus.
1. Wählen Sie den **Container**-Slot aus und wählen Sie im Eigenschaftenbereich rechts die Option **Breite** aus, um den **Behälter zu füllen**.
1. Wählen Sie im Slot **Container** die Ellipsen-Schaltfläche (**...**) und wählen Sie **Modul hinzufügen**.
1. Wählen Sie im Dialogfeld **Modul hinzufügen** das Modul **Kopfzeile** und dann **OK** aus.
1. Im Slot **Navigationsmenü** wählen Sie das Kopfzeilenmodul, wählen die Ellipsen (**...**) und wählen **Modul hinzufügen**.
1. Im Dialogfeld **Modul hinzufügen** wählen Sie das Modul **Navigationsmenü** und wählen Sie dann **OK**.
1. Konfigurieren Sie im Eigenschaftenbereich für das Navigationsmenümodul die Eigenschaften des Navigationsmenümoduls nach Bedarf.
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

[Überblick über Starterkit](starter-kit-overview.md)

[Containermodul](add-container-module.md)

[Kauffeldmodul](add-buy-box.md)

[Einkaufswagenmodul](add-cart-module.md)

[Symbol Einkaufswagenmodul](cart-icon-module.md)

[Auschecken-Modul](add-checkout-module.md)

[Auftragsbestätigungsmodul](order-confirmation-module.md)

[Kopfzeilenmodul](author-header-module.md)

[Fußzeilenmodul](author-footer-module.md)
