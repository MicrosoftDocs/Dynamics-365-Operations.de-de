---
title: Kopfzeilenmodul
description: In diesem Thema werden Kopfzeilenmodule behandelt und deren Erstellung in Microsoft Dynamics 365 Commerce beschrieben.
author: anupamar
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
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: cc98419077f6f563ea2265d4e68ba809971cfbd6
ms.sourcegitcommit: ff93b8f6a11993f2cd00be2da7aa77ef0d950ab8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/03/2019
ms.locfileid: "2885477"
---
# <a name="header-module"></a>Kopfzeilenmodul

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

In diesem Thema werden Kopfzeilenmodule behandelt und deren Erstellung in Microsoft Dynamics 365 Commerce beschrieben.

## <a name="overview"></a>Übersicht

Ein Kopfmodul ist ein spezieller Container, der verwendet wird, um alle Module zu hosten, die in der Kopzeile auf der Seite angezeigt werden. Beispielsweise kann es das Sitelogo, Links zur Navigationshierarchie, Links zu anderen Seiten auf der Site und die Suchenleiste umfassen.

Ein Kopfmodul wird automatisch für das Gerät optimiert, auf dem die Site anzgezeigt wird (z.B. Desktopgerät oder mobiles Gerät). Beispiel wird auf einem mobilen Gerät die Navigationsleiste in einer Schaltfläche **Menü** verringert (mitunter auch als *Hamburgermenü* bezeichnet).

## <a name="properties-of-a-header"></a>Eigenschaften einer Kopfzeile

Wie die generischen Container unterstützt ein Kopfzeilenmodul die Eigenschaften für die **Überschrift** und die **Breite**.

Ein Kopfzeilenmodul hat mehrere Slots. Beispielsweise gibt es Slots für eine Informationsmeldung, ein Navigationsmenü, Logo, Suchleiste, Einkaufskorbsymbol, Wunschlistensymbol und Kontoinformationen. Jeder Slot unterstützt ein bestimmtes Modulset.

## <a name="modules-that-are-available-in-a-header-module"></a>Module, die in einem Kopfzeilenmodul verfügbar sind

Die folgenden Module können im Kopfzeilenmodul verwendet werden:

- **Navigationsmenü** – Das Navigationsmenü stellt die Kanalnavigationshierarchie und anderen statischen Navigationslinks dar. Die Kanalnavigationshierarchie kann in Dynamics 365 Retail konfiguriert werden. Konfigurierte Artikel werden dann als Kopfzeilennavigation angezeigt. Darüber hinaus können statische Navigationslinks konfiguriert werden und es können relative Links zu anderen Seiten auf der E-Commerce-Webseite bereitgestellt werden. Die Kopfzeile kann links, rechts oder in der Mitte ausgerichtet werden.
- **Einkaufswagensymbol** – Das Einkaufswagensymbol ist ein spezielles Symbol, das den Einkaufswagen darstellt. Sie wird in der Kopfzeile dargestellt und zeigt die Anzahl der Element im Einkaufswagen. Ein Link zu der Einkaufswagenseite sollte das Einkaufswagensymbol begleiten, damit Kunden zur Einkaufswagenseite umgeleitet werden können, wenn sie mit dem Symbol interagieren.
- **Wunschlistensymbol** – Das Wunschlistensymbol wird in der Kopfzeile angezeigt und zeigt die Anzahl der Artikel an, die der Wunschliste des Kunden hinzugefügt wurden. Ein Link zu der Wunschlistenseite begleitet dieses Symbol, so dass der Kunde auf die Wunschlistenseite umgeleitet werden kann, wenn er mit dem Symbol interagieren.
- **Anmeldungsmodul** – Das Anmeldungsmodul wird in der Kopfzeile angezeigt. Sie ermöglicht es Kunden, sich entweder beim Konto anzumelden oder sich für ein Konto zu registrieren. Wenn der Debitor bereits angemeldet ist, kann das Modul so konfiguriert werden, dass Links zur Kontoauftragsverlaufseite oder einer anderen Seite angezeigt werden.
- **Logomodul** – Dieses Modul enthält das Logos, das den Einzelhändler und die Marke darstellt. Es ist ein Bild, das einen Link hat. Der Link wird normalerweise so konfiguriert, dass er eine Umleitung zur Startseite enthält. Deshalb können Debitoren rasch von jeder beliebigen Seite aus auf die Startseite zurückkehren.
- **Warnung** – Eine Warnung wird in der Kopfzeile angezeigt und wird verwendet, um eine Inline-Meldung anzuzeigen, die auf alle Seiten der Site Geltung hat. Beispielsweise könnte eine Warnung eine Nachricht anzeigen wie „Jahresendverkauf endet in 2 Tagen“.
- **Suchenleiste** – Die Suchenleiste ermöglicht es Benutzern, Suchbegriffe einzugeben, sodass sie nach Produkten suchen können. Das Modul muss mit der URL der Suchergebnisseite konfiguriert werden. Der Abfragezeichenfolgenparameter kann konfiguriert werden (der Standardwert ist **„q“**). Die Suchenleiste hat einen Slot mit automatischen Vorschlägen, in dem das Modul automatische Vorschläge hinzugefügt werden soll.
- **Automatische Vorschläge** – Das Modul automatische Vorschläge zeigt die automatisch vorgeschlagenen Ergebnisse. Die Ergebnisse können Schlüsselwörter, Produkte oder Kategorien sein, in denen Suchbegriffe gefunden wurden.

## <a name="create-a-header-module"></a>Erstellen eines Kopfzeilenmoduls

Um ein neues Kopfzeilenmodul zu erstellen, befolgen Sie diese Schritte.

1. Erstellen Sie ein Seitenfragment, das ein Kopfzeilenmodul enthält.
1. Fügen Sie Module den Slots im Kopfzeilenmodul hinzu.
1. Aktualisieren Sie die Einstellungen für jedes Modul.
1. Speichern Sie das Seitenfragment. 
1. Laden Sie die Seite hoch und veröffentlichen Sie sie.

Um Sicherzustellen, dass eine Kopfzeile auf jeder Seite angezeigt wird, führen Sie die folgenden Schritte für jede Seitenvorlage aus, die für die Site erstellt wird.

1. Auf der Standardseite fügen Sie das Seitenfragment hinzu, das das Kopfzeilenmodul im Hauptslot enthält.
1. Vorlage speichern. 
1. Überprüfen Sie in die Vorlage, und veröffentlichen Sie sie.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Starterkit-Überblick](starter-kit-overview.md)

[Containermodul](add-container-module.md)

[Kauffeldmodul](add-buy-box.md)

[Einkaufswagenmodul](add-cart-module.md)

[Auschecken-Modul](add-checkout-module.md)

[Auftragsbestätigungsmodul](order-confirmation-module.md)

[Kopfzeilenmodul](author-header-module.md)

[Fußzeilenmodul](author-footer-module.md)
