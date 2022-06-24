---
title: Modul für Einkaufswagensymbol
description: Dieser Artikel behandelt das Warenkorbsymbolmodul und es wird beschrieben, wie es Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt wird.
author: anupamar-ms
ms.date: 08/02/2021
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
ms.openlocfilehash: a5b86b0c843a680dd0c46295a69e12d6e3542619
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859112"
---
# <a name="cart-icon-module"></a>Modul für Einkaufswagensymbol

[!include [banner](includes/banner.md)]

Dieser Artikel behandelt das Warenkorbsymbolmodul und es wird beschrieben, wie es Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt wird.

Warenkorbsymbol – Das Warenkorbsymbolmodul im Kopfmodul der Seite zeigt die Anzahl der Artikel im Warenkorb zu einem bestimmten Zeitpunkt an. Das Warenkorbsymbolmodul zeigt auch eine Warenkorbübersicht (auch als Minikorb bezeichnet) an, wenn Sie den Mauszeiger über das Warenkorbsymbol halten. Der Mini-Warenkorb bietet dem Benutzer eine Zusammenfassung der Artikel im Warenkorb, ohne zur Warenkorbseite navigieren zu müssen. Darüber hinaus kann der Benutzer direkt zur Checkout-Seite gehen, wenn er mit der Zusammenfassung zufrieden ist. Dies reduziert die Anzahl der Seitennavigationen und beschleunigt das Auschecken. 

Das folgende Bild zeigt ein Beispiel für ein Warenkorbsymbolmodul, das einen Mini-Wagen in der Fabrikam-Kopfzeile anzeigt.

![Beispiel eines Warenkorbsymbolmoduls.](./media/ecommerce-Minicart.PNG)

## <a name="module-properties"></a>Moduleigenschaften

- **Mini-Warenkorb anzeigen**: Wenn diese Eigenschaft auf **wahr** gesetzt ist, wird eine Warenkorbübersicht (Mini-Warenkorb) angezeigt, wenn Benutzer den Mauszeiger über das Warenkorbsymbol bewegen. Diese Funktionalität wird nur für Desktop-Ansichtsports unterstützt.
- **Anonymes Zurkassegehen erlauben**: Wenn diese Eigenschaft auf **Wahr** gesetzt ist, erlaubt der Mini-Warenkorb Benutzern, die nicht abgemeldet sind, als Gast zur Kasse zu gehen. Diese Eigenschaft ist in der Commerce-Version 10.0.21 als Teil des Commerce-Modulbibliothekspakets verfügbar.
- **Artikelreihenfolge**: Diese Eigenschaft steuert die Reihenfolge, in der Artikel im Mini-Warenkorb erscheinen. Wenn die Option **Neue Artikel am Anfang der Liste hinzufügen** ausgewählt ist, werden neue Artikel, die dem Warenkorb hinzugefügt werden, oben in der Liste der Artikel des Mini-Warenkorbs angezeigt. Wenn die Standardoption **Neue Artikel am Ende der Liste hinzufügen** ausgewählt ist, werden neue Artikel, die dem Warenkorb hinzugefügt werden, unten in der Liste der Artikel des Mini-Warenkorbs angezeigt. Diese Eigenschaft ist ab Commerce-Version 10.0.21 als Teil des Commerce-Modulbibliothekspakets verfügbar.

> [!IMPORTANT]
> Die Eigenschaft **Anonymes Zurkassegehen erlauben** und **Artikelreihenfolge** sind ab der Commerce-Version 10.0.21 verfügbar. Sie erfordern, dass das Commerce-Modulbibliothekspaket in der Version 9.31 installiert ist.

## <a name="module-properties-and-slots-in-the-adventure-works-theme"></a>Moduleigenschaften und Slots im Adventure Works-Design

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
