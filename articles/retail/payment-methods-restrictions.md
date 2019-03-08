---
title: Zahlungsmethoden für Retouren ohne Beleg beschränken
description: In diesem Thema wird beschrieben, wie bestimmte Zahlungsarten für die Rückerstattung eingeschränkt werden können, wenn die Rücksendung ohne Beleg erfolgt.
author: rapraj
manager: AnnBe
ms.date: 01/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTenderTypeTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15831
ms.assetid: 465893a5-6b4f-4c5f-b305-db071df2d33f
ms.search.region: global
ms.search.industry: Retail
ms.author: yabinl
ms.search.validFrom: 2019-02-01
ms.dyn365.ops.version: AX 10.0.0, Retail Feb 2019 update
ms.openlocfilehash: 1f84a6382453c0ba7540e618ad90ae1d3c684a2b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "315911"
---
# <a name="restrict-payment-methods-for-returns-without-a-receipt"></a><span data-ttu-id="526df-103">Zahlungsmethoden für Retouren ohne Beleg beschränken</span><span class="sxs-lookup"><span data-stu-id="526df-103">Restrict payment methods for returns without a receipt</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="526df-104">Jeder Zahlungstyp, der von einem Einzelhändler akzeptiert wird, muss beim Einrichten des Systems konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="526df-104">Each payment type that a retailer accepts must be configured when the system is set up.</span></span> <span data-ttu-id="526df-105">In diesem Thema wird beschrieben, wie bestimmte Zahlungsarten für die Rückerstattung eingeschränkt werden können, wenn die Rücksendung ohne Beleg erfolgt.</span><span class="sxs-lookup"><span data-stu-id="526df-105">This topic describes how certain payment types can be restricted for refund if the returns are made without a receipt.</span></span>

## <a name="set-up-payment-methods"></a><span data-ttu-id="526df-106">Einrichten von Zahlungsmethoden</span><span class="sxs-lookup"><span data-stu-id="526df-106">Set up payment methods</span></span>

<span data-ttu-id="526df-107">Zum Einrichten von Zahlungsmethoden müssen die folgenden Aufgaben abgeschlossen sein.</span><span class="sxs-lookup"><span data-stu-id="526df-107">To set up payment methods, the following tasks must be completed.</span></span>
1. <span data-ttu-id="526df-108">Erstellen Sie die Zahlungsmethoden, die von der gesamten Organisation akzeptiert werden.</span><span class="sxs-lookup"><span data-stu-id="526df-108">Create the payment methods that are accepted by the entire organization.</span></span>
2. <span data-ttu-id="526df-109">Einrichten von organisationsweiten Kartentypen und Kartennummern</span><span class="sxs-lookup"><span data-stu-id="526df-109">Create organization-wide card types and card numbers.</span></span> <span data-ttu-id="526df-110">Wenn Kredit- oder Debitkarten akzeptiert werden, müssen Sie eine Zahlungsmethode für Karten und anschließend die organisationsweiten Kartentypen und Kartennummern erstellen.</span><span class="sxs-lookup"><span data-stu-id="526df-110">If credit cards or debit cards are accepted, you must create one payment method for cards, and then create the organization-wide card types and card numbers.</span></span>
3. <span data-ttu-id="526df-111">Einrichten von Shopzahlungsmethoden.</span><span class="sxs-lookup"><span data-stu-id="526df-111">Set up store payment methods.</span></span> <span data-ttu-id="526df-112">Ordnen Sie die Zahlungsmethoden den einzelnen Shops zu, und geben Sie dann für jede Zahlungsmethode shopspezifische Einstellungen ein.</span><span class="sxs-lookup"><span data-stu-id="526df-112">Associate payment methods with each store, and then enter the store-specific settings for each payment method.</span></span>
4. <span data-ttu-id="526df-113">Einrichten von Kartenzahlungsmethoden für Shops</span><span class="sxs-lookup"><span data-stu-id="526df-113">Set up card payment methods for stores.</span></span> <span data-ttu-id="526df-114">Schließen Sie für alle Zahlungsmittel vom Typ "Karte", die im Shop akzeptiert werden, die Karteneinrichtung ab.</span><span class="sxs-lookup"><span data-stu-id="526df-114">For any card payment methods that the store accepts, complete the card setup.</span></span>

