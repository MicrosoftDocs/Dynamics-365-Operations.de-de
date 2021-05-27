---
title: Auf der Kreditkarten-Eingabeseite wird beim Auschecken ein Fehler angezeigt
description: Dieses Thema enthält Anleitungen zur Problembehandlung, die hilfreich sein können, wenn der Abschnitt zur Zahlungsmethode nicht geladen wird und eine Fehlermeldung angezeigt wird.
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
ms.openlocfilehash: ea9105481e6c5812565f0d3604906c905bcb5443
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018505"
---
# <a name="credit-card-entry-page-shows-an-error-at-checkout"></a><span data-ttu-id="38a2a-103">Auf der Kreditkarten-Eingabeseite wird beim Auschecken ein Fehler angezeigt</span><span class="sxs-lookup"><span data-stu-id="38a2a-103">Credit card entry page shows an error at checkout</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="38a2a-104">Dieses Thema enthält Anleitungen zur Problembehandlung, die hilfreich sein können, wenn der Abschnitt **Zahlungsmethode** nicht geladen wird und eine Fehlermeldung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="38a2a-104">This topic provides troubleshooting guidance that can help when the **Payment method** section isn't loaded and shows an error message.</span></span>

## <a name="description"></a><span data-ttu-id="38a2a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="38a2a-105">Description</span></span>

<span data-ttu-id="38a2a-106">Wenn Sie die Checkout-Seite eines Onlineshops öffnen, wird der Abschnitt **Zahlungsmethode** nicht geladen und die folgende Fehlermeldung wird angezeigt: „Es ist ein Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="38a2a-106">When you open the checkout page of an online store, the **Payment method** section isn't loaded, and the following error message is shown: "Something went wrong.</span></span> <span data-ttu-id="38a2a-107">Bitte versuchen Sie es später erneut.“</span><span class="sxs-lookup"><span data-stu-id="38a2a-107">Please try again later."</span></span>

![Zahlungsmodulfehler](media/payment-module-error.jpg)

## <a name="resolution"></a><span data-ttu-id="38a2a-109">Lösung</span><span class="sxs-lookup"><span data-stu-id="38a2a-109">Resolution</span></span>

### <a name="wait-for-the-commerce-scale-unit-cache-to-expire"></a><span data-ttu-id="38a2a-110">Warten, bis der Commerce Scale Unit-Cache abgelaufen ist</span><span class="sxs-lookup"><span data-stu-id="38a2a-110">Wait for the Commerce Scale Unit cache to expire</span></span>

<span data-ttu-id="38a2a-111">Die Einstellungen für den Zahlungsdienst auf der Checkout-Seite des Onlineshops werden in der Commerce Scale Unit zwischengespeichert und können bis zu 15 Minuten brauchen, bis sie auf der E-Commerce-Website angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="38a2a-111">The payment service settings on the online store's checkout page are cached on the Commerce Scale Unit and can take up to 15 minutes to appear on the e-commerce site.</span></span> <span data-ttu-id="38a2a-112">Diese Zahlungsdiensteinstellungen umfassen Änderungen an der Händlerkonto-ID, dem Cloud-API-Schlüssel und verschiedenen Konfigurationseinstellungen, die sich auf die Zahlungsmethode beziehen.</span><span class="sxs-lookup"><span data-stu-id="38a2a-112">These payment service settings include changes to the merchant account ID, cloud API key, and various configuration settings that are related to the payment method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="38a2a-113">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="38a2a-113">Additional resources</span></span>

[<span data-ttu-id="38a2a-114">Einen Onlinechannel einrichten</span><span class="sxs-lookup"><span data-stu-id="38a2a-114">Set up an online channel</span></span>](../channel-setup-online.md)
