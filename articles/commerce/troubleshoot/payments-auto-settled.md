---
title: Zahlungen werden automatisch abgerechnet, bevor Aufträge fakturiert oder versendet werden
description: Dieses Thema enthält Anleitungen zur Fehlerbehebung, die hilfreich sein können, wenn eine Zahlung unmittelbar nach Auftragserteilung im Adyen-Portal abgerechnet wird, obwohl der Auftrag nicht fakturiert oder versendet wurde.
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
ms.openlocfilehash: b4fd37a3c45f2559c9659f072ca0b6f02e712f53
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018259"
---
# <a name="payments-are-automatically-settled-before-orders-are-invoiced-or-shipped"></a><span data-ttu-id="40310-103">Zahlungen werden automatisch abgerechnet, bevor Aufträge fakturiert oder versendet werden</span><span class="sxs-lookup"><span data-stu-id="40310-103">Payments are automatically settled before orders are invoiced or shipped</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="40310-104">Dieses Thema enthält Anleitungen zur Fehlerbehebung, die hilfreich sein können, wenn eine Zahlung unmittelbar nach Auftragserteilung im Adyen-Portal abgerechnet wird, obwohl der Auftrag nicht fakturiert oder versendet wurde.</span><span class="sxs-lookup"><span data-stu-id="40310-104">This topic provides troubleshooting guidance that can help when a payment is settled in the Adyen portal immediately after an order is placed, even though the sales order hasn't been invoiced or shipped.</span></span>

## <a name="description"></a><span data-ttu-id="40310-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="40310-105">Description</span></span>

<span data-ttu-id="40310-106">Nach Erteilung eines Auftrags wird die Zahlung sofort im Adyen-Portal abgerechnet, obwohl der Auftrag nicht fakturiert oder versendet wurde.</span><span class="sxs-lookup"><span data-stu-id="40310-106">After an order is placed, the payment is immediately settled in the Adyen portal, even though the sales order hasn't been invoiced or shipped.</span></span>

## <a name="resolution"></a><span data-ttu-id="40310-107">Lösung</span><span class="sxs-lookup"><span data-stu-id="40310-107">Resolution</span></span>

### <a name="configure-manual-capture-for-e-commerce-payments-in-the-adyen-portal"></a><span data-ttu-id="40310-108">Die manuelle Erfassung für E-Commerce-Zahlungen im Adyen-Portal konfigurieren</span><span class="sxs-lookup"><span data-stu-id="40310-108">Configure manual capture for e-commerce payments in the Adyen portal</span></span>

<span data-ttu-id="40310-109">Befolgen Sie diese Schritte, um die manuelle Erfassung für E-Commerce-Zahlungen im Adyen-Portal zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="40310-109">To configure manual capture for e-commerce payments in the Adyen portal, follow these steps.</span></span>

1. <span data-ttu-id="40310-110">Melden Sie sich beim Adyen-Portal an.</span><span class="sxs-lookup"><span data-stu-id="40310-110">Sign in to the Adyen portal.</span></span>
1. <span data-ttu-id="40310-111">Wählen Sie in der oberen rechten Ecke Ihr Händlerkonto für den E-Commerce-Kanal aus.</span><span class="sxs-lookup"><span data-stu-id="40310-111">In the upper-right corner, select your merchant account for the e-commerce channel.</span></span>
1. <span data-ttu-id="40310-112">Wählen Sie in der oberen Navigationsleiste **Konto** und dann **Einstellungen** aus.</span><span class="sxs-lookup"><span data-stu-id="40310-112">On the top navigation, select **Account**, and then select **Settings**.</span></span>
1. <span data-ttu-id="40310-113">Wählen Sie im Feld **Verzögerung erfassen** die Option **Manuell** aus.</span><span class="sxs-lookup"><span data-stu-id="40310-113">In the **Capture Delay** field, select **manual**.</span></span>

    ![„Verzögerung erfassen“-Einstellung im Adyen-Portal](media/adyen-capture-delay.jpg)

## <a name="additional-resources"></a><span data-ttu-id="40310-115">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="40310-115">Additional resources</span></span>

[<span data-ttu-id="40310-116">Adyen-Zahlungserfassung</span><span class="sxs-lookup"><span data-stu-id="40310-116">Adyen payment capture</span></span>](https://docs.adyen.com/point-of-sale/capturing-payments)

[<span data-ttu-id="40310-117">Zahlungskonnektor von Dynamics 365 für Adyen</span><span class="sxs-lookup"><span data-stu-id="40310-117">Dynamics 365 Payment Connector for Adyen</span></span>](../dev-itpro/adyen-connector.md)

[<span data-ttu-id="40310-118">Adyen-Zahlungskonnektor für Dynamics 365 einrichten</span><span class="sxs-lookup"><span data-stu-id="40310-118">Set up the Adyen payment connector for Dynamics 365</span></span>](https://docs.adyen.com/plugins/microsoft-dynamics)
