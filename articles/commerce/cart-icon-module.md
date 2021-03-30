---
title: Symbol Einkaufswagenmodul
description: Dieses Thema behandelt das Warenkorbsymbolmodul und es wird beschrieben, wie es Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt wird.
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 43bc274548de016f24569001bac94aff324bea12
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5213233"
---
# <a name="cart-icon-module"></a><span data-ttu-id="feefc-103">Modul für Einkaufswagensymbol</span><span class="sxs-lookup"><span data-stu-id="feefc-103">Cart icon module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="feefc-104">Dieses Thema behandelt das Warenkorbsymbolmodul und es wird beschrieben, wie es Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="feefc-104">This topic covers the cart icon module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="feefc-105">Warenkorbsymbol – Das Warenkorbsymbolmodul im Kopfmodul der Seite zeigt die Anzahl der Artikel im Warenkorb zu einem bestimmten Zeitpunkt an.</span><span class="sxs-lookup"><span data-stu-id="feefc-105">The cart icon module represents the cart in the header module of the page, and shows the number of items in the cart.</span></span> <span data-ttu-id="feefc-106">Das Warenkorbsymbolmodul zeigt auch eine Warenkorbübersicht (auch als Minikorb bezeichnet) an, wenn Sie den Mauszeiger über das Warenkorbsymbol halten.</span><span class="sxs-lookup"><span data-stu-id="feefc-106">The cart icon module also displays a cart summary (also known as a mini cart) when the cart icon is hovered over.</span></span> <span data-ttu-id="feefc-107">Der Mini-Warenkorb bietet dem Benutzer eine Zusammenfassung der Artikel im Warenkorb, ohne zur Warenkorbseite navigieren zu müssen.</span><span class="sxs-lookup"><span data-stu-id="feefc-107">The mini cart provides the user with a summary of the items in the cart without having to navigate to the cart page.</span></span> <span data-ttu-id="feefc-108">Darüber hinaus kann der Benutzer direkt zur Checkout-Seite gehen, wenn er mit der Zusammenfassung zufrieden ist.</span><span class="sxs-lookup"><span data-stu-id="feefc-108">In addition, it also allows the user to directly go to checkout page if they are happy with the summary.</span></span> <span data-ttu-id="feefc-109">Dies reduziert die Anzahl der Seitennavigationen und beschleunigt das Auschecken.</span><span class="sxs-lookup"><span data-stu-id="feefc-109">This reduces the number of page navigations and makes checkout faster.</span></span> 

> [!NOTE]
> <span data-ttu-id="feefc-110">Hilfe für das Modul Warenkorbsymbol finden Sie in Dynamics 365 Commerce Release 10.0.11.</span><span class="sxs-lookup"><span data-stu-id="feefc-110">Support for the cart icon module is available in the Dynamics 365 Commerce 10.0.11 release.</span></span>

<span data-ttu-id="feefc-111">Das folgende Bild zeigt ein Beispiel für ein Warenkorbsymbolmodul, das einen Mini-Wagen in der Fabrikam-Kopfzeile anzeigt.</span><span class="sxs-lookup"><span data-stu-id="feefc-111">The following image shows an example of a cart icon module that displays a mini cart in the Fabrikam header.</span></span>

![Beispiel eines Warenkorbsymbolmoduls](./media/ecommerce-Minicart.PNG)

## <a name="module-properties"></a><span data-ttu-id="feefc-113">Moduleigenschaften</span><span class="sxs-lookup"><span data-stu-id="feefc-113">Module properties</span></span>

- <span data-ttu-id="feefc-114">**Mini-Warenkorb anzeigen** – Wenn true, kann mit dieser Eigenschaft eine Warenkorbübersicht (Mini-Warenkorb) angezeigt werden, wenn Sie den Mauszeiger über das Warenkorbsymbol bewegen.</span><span class="sxs-lookup"><span data-stu-id="feefc-114">**Show mini cart** – When true, this property enables a cart summary (mini cart) to be displayed when the cart icon is hovered over.</span></span> <span data-ttu-id="feefc-115">Diese Funktionalität wird nur für Desktop-Ansichtsports unterstützt.</span><span class="sxs-lookup"><span data-stu-id="feefc-115">This functionality is only supported for desktop view ports.</span></span>

## <a name="add-a-cart-icon-module-to-a-page"></a><span data-ttu-id="feefc-116">Ein Warenkorbsymbolmodul einer Seite hinzufügen</span><span class="sxs-lookup"><span data-stu-id="feefc-116">Add a cart icon module to a page</span></span>

<span data-ttu-id="feefc-117">Informationen zum Hinzufügen eines Warenkorbsymbolmoduls finden Sie unter [Kopf-Modul](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="feefc-117">To add a cart icon module, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="feefc-118">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="feefc-118">Additional resources</span></span>

[<span data-ttu-id="feefc-119">Einkaufswagenmodul</span><span class="sxs-lookup"><span data-stu-id="feefc-119">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="feefc-120">Auschecken-Modul</span><span class="sxs-lookup"><span data-stu-id="feefc-120">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="feefc-121">Zahlungsmodul</span><span class="sxs-lookup"><span data-stu-id="feefc-121">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="feefc-122">Versandadressenmodul</span><span class="sxs-lookup"><span data-stu-id="feefc-122">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="feefc-123">Lieferoptionenmodul</span><span class="sxs-lookup"><span data-stu-id="feefc-123">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="feefc-124">Abholinformationsmodul</span><span class="sxs-lookup"><span data-stu-id="feefc-124">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="feefc-125">Auftragsdetailmodul</span><span class="sxs-lookup"><span data-stu-id="feefc-125">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="feefc-126">Geschenkkartenmodul</span><span class="sxs-lookup"><span data-stu-id="feefc-126">Gift card module</span></span>](add-giftcard.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]