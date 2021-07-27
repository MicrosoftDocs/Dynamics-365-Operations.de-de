---
title: Adventure Works-Design – Überblick
description: Dieses Design bietet einen Überblick über das Adventure Works-Design und beschreibt, wie Sie es auf Websiteseiten in Microsoft Dynamics 365 Commerce verwenden.
author: anupamar-ms
ms.date: 07/08/2021
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
ms.openlocfilehash: c7557a36a948de5ae877d74bbbdea78821099b82
ms.sourcegitcommit: 7e976059118938b0089e40bef948029a8c088b38
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "6479460"
---
# <a name="adventure-works-theme-overview"></a>Adventure Works-Design – Überblick

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Dieses Design bietet einen Überblick über das Adventure Works-Design und beschreibt, wie Sie es auf Websiteseiten in Microsoft Dynamics 365 Commerce verwenden.

Dynamics 365 Commerce hat ein E-Commerce-Design, das Adventure Works heißt. Das Adventure Works-Design präsentiert Sport- und Freizeitprodukte und ist für ein reichhaltiges und verbessertes Storytelling-Erlebnis optimiert. Es hat ein modernes Erscheinungsbild, neues Layouts und Animationseffekte, um E-Commerce-Kunden ein immersives, ansprechendes Online-Shopping-Erlebnis zu bieten.

Das Adventure Works-Design bietet die folgenden neuen Workflows:

- Das Videoplayer-Modul unterstützt jetzt Funktionen für Überschriften, Absätze und Links für zusätzliches Storytelling.
- Die Aktivität „Zum Warenkorb hinzufügen“ ruft den Mini-Warenkorb auf, anstatt eine Benachrichtigung bereitzustellen.
- Das Schnellansichtsmodul ist ein Bereich, der sowohl in Desktop- als auch in mobilen Viewports eingeschoben wird.
- Ein leerer Warenkorb kann jetzt Promotionen vorstellen.

Das Adventure Works-Design enthält die folgenden Storytelling-Module in der Commerce-Modulbibliothek:

- Kachellistenmodul
- Interaktives Funktionsmodul
- Abonnierenmodul
- Aktives Bildmodul
- Bildlistenmodul

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
