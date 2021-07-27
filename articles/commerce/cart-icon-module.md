---
title: Symbol Einkaufswagenmodul
description: Dieses Thema behandelt das Warenkorbsymbolmodul und es wird beschrieben, wie es Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt wird.
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e0238e9d464fc1d44cbc5091638ac7270d5b6ae3
ms.sourcegitcommit: 7e976059118938b0089e40bef948029a8c088b38
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "6479303"
---
# <a name="cart-icon-module"></a>Modul für Einkaufswagensymbol

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Dieses Thema behandelt das Warenkorbsymbolmodul und es wird beschrieben, wie es Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt wird.

Warenkorbsymbol – Das Warenkorbsymbolmodul im Kopfmodul der Seite zeigt die Anzahl der Artikel im Warenkorb zu einem bestimmten Zeitpunkt an. Das Warenkorbsymbolmodul zeigt auch eine Warenkorbübersicht (auch als Minikorb bezeichnet) an, wenn Sie den Mauszeiger über das Warenkorbsymbol halten. Der Mini-Warenkorb bietet dem Benutzer eine Zusammenfassung der Artikel im Warenkorb, ohne zur Warenkorbseite navigieren zu müssen. Darüber hinaus kann der Benutzer direkt zur Checkout-Seite gehen, wenn er mit der Zusammenfassung zufrieden ist. Dies reduziert die Anzahl der Seitennavigationen und beschleunigt das Auschecken. 

Das folgende Bild zeigt ein Beispiel für ein Warenkorbsymbolmodul, das einen Mini-Wagen in der Fabrikam-Kopfzeile anzeigt.

![Beispiel eines Warenkorbsymbolmoduls.](./media/ecommerce-Minicart.PNG)

## <a name="module-properties"></a>Moduleigenschaften

- **Mini-Warenkorb anzeigen** – Wenn true, kann mit dieser Eigenschaft eine Warenkorbübersicht (Mini-Warenkorb) angezeigt werden, wenn Sie den Mauszeiger über das Warenkorbsymbol bewegen. Diese Funktionalität wird nur für Desktop-Ansichtsports unterstützt.

## <a name="module-properties-in-the-adventure-works-theme"></a>Moduleigenschaften im Adventure Works-Design

Im Adventure Works-Design enthält das Warenkorbsymbolmodul zwei zusätzliche Slots für den Mini-Warenkorb. Diese Slots sind als Erweiterung der Moduldefinition enthalten.

- **Warenkorbwerbeaktionen leeren** – Dieser Slots nimmt ein Inhaltsblockmodul auf. Wenn der Warenkorb leer ist, wird das angegebene Inhaltsblockmodul angezeigt. Das Inhaltsblockmodul kann für Werbeaktionen, Marketinginhalte und Links zu Kategorieseiten verwendet werden, um Kunden bei der Fortsetzung ihrer Einkaufsreise zu unterstützen.
- **Werbeinhalte** – Dieser Slot kann verwendet werden, um Werbeaktionen wie „Versand bei Bestellungen über 100 $ kostenlos“ vorzustellen. Inhaltsblock-, Textblock- und Bildlistenmodule können im Werbeinhalts-Slot verwendet werden.

Das folgende Bild zeigt ein Beispiel für ein Warenkorbsymbolmodul im Adventure Works-Design, das Werbeinhalte auf dem Mini-Warenkorb anzeigt.

![Beispiel für ein Warenkorbsymbolmodul im Adventure Works-Design](./media/AW_minicart.PNG)

> [!IMPORTANT]
> Das Adventure Works-Designslots stehen ab der Dynamics 365 Commerce-Version 10.0.20 zur Verfügung.

## <a name="add-a-cart-icon-module-to-a-page"></a>Ein Warenkorbsymbolmodul einer Seite hinzufügen

Informationen zum Hinzufügen eines Warenkorbsymbolmoduls finden Sie unter [Kopf-Modul](author-header-module.md).

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Einkaufswagenmodul](add-cart-module.md)

[Auschecken-Modul](add-checkout-module.md)

[Zahlungsmodul](payment-module.md)

[Versandadressenmodul](ship-address-module.md)

[Lieferoptionenmodul](delivery-options-module.md)

[Abholinformationsmodul](pickup-info-module.md)

[Auftragsdetailmodul](order-confirmation-module.md)

[Geschenkkartenmodul](add-giftcard.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
