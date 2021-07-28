---
title: Die Abholoption wird nicht auf der Warenkorbseite oder den Produktdetailseiten angezeigt
description: Dieses Thema enthält Anleitungen zur Fehlerbehebung, die hilfreich sein können, wenn die Option für die Shop-Abholung nicht auf der Warenkorbseite oder den Produktdetailseiten angezeigt wird.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 3dd4eb576f234e4d75c08b0b5e2fe967500c8c93
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6347295"
---
# <a name="pick-this-up-option-doesnt-appear-on-cart-or-product-details-pages"></a>Die Option „Abholung“ wird nicht auf der Warenkorbseite oder den Produktdetailseiten angezeigt

[!include [banner](../../includes/banner.md)]

Dieses Thema enthält Anleitungen zur Fehlerbehebung, die hilfreich sein können, wenn die Option für die Shop-Abholung nicht auf der Warenkorbseite oder den Produktdetailseiten angezeigt wird.

## <a name="description"></a>Beschreibung

Die Schaltfläche **Abholung** wird nicht auf der Warenkorbseite oder den Produktdetailseiten angezeigt.

Die folgende Abbildung zeigt ein Beispiel für eine Seite, die über die Schaltfläche **Abholung** verfügt.

![„Abholung“-Schaltfläche.](media/pickup-button-missing.jpg)

## <a name="resolution"></a>Lösung

### <a name="enable-the-bopis-extension-in-commerce-site-builder"></a>BOPIS-Erweiterung im Commerce-Website-Generator aktivieren

Führen Sie die folgenden Schritte aus, um die Erweiterung „Online kaufen, im Shop abholen“ (Buy Online, Pick Up In Store, BOPIS) im Commerce-Website-Generator zu aktivieren.

1. Wählen Sie die Website aus.
1. Wählen Sie **Site-Einstellungen** und anschließend **Erweiterungen** aus.
1. Vergewissern Sie sich, dass die Option **BOPIS deaktivieren** deaktiviert ist.

### <a name="configure-modes-of-delivery-in-commerce-headquarters"></a>Lieferarten in der Commerce-Zentralverwaltung konfigurieren

Befolgen Sie diese Schritte, um die Lieferarten in der Commerce-Zentralverwaltung zu konfigurieren.

1. Rufen Sie **Beschaffung \> Einrichtung \> Lieferarten** auf.
1. Stellen Sie sicher, dass die Lieferart **Debitorenabholung** erstellt ist und ihr Produkte und Adressen zugewiesen wurden.
1. Rufen Sie **Retail und Commerce \> Zentralverwaltungseinrichtung \> Parameter** auf.
1. Wählen Sie im linken Navigationsbereich die Option **Debitorenaufträge** aus.
1. Vergewissern Sie sich, dass **Abhollieferart** richtig konfiguriert ist.

### <a name="configure-customer-orders-payments"></a>Zahlungen für Debitorenaufträge konfigurieren

Befolgen Sie diese Schritte, um Zahlungen für Debitorenaufträge in der Commerce-Zentralverwaltung zu konfigurieren.

1. Rufen Sie **Retail und Commerce \> Zentralverwaltungseinrichtung \> Parameter** auf.
1. Wählen Sie im linken Navigationsbereich die Option **Debitorenaufträge** aus.
1. Überprüfen Sie, ob im Inforegister **Zahlungen** die Felder **Zahlungsbedingungen** und **Zahlungsart** korrekt eingestellt sind.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[BOPIS konfigurieren](../cpe-bopis.md)

[Mehrere Lieferarten zur Abholung für Kundenaufträge](../multiple-pickup-modes.md)

[Omnichannel-Commerce-Auftragszahlungen](../dev-itpro/commerce-payments.md)

[Shopauswahlmodul](../store-selector.md)
