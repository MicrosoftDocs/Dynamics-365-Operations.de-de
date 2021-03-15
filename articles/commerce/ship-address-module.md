---
title: Versandadressmodul
description: In diesem Thema wird das Versandadressmodul behandelt und beschrieben, wie es in Microsoft Dynamics 365 Commerce konfiguriert wird.
author: anupamar-ms
manager: annbe
ms.date: 08/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 6a5eb69c7746be419779b1a844ee35ec375a324c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985635"
---
# <a name="shipping-address-module"></a>Versandadressmodul

[!include [banner](includes/banner.md)]

In diesem Thema wird das Versandadressmodul behandelt und beschrieben, wie es in Microsoft Dynamics 365 Commerce konfiguriert wird.

## <a name="overview"></a>Übersicht

Das Versandadressmodul ermöglicht Debitoren die Versandadresse für einen Auftrag während des Checkout-Flows hinzuzufügen oder auszuwählen. Wenn der Debitor angemeldet ist, werden alle zuvor gespeicherten Adressen für diesen Debitor angezeigt, und der Debitor kann zwischen diesen auswählen. Der Debitor kann auch eine neue Adresse hinzufügen. Die Versandadressmodul wird für alle Artikel in einem Auftrag verwendet, die Versand erfordern.

Versandadressformate können in der Commerce-Zentrale für jedes Land oder jede Region definiert werden, und das Versandadressmodul setzt dann länderspezifische Regeln durch.

Wenn Debitoren während des Bestellvorgangs eine Versandadresse eingeben, haben sie die Möglichkeit, die Adresse als primäre Adresse zu speichern. Diese Option wird nur angezeigt, wenn ein Debitor angemeldet ist.

Obwohl das Versandadressmodul keine Adressüberprüfung bereitstellt, kann diese Funktion über die Anpassung implementiert werden.

Die folgende Abbildung zeigt ein Beispiel eines neuen Versandadressenmoduls auf einer Checkout-Seite.

![Beispiel eines Versandadressenmoduls auf einer Checkout-Seite](./media/ecommerce-shippingaddress.PNG)

## <a name="module-properties"></a>Moduleigenschaften

| Eigenschaftenname | Werte | Beschreibung |
|---------------|--------|-------------|
| Überschrift | Überschriftentext und eine Überschriftsmarkierung (**H1**, **H2**, **H3**, **H4**, **H5** oder **H6**) | Eine optionale Überschrift für das Versandadressmodul. |
| Adresstyp anzeigen | **True** oder **False** | Wenn diese optionale Eigenschaft auf **True** gesetzt ist, wird ein Adresstyp, wie z. B. **Start** oder **Unternehmen**, angezeigt. Wenn kein Adresstyp angegeben ist, wird die Adresse automatisch als **Art**=**Sonstige** gespeichert. |

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]