---
title: Auf der Kreditkarten-Eingabeseite wird beim Auschecken ein Fehler angezeigt
description: Dieses Thema enthält Anleitungen zur Problembehandlung, die hilfreich sein können, wenn der Abschnitt zur Zahlungsmethode nicht geladen wird und eine Fehlermeldung angezeigt wird.
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
ms.openlocfilehash: d2c5f01d17df79c9b23fd513aaeb5c0605d657e9
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801770"
---
# <a name="credit-card-entry-page-shows-an-error-at-checkout"></a><span data-ttu-id="26b2b-103">Auf der Kreditkarten-Eingabeseite wird beim Auschecken ein Fehler angezeigt</span><span class="sxs-lookup"><span data-stu-id="26b2b-103">Credit card entry page shows an error at checkout</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="26b2b-104">Dieses Thema enthält Anleitungen zur Problembehandlung, die hilfreich sein können, wenn der Abschnitt **Zahlungsmethode** nicht geladen wird und eine Fehlermeldung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="26b2b-104">This topic provides troubleshooting guidance that can help when the **Payment method** section isn't loaded and shows an error message.</span></span>

## <a name="description"></a><span data-ttu-id="26b2b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="26b2b-105">Description</span></span>

<span data-ttu-id="26b2b-106">Wenn Sie die Checkout-Seite eines Onlineshops öffnen, wird der Abschnitt **Zahlungsmethode** nicht geladen und die folgende Fehlermeldung wird angezeigt: „Es ist ein Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="26b2b-106">When you open the checkout page of an online store, the **Payment method** section isn't loaded, and the following error message is shown: "Something went wrong.</span></span> <span data-ttu-id="26b2b-107">Bitte versuchen Sie es später erneut.“</span><span class="sxs-lookup"><span data-stu-id="26b2b-107">Please try again later."</span></span>

![Zahlungsmodulfehler](media/payment-module-error.jpg)

## <a name="resolution"></a><span data-ttu-id="26b2b-109">Lösung</span><span class="sxs-lookup"><span data-stu-id="26b2b-109">Resolution</span></span>

### <a name="wait-for-the-commerce-scale-unit-cache-to-expire"></a><span data-ttu-id="26b2b-110">Warten, bis der Commerce Scale Unit-Cache abgelaufen ist</span><span class="sxs-lookup"><span data-stu-id="26b2b-110">Wait for the Commerce Scale Unit cache to expire</span></span>

<span data-ttu-id="26b2b-111">Die Einstellungen für den Zahlungsdienst auf der Checkout-Seite des Onlineshops werden in der Commerce Scale Unit zwischengespeichert und können bis zu 15 Minuten brauchen, bis sie auf der E-Commerce-Website angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="26b2b-111">The payment service settings on the online store's checkout page are cached on the Commerce Scale Unit and can take up to 15 minutes to appear on the e-commerce site.</span></span> <span data-ttu-id="26b2b-112">Diese Zahlungsdiensteinstellungen umfassen Änderungen an der Händlerkonto-ID, dem Cloud-API-Schlüssel und verschiedenen Konfigurationseinstellungen, die sich auf die Zahlungsmethode beziehen.</span><span class="sxs-lookup"><span data-stu-id="26b2b-112">These payment service settings include changes to the merchant account ID, cloud API key, and various configuration settings that are related to the payment method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="26b2b-113">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="26b2b-113">Additional resources</span></span>

[<span data-ttu-id="26b2b-114">Einen Onlinechannel einrichten</span><span class="sxs-lookup"><span data-stu-id="26b2b-114">Set up an online channel</span></span>](../channel-setup-online.md)
