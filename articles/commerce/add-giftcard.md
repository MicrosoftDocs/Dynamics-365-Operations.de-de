---
title: Geschenkkartenmodul
description: Dieses Thema enthält Geschenkkartenmodule und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 41f808d671bf5e7425390484ea30470e044899d8
ms.sourcegitcommit: ae0843763a8b6b232bb71db326fab28605ac6c53
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2020
ms.locfileid: "3661241"
---
# <a name="gift-card-module"></a>Geschenkkartenmodul

[!include [banner](includes/banner.md)]

Dieses Thema enthält Geschenkkartenmodule und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.

## <a name="overview"></a>Übersicht

Geschenkkarten sind eine übliche Zahlungsmethode, und das Geschenkkartenmodul kann in einem Checkout-Modul zum Akzeptieren von Geschenkkarten verwendet werden. Das Geschenkkartenmodul unterstützt Dynamics 365-, SVS- und Givex-Geschenkkarten. SVS- und Givex-Geschenkkarten werden über den Adyen-Zahlungsanbieter eingelöst.

Weitere Informationen zur Unterstützung externer Geschenkkarten wie SVS und Givex finden Sie unter [Unterstützung für externe Geschenkkarten](./dev-itpro/gift-card.md)

Das folgende Bild zeigt ein Beispiel eines Geschenkkartenmoduls, das auf einer Auschecken-Seite verwendet wird.

![Beispiel eines Geschenkkarten-Moduls](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a>Moduleigenschaften

- **Zusätzliche Felder anzeigen** – Diese Eigenschaft definiert, welche Felder für Geschenkkarten zusätzlich zur Geschenkkartennummer angezeigt werden sollen, die standardmäßig immer angezeigt wird. Beispielsweise unterstützen einige Geschenkkarten die Anzeige einer persönlichen Identifikationsnummer (PIN), andere die Anzeige einer PIN und eines Ablaufdatums. Alternativ könnte diese Eigenschaft auf Keine gesetzt werden, wodurch nur die Geschenkkartennummer und keine zusätzlichen Felder angezeigt werden.

Unterstützte Werte:
-   PIN
-   Ablaufdatum
-   Pin und Ablaufdatum festlegen 
-   Keiner

## <a name="site-settings-for-gift-card-modules"></a>Site-Einstellungen für Geschenkkartenmodule

Im Commerce Site Builder unter **Seiteneinstellungen \> Erweiterungen** gibt es eine Geschenkkartenmoduleinstellung namens **Unterstützter Geschenkkartentyp**. Diese Einstellung unterstützt drei Werte:
- **Dynamics 365 Geschenkkarte** – Wenn diese Einstellung angewendet wird, ermöglicht das Geschenkkartenmodul nur das Einlösen von Dynamics 365-Geschenkkarten. Diese Einstellung wird nur für angemeldete Benutzer auf der E-Commerce-Site unterstützt.
- **SVS und Givex Geschenkkarte** – Wenn diese Einstellung angewendet wird, ermöglicht das Geschenkkartenmodul nur das Einlösen von Givex und SVS Geschenkkarten. Diese Einstellung wird nur für angemeldete und anonyme Benutzer auf der E-Commerce-Site unterstützt.
- **Dynamics 365, SVS und Givex Geschenkkarte** – Wenn diese Einstellung angewendet wird, ermöglicht das Geschenkkartenmodul nur das Einlösen von Dynamics 365-Geschenkkarten. Diese Einstellung wird nur für angemeldete Benutzer auf der E-Commerce-Site unterstützt.

## <a name="add-a-gift-card-module-to-a-page"></a>Hinzufügen eines Geschenkkartenmoduls zu einer Seite

Anweisungen zum Hinzufügen eines Geschenkkartenmoduls zu einer Checkout-Seite und zum Festlegen der erforderlichen Eigenschaften finden Sie unter [Checkout-Modul](add-checkout-module.md).

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Einkaufswagenmodul](add-cart-module.md)

[Modul für Einkaufswagensymbol](cart-icon-module.md)

[Auschecken-Modul](add-checkout-module.md)

[Zahlungsmodul](payment-module.md)

[Versandadressmodul](ship-address-module.md)

[Lieferoptionsmodul](delivery-options-module.md)

[Auftragsdetailmodul](order-confirmation-module.md)

[Unterstützung für externe Geschenkgutscheine](./dev-itpro/gift-card.md)
