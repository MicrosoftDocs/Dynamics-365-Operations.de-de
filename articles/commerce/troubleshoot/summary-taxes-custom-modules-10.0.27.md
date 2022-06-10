---
title: Die Zwischensumme der Bestellzusammenfassung enthält keine Steuern auf Belastungen, wenn Sie angepasste Module für die Bestellzusammenfassung verwenden.
description: Dieses Thema enthält Hinweise zur Problembehandlung, die Ihnen helfen können, wenn Sie angepasste Module für die Bestellzusammenfassung verwenden und die Zwischensumme der Bestellzusammenfassung keine Steuern auf Belastungen im Szenario „Preis enthält Mehrwertsteuer“ enthält.
author: gvrmohanreddy
ms.date: 05/17/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-04-22
ms.openlocfilehash: 1a47561a3ac984bc554b5b93546592237c16cf18
ms.sourcegitcommit: 48d094d083c1bd45c3d72f8b666926b48ec7ae35
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/18/2022
ms.locfileid: "8767965"
---
# <a name="order-summary-subtotal-doesnt-include-taxes-on-charges-when-using-customized-order-summary-modules"></a>Die Zwischensumme der Bestellzusammenfassung enthält keine Steuern auf Belastungen, wenn Sie angepasste Module für die Bestellzusammenfassung verwenden.

Dieses Thema enthält Hinweise zur Problembehandlung, die Ihnen helfen können, wenn Sie angepasste Module für die Bestellzusammenfassung verwenden und die Zwischensumme der Bestellzusammenfassung keine Steuern auf Belastungen im Szenario „Preis enthält Mehrwertsteuer“ enthält.

## <a name="description"></a>Description

Mit der Version Microsoft Dynamics 365 Commerce 10.0.27 wurden die folgenden Änderungen am Szenario „Preis enthält Mehrwertsteuer“ vorgenommen, um eine konsistente Erfahrung in den Modulen für die Bestellzusammenfassung auf allen E-Commerce-Seiten zu gewährleisten.

- Es wurden zwei neue Felder hinzugefügt: **TaxOnShippingCharge** und **TaxOnNonShippingCharges**.
- Die Anwendungsprogrammierschnittstellen (APIs) **GetSalesOrderBySalesId** und **GetSalesOrderByTransactionId** haben genaue Werte für die folgenden Felder im Szenario „Preis enthält Mehrwertsteuer“:

    - SubtotalSalesAmount
    - SubtotalAmountWithoutTax
    - SubtotalAmount
    - ShippingChargeAmount
    - OtherChargeAmount

Wenn Sie jedoch angepasste Module für die Bestellungszusammenfassung verwenden, können sich diese Änderungen auf die Zwischensummenwerte der Bestellungszusammenfassung auswirken, da Steuern auf Belastungen nicht berücksichtigt werden.

## <a name="resolution"></a>Lösung

Wenn Sie angepasste Module für die Zusammenfassung von Bestellungen verwenden und die Änderungen am Szenario „Preis enthält Mehrwertsteuer“ in Commerce Version 10.0.27 und höher nicht übernehmen möchten, folgen Sie den Anweisungen in diesem Abschnitt.

Durch die Rückkehr zum früheren (vor Version 10.0.27) Verhalten der **Verkaufsvorgang.SubtotalAmount** und **Verkaufsvorgang. SubtotalAmountWithoutTax** stellen Sie die Einbeziehung des Gesamtsteuerbetrags der Gebühren (**TaxOnShippingCharge** und **TaxOnNonShippingCharges**) in die Zwischensummen (**SubtotalAmount** und **SubtotalAmountWithoutTax**) wieder her.

Gehen Sie wie folgt vor, um zum vorherigen Verhalten der Bestellzusammenfassung zurückzukehren.

1. In der Commerce Headquarters öffnen Sie die Seite Commerce-Parameter (**Einzelhandel und Commerce \> Einrichtung der Zentralverwaltung \> Parameter \> Commerce-Parameter**).
1. Wählen Sie im linken Navigationsbereich **Konfigurationsparameter**.
1. Fügen Sie die folgenden Konfigurationsparameter hinzu und legen Sie den Wert für jeden Parameter auf **wahr** fest:

    - IsLegacyTaxOnChargeInSubtotalAmountIncludedInTaxIncusiveEnabled
    - IsLegacyOrderSummaryHydrationEnabled

> [!NOTE]
> Wenn Sie zuvor den Konfigurationsparameter **IsUpdatedPriceIncludesTaxSubtotalCalculationEnabled** verwendet haben und dasselbe Verhalten für die Eigenschaft **order.NetAmountWithoutTax** beibehalten möchten, sollten Sie auch den Konfigurationsparameter **IsLegacyPriceIncludesTaxNetAmountWithoutTaxCalculationEnabled** hinzufügen und seinen Wert auf **True** festlegen.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Informationen zur Steueraufteilung in Bestellzusammenfassungen ausblenden](../hide-taxes-breakup.md)
