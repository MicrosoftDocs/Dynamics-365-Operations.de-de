---
title: Versandadressenmodul
description: Dieser Artikel behandelt das Versandadressenmodul und erläutert, wie es in Microsoft Dynamics 365 Commerce konfiguriert wird.
author: anupamar-ms
ms.date: 02/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: e30e639b7ba1c0caaf72fa66d13f80d04c2e861c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8882195"
---
# <a name="shipping-address-module"></a>Versandadressenmodul

[!include [banner](includes/banner.md)]

Dieser Artikel behandelt das Versandadressmodul und erläutert, wie es in Microsoft Dynamics 365 Commerce konfiguriert wird.

Das Versandadressmodul ermöglicht Debitoren die Versandadresse für einen Auftrag während des Checkout-Flows hinzuzufügen oder auszuwählen. Wenn der Debitor angemeldet ist, werden alle zuvor gespeicherten Adressen für diesen Debitor angezeigt, und der Debitor kann zwischen diesen auswählen. Der Debitor kann auch eine neue Adresse hinzufügen. Die Versandadressmodul wird für alle Artikel in einem Auftrag verwendet, die Versand erfordern.

Versandadressformate können in der Commerce-Zentrale für jedes Land oder jede Region definiert werden, und das Versandadressmodul setzt dann länderspezifische Regeln durch.

Wenn Debitoren während des Bestellvorgangs eine Versandadresse eingeben, haben sie die Möglichkeit, die Adresse als primäre Adresse zu speichern. Diese Option wird nur angezeigt, wenn ein Debitor angemeldet ist.

Obwohl das Versandadressmodul keine Adressüberprüfung bereitstellt, kann diese Funktion über die Anpassung implementiert werden.

Die folgende Abbildung zeigt ein Beispiel eines neuen Versandadressenmoduls auf einer Checkout-Seite.

![Beispiel eines Versandadressenmoduls auf einer Checkout-Seite.](./media/ecommerce-shippingaddress.PNG)

## <a name="module-properties"></a>Moduleigenschaften

| Eigenschaftenname | Werte | Beschreibung |
|---------------|--------|-------------|
| Überschrift | Überschriftentext und eine Überschriftsmarkierung (**H1**, **H2**, **H3**, **H4**, **H5** oder **H6**) | Eine optionale Überschrift für das Versandadressmodul. |
| Adresstyp anzeigen | **True** oder **False** | Wenn diese optionale Eigenschaft auf **True** gesetzt ist, wird ein Adresstyp, wie z. B. **Start** oder **Unternehmen**, angezeigt. Wenn kein Adresstyp angegeben ist, wird die Adresse automatisch als **Art**=**Sonstige** gespeichert. |
| Automatisches Vorschlagen aktivieren| **True** oder **False** | Wenn diese optionale Eigenschaft auf **True** gesetzt ist, werden automatische Adressvorschläge bereitgestellt. Diese Vorschläge werden von Bing Maps unterstützt. Informationen zum Einrichten der Bing Maps-Integration auf Ihrer Website finden Sie unter [Shopauswahlmodul](store-selector.md). Diese Funktion ist ab der Commerce-Version 10.0.15 verfügbar.|
|Optionen für automatisches Vorschlagen| Eine Anzahl| Wenn automatische Adressvorschläge aktiviert sind, können Sie zusätzliche Optionen angeben, z. B. die maximale Anzahl von Vorschlägen, die bereitgestellt werden sollen.|

## <a name="add-a-shipping-address-module-to-a-checkout-page-and-set-the-required-properties"></a>Ein Versandadressmodul in eine Checkout-Seite hinzufügen und die erforderlichen Eigenschaften bestimmen

Ein Versandadressmodul kann nur zu einem Checkout-Modul hinzugefügt werden. Weitere Informationen zum Konfigurieren des Versandadressmoduls und zum Hinzufügen zu einer Checkout-Seite finden Sie unter [Checkout-Modul](add-checkout-module.md).

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Einkaufswagenmodul](add-cart-module.md)

[Modul für Einkaufswagensymbol](cart-icon-module.md)

[Auschecken-Modul](add-checkout-module.md)

[Zahlungsmodul](payment-module.md)

[Lieferoptionenmodul](delivery-options-module.md)

[Abholinformationsmodul](pickup-info-module.md)

[Auftragsdetailmodul](order-confirmation-module.md)

[Geschenkkartenmodul](add-giftcard.md)

[Shopauswahlmodul](store-selector.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]