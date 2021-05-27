---
title: Die Option „Für meine nächste Zahlung speichern“ wird nicht angezeigt
description: Dieses Thema enthält Anleitungen zur Fehlerbehebung, die hilfreich sein können, wenn das Kontrollkästchen „Für meine nächste Zahlung speichern“ auf der Checkout-Seite einer E-Commerce-Website nicht unter Zahlungsmethode angezeigt wird.
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
ms.openlocfilehash: af19a3abd78d543d82f7a8d017e2dc413115a6d8
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018433"
---
# <a name="save-for-my-next-payment-option-doesnt-appear"></a><span data-ttu-id="e6caf-103">Die Option „Für meine nächste Zahlung speichern“ wird nicht angezeigt</span><span class="sxs-lookup"><span data-stu-id="e6caf-103">"Save for my next payment" option doesn't appear</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e6caf-104">Dieses Thema enthält Anleitungen zur Fehlerbehebung, die hilfreich sein können, wenn das Kontrollkästchen **Für meine nächste Zahlung speichern** auf der Checkout-Seite einer E-Commerce-Website nicht unter **Zahlungsmethode** angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="e6caf-104">This topic provides troubleshooting guidance that can help when the **Save for my next payment** check box doesn't appear under **Payment method** on an e-commerce site's checkout page.</span></span>

## <a name="description"></a><span data-ttu-id="e6caf-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e6caf-105">Description</span></span>

<span data-ttu-id="e6caf-106">Das Kontrollkästchen **Für meine nächste Zahlung speichern** wird nicht im Abschnitt **Zahlungsmethode** auf der Checkout-Seite einer E-Commerce-Website angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e6caf-106">The **Save for my next payment** check box doesn't appear in the **Payment method** section on an e-commerce site's checkout page.</span></span>

<span data-ttu-id="e6caf-107">Die folgende Abbildung zeigt ein Beispiel für eine Checkout-Seite, die das Kontrollkästchen **Für meine nächste Zahlung speichern** enthält.</span><span class="sxs-lookup"><span data-stu-id="e6caf-107">The following illustration shows an example of a checkout page that includes the **Save for my next payment** check box.</span></span>

![Kontrollkästchen „Für meine nächste Zahlung speichern“ im Zahlungsmodul](media/payment-module-save-payment.jpg)

## <a name="resolution"></a><span data-ttu-id="e6caf-109">Lösung</span><span class="sxs-lookup"><span data-stu-id="e6caf-109">Resolution</span></span>

### <a name="verify-that-the-dynamics-365-payment-connector-for-adyen-is-correctly-configured-in-commerce-headquarters"></a><span data-ttu-id="e6caf-110">Sicherstellen, dass der Dynamics 365 Payment Connector für Adyen in der Commerce-Zentralverwaltung korrekt konfiguriert ist</span><span class="sxs-lookup"><span data-stu-id="e6caf-110">Verify that the Dynamics 365 Payment Connector for Adyen is correctly configured in Commerce headquarters</span></span>

<span data-ttu-id="e6caf-111">Befolgen Sie diese Schritte, um sicherzustellen, dass der Dynamics 365 Payment Connector für Adyen in der Commerce-Zentralverwaltung korrekt konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="e6caf-111">To verify that the Dynamics 365 Payment Connector for Adyen is correctly configured in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="e6caf-112">Rufen Sie **Retail und Commerce \> Kanäle \> Onlineshops** auf.</span><span class="sxs-lookup"><span data-stu-id="e6caf-112">Go to **Retail and Commerce \> Channels \> Online Stores**.</span></span>
1. <span data-ttu-id="e6caf-113">Wählen Sie den Onlineshop aus.</span><span class="sxs-lookup"><span data-stu-id="e6caf-113">Select the online store.</span></span>
1. <span data-ttu-id="e6caf-114">Vergewissern Sie sich, dass im Inforegister **Zahlungskonten** das Feld **Speichern von Zahlungsinformationen in E-Commerce zulassen** auf **True** gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="e6caf-114">On the **Payment accounts** FastTab, make sure that the **Allow saving payment information in e-commerce** field is set to **True**.</span></span>

![Das Feld „Speichern von Zahlungsinformationen in E-Commerce zulassen“ in der Commerce-Zentralverwaltung](media/payment-connector-save-payment.jpg)

## <a name="additional-resources"></a><span data-ttu-id="e6caf-116">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e6caf-116">Additional resources</span></span>

[<span data-ttu-id="e6caf-117">Zahlungsmodul</span><span class="sxs-lookup"><span data-stu-id="e6caf-117">Payment module</span></span>](../payment-module.md)

[<span data-ttu-id="e6caf-118">Online-Zahlungsmittel mit dem Adyen-Connector speichern</span><span class="sxs-lookup"><span data-stu-id="e6caf-118">Saving online payment instruments with the Adyen connector</span></span>](../dev-itpro/adyen-connector-listPI.md)
