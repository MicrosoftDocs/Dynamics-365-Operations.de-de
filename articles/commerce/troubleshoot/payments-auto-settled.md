---
title: Zahlungen werden automatisch abgerechnet, bevor Aufträge fakturiert oder versendet werden
description: Dieses Thema enthält Anleitungen zur Fehlerbehebung, die hilfreich sein können, wenn eine Zahlung unmittelbar nach Auftragserteilung im Adyen-Portal abgerechnet wird, obwohl der Auftrag nicht fakturiert oder versendet wurde.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
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
ms.openlocfilehash: 43fe90cf99ddbe42dc89685e7fc747ded5a285c0
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801650"
---
# <a name="payments-are-automatically-settled-before-orders-are-invoiced-or-shipped"></a><span data-ttu-id="fa5ce-103">Zahlungen werden automatisch abgerechnet, bevor Aufträge fakturiert oder versendet werden</span><span class="sxs-lookup"><span data-stu-id="fa5ce-103">Payments are automatically settled before orders are invoiced or shipped</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fa5ce-104">Dieses Thema enthält Anleitungen zur Fehlerbehebung, die hilfreich sein können, wenn eine Zahlung unmittelbar nach Auftragserteilung im Adyen-Portal abgerechnet wird, obwohl der Auftrag nicht fakturiert oder versendet wurde.</span><span class="sxs-lookup"><span data-stu-id="fa5ce-104">This topic provides troubleshooting guidance that can help when a payment is settled in the Adyen portal immediately after an order is placed, even though the sales order hasn't been invoiced or shipped.</span></span>

## <a name="description"></a><span data-ttu-id="fa5ce-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fa5ce-105">Description</span></span>

<span data-ttu-id="fa5ce-106">Nach Erteilung eines Auftrags wird die Zahlung sofort im Adyen-Portal abgerechnet, obwohl der Auftrag nicht fakturiert oder versendet wurde.</span><span class="sxs-lookup"><span data-stu-id="fa5ce-106">After an order is placed, the payment is immediately settled in the Adyen portal, even though the sales order hasn't been invoiced or shipped.</span></span>

## <a name="resolution"></a><span data-ttu-id="fa5ce-107">Lösung</span><span class="sxs-lookup"><span data-stu-id="fa5ce-107">Resolution</span></span>

### <a name="configure-manual-capture-for-e-commerce-payments-in-the-adyen-portal"></a><span data-ttu-id="fa5ce-108">Die manuelle Erfassung für E-Commerce-Zahlungen im Adyen-Portal konfigurieren</span><span class="sxs-lookup"><span data-stu-id="fa5ce-108">Configure manual capture for e-commerce payments in the Adyen portal</span></span>

<span data-ttu-id="fa5ce-109">Befolgen Sie diese Schritte, um die manuelle Erfassung für E-Commerce-Zahlungen im Adyen-Portal zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="fa5ce-109">To configure manual capture for e-commerce payments in the Adyen portal, follow these steps.</span></span>

1. <span data-ttu-id="fa5ce-110">Melden Sie sich beim Adyen-Portal an.</span><span class="sxs-lookup"><span data-stu-id="fa5ce-110">Sign in to the Adyen portal.</span></span>
1. <span data-ttu-id="fa5ce-111">Wählen Sie in der oberen rechten Ecke Ihr Händlerkonto für den E-Commerce-Kanal aus.</span><span class="sxs-lookup"><span data-stu-id="fa5ce-111">In the upper-right corner, select your merchant account for the e-commerce channel.</span></span>
1. <span data-ttu-id="fa5ce-112">Wählen Sie in der oberen Navigationsleiste **Konto** und dann **Einstellungen** aus.</span><span class="sxs-lookup"><span data-stu-id="fa5ce-112">On the top navigation, select **Account**, and then select **Settings**.</span></span>
1. <span data-ttu-id="fa5ce-113">Wählen Sie im Feld **Verzögerung erfassen** die Option **Manuell** aus.</span><span class="sxs-lookup"><span data-stu-id="fa5ce-113">In the **Capture Delay** field, select **manual**.</span></span>

    ![„Verzögerung erfassen“-Einstellung im Adyen-Portal](media/adyen-capture-delay.jpg)

## <a name="additional-resources"></a><span data-ttu-id="fa5ce-115">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="fa5ce-115">Additional resources</span></span>

[<span data-ttu-id="fa5ce-116">Adyen-Zahlungserfassung</span><span class="sxs-lookup"><span data-stu-id="fa5ce-116">Adyen payment capture</span></span>](https://docs.adyen.com/point-of-sale/capturing-payments)

[<span data-ttu-id="fa5ce-117">Zahlungskonnektor von Dynamics 365 für Adyen</span><span class="sxs-lookup"><span data-stu-id="fa5ce-117">Dynamics 365 Payment Connector for Adyen</span></span>](../dev-itpro/adyen-connector.md)

[<span data-ttu-id="fa5ce-118">Adyen-Zahlungskonnektor für Dynamics 365 einrichten</span><span class="sxs-lookup"><span data-stu-id="fa5ce-118">Set up the Adyen payment connector for Dynamics 365</span></span>](https://docs.adyen.com/plugins/microsoft-dynamics)
