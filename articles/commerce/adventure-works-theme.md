---
title: Adventure Works-Design – Überblick
description: Dieses Design bietet einen Überblick über das Adventure Works-Design und beschreibt, wie Sie es auf Websiteseiten in Microsoft Dynamics 365 Commerce verwenden.
author: anupamar-ms
ms.date: 07/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: c8183d09e15f83606d84fddd02cb2dfb9b2fb528
ms.sourcegitcommit: 0c77dbb8547cd36fce3977ca9515fa1474efa77a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/22/2021
ms.locfileid: "6655631"
---
# <a name="adventure-works-theme-overview"></a>Adventure Works-Design – Überblick

[!include [banner](includes/banner.md)]

Dieses Design bietet einen Überblick über das Adventure Works-Design und beschreibt, wie Sie es auf Websiteseiten in Microsoft Dynamics 365 Commerce verwenden.

Dynamics 365 Commerce hat ein E-Commerce-Design, das Adventure Works heißt. Das Adventure Works-Design präsentiert Sport- und Freizeitprodukte und ist für ein reichhaltiges und verbessertes Storytelling-Erlebnis optimiert. Es hat ein modernes Erscheinungsbild, neues Layouts und Animationseffekte, um E-Commerce-Kunden ein immersives, ansprechendes Online-Shopping-Erlebnis zu bieten.

## <a name="trial-environments-in-commerce"></a>Testumgebungen in Commerce

Um zu sehen, wie das Adventure Works-Design aussieht, wenn es für Business-to-Consumer (B2C)- und Business-to-Business (B2B)-Sites bereitgestellt wird, besuchen Sie die folgenden Test-Sites:

- [Adventure Works-B2C-Site](https://www.adventure-works.com/)
- [Adventure Works-B2B-Site](https://www.adventure-works.com/business)

## <a name="theme-capabilities"></a>Themenfunktionen

Das Adventure Works-Design bietet die folgenden neuen Funktionen:

- Das Videoplayer-Modul unterstützt jetzt Funktionen für Überschriften, Absätze und Links für zusätzliches Storytelling.
- Es gibt bessere Übergänge von Inhalten durch Animationen.
- Die Aktivität „Zum Warenkorb hinzufügen“ ruft den Mini-Warenkorb auf, anstatt eine Benachrichtigung bereitzustellen.
- Das Schnellansichtsmodul ist ein Bereich, der sowohl in Desktop- als auch in mobilen Viewports eingeschoben wird.
- Es gibt neue Layouts für die Site-Seiten. 
- Marketinginhalte können für den Warenkorb und den Mini-Warenkorb konfiguriert werden, wenn diese leer sind.
- Im Mini-Warenkorb können Werbebotschaften angezeigt werden, z. B. kostenloser Versand bei Bestellungen über $50.
- Beschreibungskarten werden auf Such- und Kategorieseiten gerendert.

Das Adventure Works-Design enthält nun die folgenden Storytelling-Module in der Commerce-Modulbibliothek:

- [Kachellistenmodul](tile-list-module.md)
- [Interaktives Funktionsmodul](interactive-feature-module.md)
- [Aktives Bildmodul](active-image-module.md)
- [Modul abonnieren](subscribe-module.md)
- [Bildlistenmodul](image-list-module.md)

Das Adventure Works-Design reagiert vollständig und bietet eine optimierte Erfahrung für Desktop-, Mobil- und Tablet-Viewports.

> [!IMPORTANT]
> Das Adventure Works-Design und die neuen Module stehen ab der Dynamics 365 Commerce-Version 10.0.20 zur Verfügung.

Die folgende Abbildung zeigt ein Beispiel für eine Homepage, die das Adventure Works-Design verwendet.

![Beispiel für eine Homepage, die das Adventure Works-Design verwendet](./media/aw_b2c.PNG)

Die folgende Abbildung zeigt ein Beispiel für eine Listenseite, die das Adventure Works-Design verwendet.

![Beispiel für eine Listenseite, die das Adventure Works-Design verwendet](./media/Aw_list.PNG)

Die folgende Abbildung zeigt ein Beispiel für eine Produktdetailseite (PDP), die das Adventure Works-Design verwendet.

![Beispiel für eine Produktdetailseite (PDP), die das Adventure Works-Design verwendet](./media/aw_pdp.PNG)

## <a name="use-the-adventure-works-theme-for-b2b-sites"></a>Das Adventure Works-Design für B2B-Websites verwenden

Das Adventure Works-Design ist auch ein Referenzthema für Business-to-Business (B2B)-Websites. Alle B2B-Module und -Workflows werden im Adventure Works-Design vorgestellt. Informationen zum Einrichten einer B2B-Website finden Sie unter [B2B-Website einrichten](./b2b/set-up-b2b-site.md).

Die folgende Abbildung zeigt ein Beispiel für eine B2B-Homepage, die das Adventure Works-Design verwendet.

![Beispiel für eine B2B-Homepage, die das Adventure Works-Design verwendet](./media/aw_b2b.PNG)

## <a name="theme-extensions"></a>Design-Erweiterungen

Das Adventure Works-Design enthält mehrere Designerweiterungen, wie z. B. die Erweiterungen **Erweiterungen anzeigen** und **Moduldefinition**. Das Adventure Works-Design kann als Referenzdesign verwendet werden, um ähnliche Erweiterungen zu erstellen. Beispielsweise wird die Listenseite im Adventure Works-Design als Ansichtserweiterung implementiert, die über eine horizontale Einschränkung verfügt. (Im Gegensatz dazu wird im Fabrikam-Design eine Einschränkung für den linken Bereich verwendet.)

Gleichzeitig erhalten andere Module Moduldefinitionserweiterungen. Zum Beispiel enthält das [Warenkorbsymbolmodul](cart-icon-module.md) zwei zusätzliche Slots **Leerer Warenkorb** und **Werbeinhalte**, die mithilfe von Moduldefinitionserweiterungen implementiert werden. Darüber hinaus wurde dem Kopfzeilenmodul die neue Eigenschaft **Mobiles Logo** hinzugefügt, um ein Logo in mobilen Viewports zu unterstützen. Diese Eigenschaft wird als Erweiterung der Kopfzeilenmoduldefinition implementiert.

Weitere Informationen zu Designerweiterungen finden Sie unter [Designerweiterungen](e-commerce-extensibility/theme-module-extensions.md).

## <a name="install-the-adventure-works-theme"></a>Adventure Works-Design installieren

Informationen zum Installieren des Adventure Works-Designs finden Sie unter [Installieren Sie das Adventure Works-Design](install-adventure-works.md).

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Informationen zur Modulbibliothek](starter-kit-overview.md)

[Kachellistenmodul](tile-list-module.md)

[Interaktives Funktionsmodul](interactive-feature-module.md)

[Aktives Bildmodul](active-image-module.md)

[Abonnierenmodul](subscribe-module.md)

[Bildlistenmodul](image-list-module.md)

[Design-Erweiterungen](e-commerce-extensibility/theme-module-extensions.md)

[Modul für Einkaufswagensymbol](cart-icon-module.md)

[Website für B2B-E-Commerce einrichten](./b2b/set-up-b2b-site.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
