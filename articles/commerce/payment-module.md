---
title: Zahlungsmodul
description: In diesem Thema wird das Zahlungsmodul behandelt und beschrieben, wie es in Microsoft Dynamics 365 Commerce konfiguriert wird.
author: anupamar-ms
manager: annbe
ms.date: 08/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: f4f6baa3c4a42a2994cab772c98d373996e2648b
ms.sourcegitcommit: ae0843763a8b6b232bb71db326fab28605ac6c53
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2020
ms.locfileid: "3661205"
---
# <a name="payment-module"></a>Zahlungsmodul

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

In diesem Thema wird das Zahlungsmodul behandelt und beschrieben, wie es in Microsoft Dynamics 365 Commerce konfiguriert wird.

## <a name="overview"></a>Übersicht

Das Zahlungsmodul ermöglicht es Debitoren, für eine Bestellung mit Kredit‑ oder Debitkarten zu bezahlen. Die Zahlungsintegration für dieses Modul wird vom Zahlungskonnektor von Dynamics 365 für Adyen gewährleistet. Weitere Informationen darüber, wie der Zahlungskonnektor für konfiguriert und eingerichtet wird, finden Sie unter [Zahlungskonnektor von Dynamics 365 für Adyen](dev-itpro/adyen-connector.md).

Das Zahlungsmodul hostet die Zahlungsinformationen, die über Adyen bereitgestellt werden, in einem HTML-Inlineframe (iFrame). Das Zahlungsmodul interagiert mit der Commerce Scale Unit, um die Adyen-Zahlungsinformationen abzurufen. Im Rahmen der Commerce Scale Unit-Interaktion kann das Zahlungsmodul die Bereitstellung von Rechnungsadressinformationen entweder im iFrame oder als separates Modul ermöglichen. Im Fabrikam-Design wird die Rechnungsadresse in einem separaten Modul angezeigt. Dieser Ansatz ermöglicht eine größere Flexibilität bei der Formatierung, da die Adresszeilen so gerendert werden können, dass sie den Zeilen der Lieferadresse ähneln.

Mit dem Zahlungsmodul können angemeldete Debitoren auch ihre Zahlungsinformationen speichern. Die Zahlungsinformationen und die Rechnungsadresse werden über den Adyen-Zahlungskonnektor gespeichert und verwaltet.

Das Zahlungsmodul deckt alle Auftragszuschläge ab, die nicht bereits durch Treuepunkte oder eine Geschenkkarte gedeckt sind. Wenn der Gesamtbetrag einer Bestellung vollständig durch Treuepunkte oder Gutschriften für Geschenkkarten gedeckt ist, wird das Zahlungsmodul ausgeblendet und der Debitor kann die Bestellung ohne diese aufgeben.

Der Adyen-Zahlungskonnektor unterstützt auch Starke Kundenauthentifizierung (SCA). Ein Teil der Richtlinie über Zahlungsdienste der Europäischen Union (EU) 2.0 (PSD2.0) verlangt, dass Online-Käufer außerhalb ihres Online-Einkaufserlebnisses authentifiziert werden, wenn sie eine elektronische Zahlungsmethode verwenden. Während des Checkout-Flows werden Debitoren zur Website ihrer Bank weitergeleitet. Nach der Authentifizierung werden sie dann zurück zum Commerce-Checkout-Flow umgeleitet. Während dieser Umleitung bleiben die Informationen, die ein Debitor in den Checkout-Flow eingegeben hat (z. B. Versandadresse, Lieferoptionen, Geschenkkarteninformationen und Treueinformationen), erhalten. Bevor Sie diese Funktion aktivieren können, muss der Zahlungskonnektor für SCA in der Commerce-Zentrale konfiguriert sein. Weitere Informationen finden Sie unter [Starke Kundenauthentifizierung mit Adyen](adyen_redirect.md).

Die folgende Abbildung zeigt ein Beispiel für Geschenkkarten‑, Treuepunkt‑, Zahlungsmodule auf einer Checkout-Seite.

![Beispiel für Geschenkkarten‑, Treuepunkt‑ und Zahlungsmodule auf einer Checkout-Seite](./media/ecommerce-payments.PNG)

## <a name="payment-module-properties"></a>Zahlungsmoduleigenschaften

| Eigenschaftenname | Werte | Beschreibung |
|---------------|--------|-------------|
| Überschrift | Überschriftentext | Eine optionale Überschrift für das Zahlungsmodul. |
| Höhe des iFrame | Pixel | Die iFrame-Höhe in Pixel. Die Höhe kann nach Bedarf geändert werden. |
| Rechnungsadresse anzeigen | **True** oder **False** | Wenn diese Eigenschaft auf **True** gesetzt ist, wird die Rechnungsadresse von Adyen im Zahlungsmodul iFrame bereitgestellt. Wenn sie auf **False** eingestellt ist, wird die Rechnungsadresse nicht von Adyen bereitgestellt, und ein Commerce-Benutzer muss ein Modul konfigurieren, um die Rechnungsadresse auf der Checkout-Seite anzuzeigen. |
| Zahlungsstil überschreiben | Cascading Style Sheets (CSS)-Code | Da das Zahlungsmodul in einem IFrame gehostet wird, sind die Styling-Funktionen eingeschränkt. Mit dieser Eigenschaft können Sie ein gewisses Maß an Styling erzielen. Um Site-Stile zu überschreiben, müssen Sie den CSS-Code als Wert dieser Eigenschaft einfügen. Site Builder CSS-Überschreibungen und Stile gelten nicht für dieses Modul. |

## <a name="billing-address"></a>Rechnungsadresse

Mit dem Zahlungsmodul können Debitoren eine Rechnungsadresse für ihre Zahlungsinformationen angeben. Außerdem können sie ihre Lieferadresse als Rechnungsadresse verwenden, um den Checkout-Flow einfacher und schneller zu gestalten. Wenn die Eigenschaft **Rechnungsadresse anzeigen** auf **False** gesetzt ist, sollte das Zahlungsmodul auf der Checkout-Seite konfiguriert werden.

## <a name="add-a-payment-module-to-a-checkout-page-and-set-the-required-properties"></a>Einer Checkout-Seite ein Zahlungsmodul hinzufügen, und die benötigten Eigenschaften einrichten

Ein Zahlungsmodul kann nur zu einem Checkout-Modul hinzugefügt werden. Weitere Informationen zum Konfigurieren eines Zahlungsmoduls für eine Checkout-Seite erhalten Sie unter [Checkout-Modul](add-checkout-module.md).

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Einkaufswagenmodul](add-cart-module.md)

[Modul für Einkaufswagensymbol](cart-icon-module.md)

[Auschecken-Modul](add-checkout-module.md)

[Versandadressmodul](ship-address-module.md)

[Lieferoptionsmodul](delivery-options-module.md)

[Auftragsdetailmodul](order-confirmation-module.md)

[Geschenkkartenmodul](add-giftcard.md)

[Zahlungskonnektor von Dynamics 365 für Adyen](dev-itpro/adyen-connector.md)

[Starke Kundenauthentifizierung mit dem Adyen-Konnektor](adyen_redirect.md)