<span data-ttu-id="526df-115">![Einzelhandelsshop-Setup](media/NoReceiptReturns1.png "Einzelhandelsshop-Setup")</span><span class="sxs-lookup"><span data-stu-id="526df-115">![Retail Store Setup](media/NoReceiptReturns1.png "Retail Store Setup")</span></span> 


## <a name="restrict-payment-methods-for-returns-without-a-receipt"></a><span data-ttu-id="526df-116">Zahlungsmethoden für Retouren ohne Beleg beschränken</span><span class="sxs-lookup"><span data-stu-id="526df-116">Restrict payment methods for returns without a receipt</span></span>

<span data-ttu-id="526df-117">Setzen Sie für jede Shop-Zahlungsmethode auf der Seite **Einzelhandelsshopleitung** unter **Retouren ohne Beleg** **Beschränkung für Rückerstattungen ohne Beleg** auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="526df-117">For each store payment method, on the **Retail store management** page, under **Non receipt returns**, set **Restrict for refunds without receipt** to **Yes**.</span></span> 

<span data-ttu-id="526df-118">Der Standardwert des Umschalters ist **Nein**, wodurch sichergestellt wird, dass der Zahlweg für Rückerstattungen zugelassen wird.</span><span class="sxs-lookup"><span data-stu-id="526df-118">The default value of the toggle is **No**, which ensures that the payment method is allowed for refunds.</span></span> 

<span data-ttu-id="526df-119">Wenn **Beschränkung für Rückerstattungen ohne Beleg** auf **Ja** gesetzt ist, wird die gewählte Zahlungsmethode für Rückerstattungen nicht zugelassen.</span><span class="sxs-lookup"><span data-stu-id="526df-119">When **Restrict for refunds without receipt** is set to **Yes**, the selected payment method will not be allowed for refunds.</span></span> 

<span data-ttu-id="526df-120">![Zahlungsmethode im Einzelhandel](media/NoReceiptReturns3.png "Zahlungsmethode im Einzelhandel")</span><span class="sxs-lookup"><span data-stu-id="526df-120">![Retail Store payment method](media/NoReceiptReturns3.png "Retail Store Payment Method")</span></span> 

> [!NOTE]
> <span data-ttu-id="526df-121">Wenn ein Kassierer eine Zahlungsmethode auswählt, die ohne Beleg für die Rückerstattung eingeschränkt ist, wird eine Meldung angezeigt, um die zulässigen Zahlungsmethoden zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="526df-121">When a cashier selects a payment method that is restricted for refund without a receipt, a message displays to verify the acceptable payment methods.</span></span>

<span data-ttu-id="526df-122">![Akzeptierte Zahlungsmethoden](media/NoReceiptReturns4.png "Akzeptierte Zahlungsmethoden")</span><span class="sxs-lookup"><span data-stu-id="526df-122">![Acceptable payment methods](media/NoReceiptReturns4.png "Acceptable payment methods")</span></span> 

<span data-ttu-id="526df-123">Wenn eine Transaktion sowohl eine quittierte Rücksendung als auch eine Rücksendung ohne Beleg hat, werden die Einschränkungsbedingungen nicht durchgesetzt, da es sich bei der Transaktion um einen Rückgabe-Workflow mit Beleg handelt.</span><span class="sxs-lookup"><span data-stu-id="526df-123">If a transaction has both a receipted return and a return without a receipt, the restriction conditions will not be enforced because the transaction will be a return workflow with a receipt.</span></span> 

