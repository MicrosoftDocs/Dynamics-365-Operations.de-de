---
title: Symbol Einkaufswagenmodul
description: Dieses Thema enthält das Warenkorbsymbolmodul und es wird beschrieben, wie es Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: ebc5cfa490a4c8538fd081aced0844ed01d63a26
ms.sourcegitcommit: 12d271bb26c7490e7525d9b4bbf125cdc39fef43
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/07/2020
ms.locfileid: "4412724"
---
# <a name="cart-icon-module"></a><span data-ttu-id="39569-103">Symbol Einkaufswagenmodul</span><span class="sxs-lookup"><span data-stu-id="39569-103">Cart icon module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="39569-104">Dieses Thema enthält das Warenkorbsymbolmodul und es wird beschrieben, wie es Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="39569-104">This topic covers the cart icon module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="39569-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="39569-105">Overview</span></span>

<span data-ttu-id="39569-106">Warenkorbsymbol – Das Warenkorbsymbolmodul im Kopfmodul der Seite zeigt die Anzahl der Artikel im Warenkorb zu einem bestimmten Zeitpunkt an.</span><span class="sxs-lookup"><span data-stu-id="39569-106">The cart icon module represents the cart in the header module of the page, and shows the number of items in the cart.</span></span> <span data-ttu-id="39569-107">Das Warenkorbsymbolmodul zeigt auch eine Warenkorbübersicht (auch als Minikorb bezeichnet) an, wenn Sie den Mauszeiger über das Warenkorbsymbol halten.</span><span class="sxs-lookup"><span data-stu-id="39569-107">The cart icon module also displays a cart summary (also known as a mini cart) when the cart icon is hovered over.</span></span> <span data-ttu-id="39569-108">Der Mini-Warenkorb bietet dem Benutzer eine Zusammenfassung der Artikel im Warenkorb, ohne zur Warenkorbseite navigieren zu müssen.</span><span class="sxs-lookup"><span data-stu-id="39569-108">The mini cart provides the user with a summary of the items in the cart without having to navigate to the cart page.</span></span> <span data-ttu-id="39569-109">Darüber hinaus kann der Benutzer direkt zur Checkout-Seite gehen, wenn er mit der Zusammenfassung zufrieden ist.</span><span class="sxs-lookup"><span data-stu-id="39569-109">In addition, it also allows the user to directly go to checkout page if they are happy with the summary.</span></span> <span data-ttu-id="39569-110">Dies reduziert die Anzahl der Seitennavigationen und beschleunigt das Auschecken.</span><span class="sxs-lookup"><span data-stu-id="39569-110">This reduces the number of page navigations and makes checkout faster.</span></span> 

> [!NOTE]
> <span data-ttu-id="39569-111">Hilfe für das Modul Warenkorbsymbol finden Sie in Dynamics 365 Commerce Release 10.0.11.</span><span class="sxs-lookup"><span data-stu-id="39569-111">Support for the cart icon module is available in the Dynamics 365 Commerce 10.0.11 release.</span></span>

<span data-ttu-id="39569-112">Das folgende Bild zeigt ein Beispiel für ein Warenkorbsymbolmodul, das einen Mini-Wagen in der Fabrikam-Kopfzeile anzeigt.</span><span class="sxs-lookup"><span data-stu-id="39569-112">The following image shows an example of a cart icon module that displays a mini cart in the Fabrikam header.</span></span>

![Beispiel eines Warenkorbsymbolmoduls](./media/ecommerce-Minicart.PNG)

## <a name="module-properties"></a><span data-ttu-id="39569-114">Moduleigenschaften</span><span class="sxs-lookup"><span data-stu-id="39569-114">Module properties</span></span>

- <span data-ttu-id="39569-115">**Mini-Warenkorb anzeigen** – Wenn true, kann mit dieser Eigenschaft eine Warenkorbübersicht (Mini-Warenkorb) angezeigt werden, wenn Sie den Mauszeiger über das Warenkorbsymbol bewegen.</span><span class="sxs-lookup"><span data-stu-id="39569-115">**Show mini cart** – When true, this property enables a cart summary (mini cart) to be displayed when the cart icon is hovered over.</span></span> <span data-ttu-id="39569-116">Diese Funktionalität wird nur für Desktop-Ansichtsports unterstützt.</span><span class="sxs-lookup"><span data-stu-id="39569-116">This functionality is only supported for desktop view ports.</span></span>

## <a name="add-a-cart-icon-module-to-a-page"></a><span data-ttu-id="39569-117">Ein Warenkorbsymbolmodul einer Seite hinzufügen</span><span class="sxs-lookup"><span data-stu-id="39569-117">Add a cart icon module to a page</span></span>

<span data-ttu-id="39569-118">Informationen zum Hinzufügen eines Warenkorbsymbolmoduls finden Sie unter [Kopf-Modul](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="39569-118">To add a cart icon module, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="39569-119">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="39569-119">Additional resources</span></span>

[<span data-ttu-id="39569-120">Einkaufswagenmodul</span><span class="sxs-lookup"><span data-stu-id="39569-120">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="39569-121">Auschecken-Modul</span><span class="sxs-lookup"><span data-stu-id="39569-121">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="39569-122">Zahlungsmodul</span><span class="sxs-lookup"><span data-stu-id="39569-122">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="39569-123">Versandadressenmodul</span><span class="sxs-lookup"><span data-stu-id="39569-123">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="39569-124">Lieferoptionenmodul</span><span class="sxs-lookup"><span data-stu-id="39569-124">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="39569-125">Abholinformationsmodul</span><span class="sxs-lookup"><span data-stu-id="39569-125">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="39569-126">Auftragsdetailmodul</span><span class="sxs-lookup"><span data-stu-id="39569-126">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="39569-127">Geschenkkartenmodul</span><span class="sxs-lookup"><span data-stu-id="39569-127">Gift card module</span></span>](add-giftcard.md)
