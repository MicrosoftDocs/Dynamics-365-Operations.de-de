---
title: Symbol Einkaufswagenmodul
description: Dieses Thema enthält das Warenkorbsymbolmodul und es wird beschrieben, wie es Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 137debe3f4cad3948d20b2902ea80e66fa74ffd4
ms.sourcegitcommit: ae0843763a8b6b232bb71db326fab28605ac6c53
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2020
ms.locfileid: "3661146"
---
# <a name="cart-icon-module"></a>Symbol Einkaufswagenmodul

[!include [banner](includes/banner.md)]

Dieses Thema enthält das Warenkorbsymbolmodul und es wird beschrieben, wie es Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.

## <a name="overview"></a>Übersicht

Warenkorbsymbol – Das Warenkorbsymbolmodul im Kopfmodul der Seite zeigt die Anzahl der Artikel im Warenkorb zu einem bestimmten Zeitpunkt an. Das Warenkorbsymbolmodul zeigt auch eine Warenkorbübersicht (auch als Minikorb bezeichnet) an, wenn Sie den Mauszeiger über das Warenkorbsymbol halten. Der Mini-Warenkorb bietet dem Benutzer eine Zusammenfassung der Artikel im Warenkorb, ohne zur Warenkorbseite navigieren zu müssen. Darüber hinaus kann der Benutzer direkt zur Checkout-Seite gehen, wenn er mit der Zusammenfassung zufrieden ist. Dies reduziert die Anzahl der Seitennavigationen und beschleunigt das Auschecken. 

Das folgende Bild zeigt ein Beispiel für ein Warenkorbsymbolmodul, das einen Mini-Wagen in der Fabrikam-Kopfzeile anzeigt.

![Beispiel eines Warenkorbsymbolmoduls](./media/ecommerce-Minicart.PNG)

## <a name="module-properties"></a>Moduleigenschaften

- **Mini-Warenkorb anzeigen** – Wenn true, kann mit dieser Eigenschaft eine Warenkorbübersicht (Mini-Warenkorb) angezeigt werden, wenn Sie den Mauszeiger über das Warenkorbsymbol bewegen. Diese Funktionalität wird nur für Desktop-Ansichtsports unterstützt.

## <a name="add-a-cart-icon-module-to-a-page"></a>Ein Warenkorbsymbolmodul einer Seite hinzufügen

Informationen zum Hinzufügen eines Warenkorbsymbolmoduls finden Sie unter [Kopf-Modul](author-header-module.md).

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Einkaufswagenmodul](add-cart-module.md)

[Auschecken-Modul](add-checkout-module.md)

[Zahlungsmodul](payment-module.md)

[Versandadressmodul](ship-address-module.md)

[Lieferoptionsmodul](delivery-options-module.md)

[Auftragsdetailmodul](order-confirmation-module.md)

[Geschenkkartenmodul](add-giftcard.md)
