---
title: „Zahlungstyp muss Kreditkarte sein“-Fehler auf der Auftragsseite
description: Dieses Thema enthält Anleitungen zur Fehlerbehebung, die hilfreich sein können, wenn nach der Auftragssynchronisierung auf der Auftragsseite eine Fehlermeldung angezeigt wird.
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
ms.openlocfilehash: 5be19949e9d1dbc43fdd3e6def119effa50a34d0
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018409"
---
# <a name="payment-type-must-be-credit-card-error-on-the-sales-order-page"></a><span data-ttu-id="c3dcb-103">„Zahlungstyp muss Kreditkarte sein“-Fehler auf der Auftragsseite</span><span class="sxs-lookup"><span data-stu-id="c3dcb-103">"Payment type must be credit card" error on the sales order page</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c3dcb-104">Dieses Thema enthält Anleitungen zur Fehlerbehebung, die hilfreich sein können, wenn nach der Auftragssynchronisierung auf der Auftragsseite eine Fehlermeldung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="c3dcb-104">This topic provides troubleshooting guidance that can help when an error message is shown on the sales order page after an order is synced.</span></span>

## <a name="description"></a><span data-ttu-id="c3dcb-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c3dcb-105">Description</span></span>

<span data-ttu-id="c3dcb-106">Wenn Sie nach der Synchronisierung eines Auftrags die Auftragsseite öffnen, wird die folgende Fehlermeldung angezeigt: „Der Zahlungstyp muss Kreditkarte sein, da die Kreditkartennummer angegeben wurde.“</span><span class="sxs-lookup"><span data-stu-id="c3dcb-106">When you open the sales order page after you sync an order, you receive the following error message: "The payment type must be credit card, since the credit card number has been specified."</span></span>

![„Zahlungstyp muss Kreditkarte sein“-Fehler](media/payment-type-must-be-credit-card.jpg)

## <a name="resolution"></a><span data-ttu-id="c3dcb-108">Lösung</span><span class="sxs-lookup"><span data-stu-id="c3dcb-108">Resolution</span></span>

### <a name="set-the-payment-type-in-commerce-headquarters"></a><span data-ttu-id="c3dcb-109">Zahlungstyp in der Commerce-Zentralverwaltung festlegen</span><span class="sxs-lookup"><span data-stu-id="c3dcb-109">Set the payment type in Commerce headquarters</span></span>

1. <span data-ttu-id="c3dcb-110">Rufen Sie **Debitorenkonten \> Zahlungseinstellungen \> Zahlungsbedingungen** auf.</span><span class="sxs-lookup"><span data-stu-id="c3dcb-110">Go to **Accounts receivable \> Payment setup \> Terms of payment**.</span></span>
1. <span data-ttu-id="c3dcb-111">Wählen Sie in der linken Navigation Ihre Zahlungsbedingungen aus.</span><span class="sxs-lookup"><span data-stu-id="c3dcb-111">In the left navigation, select your terms of payment.</span></span>
1. <span data-ttu-id="c3dcb-112">Vergewissern Sie sich, dass im Feld **Zahlungstyp** die Option **Kreditkarte** ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="c3dcb-112">In the **Payment type** field, make sure that **Credit card** is selected.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c3dcb-113">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="c3dcb-113">Additional resources</span></span>

[<span data-ttu-id="c3dcb-114">Onlineverkäufe und -zahlungen buchen</span><span class="sxs-lookup"><span data-stu-id="c3dcb-114">Posting of online sales and payments</span></span>](../tasks/posting-online-sales-payments.md)
