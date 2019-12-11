---
title: Auftragsbestätigungsmodul
description: In diesem Thema werden Auftragsbestätigungsmodule behandelt und deren Erstellung in Microsoft Dynamics 365 Commerce beschrieben.
author: anupamar
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e339ce02bb646d0d9a68c22b24fde9b72071de6f
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698325"
---
# <a name="order-confirmation-module"></a><span data-ttu-id="65857-103">Auftragsbestätigungsmodul</span><span class="sxs-lookup"><span data-stu-id="65857-103">Order confirmation module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="65857-104">In diesem Thema werden Auftragsbestätigungsmodule behandelt und deren Erstellung in Microsoft Dynamics 365 Commerce beschrieben.</span><span class="sxs-lookup"><span data-stu-id="65857-104">This topic covers order confirmation modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="65857-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="65857-105">Overview</span></span>

<span data-ttu-id="65857-106">Ein Auftragsbestätigungsmodul wird verwendet, um eine Bestätigungsnachricht auf einer Auftragsbestätigungsseite anzuzeigen, nachdem ein Auftrag aufgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="65857-106">An order confirmation module is used to show a confirmation message on an order confirmation page after an order is placed.</span></span> <span data-ttu-id="65857-107">Das Auftragsbestätigungsmodul zeigt die Auftragsbestätigungsnummer und die Debitoren-E-Mail-Adresse an, die beim Bezahlen angegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="65857-107">The order confirmation module shows the order confirmation number and the customer email address that was provided during checkout.</span></span>

<span data-ttu-id="65857-108">Wenn ein Auftrag während des Bestellvorgangs aufgegeben wird, werden die Auftragsbestätigungsnummer und die Debitoren-E-Mail-Adresse als Abfragezeichenfolge in der URL der Seite an die Auftragsbestätigungsseite übergeben.</span><span class="sxs-lookup"><span data-stu-id="65857-108">When an order is placed during checkout, the order confirmation number and customer email address are passed to the order confirmation page as a query string in the page's URL.</span></span> <span data-ttu-id="65857-109">Das Auftragsbestätigungsmodul erhält diese Informationen und zeigt den Auftragsstatus auf der Auftragsbestätigungsseite an.</span><span class="sxs-lookup"><span data-stu-id="65857-109">The order confirmation module receives this information and renders the order status on the order confirmation page.</span></span> <span data-ttu-id="65857-110">Das Auftragsbestätigungsmodul benötigt diesen Seitenkontext, um den Status des Auftrags anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="65857-110">The order confirmation module requires this page context to provide the status of the order.</span></span>

## <a name="order-confirmation-module-properties"></a><span data-ttu-id="65857-111">Eigenschaften des Auftragsbestätigungsmoduls</span><span class="sxs-lookup"><span data-stu-id="65857-111">Order confirmation module properties</span></span>

| <span data-ttu-id="65857-112">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="65857-112">Property name</span></span> | <span data-ttu-id="65857-113">Werte</span><span class="sxs-lookup"><span data-stu-id="65857-113">Values</span></span> | <span data-ttu-id="65857-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="65857-114">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="65857-115">Überschrift</span><span class="sxs-lookup"><span data-stu-id="65857-115">Heading</span></span>       | <span data-ttu-id="65857-116">Überschriftentext und Überschriftsmarkierung (**H1**, **H2**, **H3**, **H4**, **H5** oder **H6**)</span><span class="sxs-lookup"><span data-stu-id="65857-116">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="65857-117">Das Auftragsbestätigungsmodul kann eine Überschrift haben.</span><span class="sxs-lookup"><span data-stu-id="65857-117">The order confirmation module can have a heading.</span></span> <span data-ttu-id="65857-118">Standardmäßig wird die **H2** Überschriftsmarkierung für die Überschrift verwendet.</span><span class="sxs-lookup"><span data-stu-id="65857-118">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="65857-119">Die Markierung kann jedoch geändert werden, um Zugangsbedingungen zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="65857-119">However, the tag can be changed to meet accessibility requirements.</span></span> |

## <a name="modules-that-can-be-used-in-an-order-confirmation-page-module"></a><span data-ttu-id="65857-120">Module, die in einem Modul einer Auftragsbestätigungsseite verwendet werden können</span><span class="sxs-lookup"><span data-stu-id="65857-120">Modules that can be used in an order confirmation page module</span></span> 

- <span data-ttu-id="65857-121">**Empfehlungen** – Das Empfehlungsmodul kann auf der Auftragsbestätigungsseite platziert werden, um dem Kunden andere Produkte vorzuschlagen.</span><span class="sxs-lookup"><span data-stu-id="65857-121">**Recommendations** – The recommendations module can be put on the order confirmation page to suggest other products to the customer.</span></span>
- <span data-ttu-id="65857-122">**Marketing** – Das Marketingmodul kann der Auftragsbestätigungsseite Marketinginhalte hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="65857-122">**Marketing** – The marketing module can add marketing content to the order confirmation page.</span></span>

## <a name="create-an-order-confirmation-page-module"></a><span data-ttu-id="65857-123">Erstellen eines Moduls für eine Auftragsbestätigungsseite</span><span class="sxs-lookup"><span data-stu-id="65857-123">Create an order confirmation page module</span></span>

1. <span data-ttu-id="65857-124">Erstellen Sie eine Seitenvorlage, die mit **Auftragsbestätigung** bezeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="65857-124">Create a page template that is named **order confirmation template**.</span></span>
1. <span data-ttu-id="65857-125">Im **Haupt-** Slot der Standardseite fügen Sie ein Auftragsbestätigungsmodul hinzu.</span><span class="sxs-lookup"><span data-stu-id="65857-125">In the **Main** slot of the default page, add an order confirmation module.</span></span>
1. <span data-ttu-id="65857-126">Fügen Sie im Auftragsbestätigungsmodul ein Empfehlungsmodul hinzu.</span><span class="sxs-lookup"><span data-stu-id="65857-126">In the order confirmation module, add a recommendations module.</span></span>
1. <span data-ttu-id="65857-127">Vorlage speichern und Vorschau anzeigen.</span><span class="sxs-lookup"><span data-stu-id="65857-127">Save and preview the template.</span></span> <span data-ttu-id="65857-128">Das Auftragsbestätigungsmodul soll nicht gerendert werden, da es den Kontext der Auftragsbestätigungsnummer benötigt.</span><span class="sxs-lookup"><span data-stu-id="65857-128">The order confirmation module should not be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="65857-129">Überprüfen Sie in die Vorlage, und veröffentlichen Sie sie.</span><span class="sxs-lookup"><span data-stu-id="65857-129">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="65857-130">Verwenden Sie die Auftragsbestätigungsvorlage, die Sie soeben erstellt haben, um die Seite zu erstellen, die die Bezeichnung **Auftragsbestätigung** hat.</span><span class="sxs-lookup"><span data-stu-id="65857-130">Use the order confirmation template that you just created to create a page that is named **order confirmation page**.</span></span>
1. <span data-ttu-id="65857-131">Fügen Sie die Standardseite zum Seitenumriss hinzu.</span><span class="sxs-lookup"><span data-stu-id="65857-131">Add the default page to the page outline.</span></span>
1. <span data-ttu-id="65857-132">Fügen Sie im **Kopfzeilen**-Slot ein Kopffragment hinzu.</span><span class="sxs-lookup"><span data-stu-id="65857-132">In the **Header** slot, add a header fragment.</span></span>
1. <span data-ttu-id="65857-133">Fügen Sie im **Fußzeilen**-Slot ein Fußzeilenfragment hinzu.</span><span class="sxs-lookup"><span data-stu-id="65857-133">In the **Footer** slot, add a footer fragment.</span></span>
1. <span data-ttu-id="65857-134">Fügen Sie im **Haupt**-Slot ein Auftragsbestätigungsmodul hinzu.</span><span class="sxs-lookup"><span data-stu-id="65857-134">In the **Main** slot, add an order confirmation module.</span></span>
1. <span data-ttu-id="65857-135">Fügen Sie im Eigenschaftenbereich des Auftragsbestätigungsmoduls die Überschrift **Auftragsbestätigung** hinzu.</span><span class="sxs-lookup"><span data-stu-id="65857-135">In the property pane of the order confirmation module, add the heading **Order confirmation**.</span></span>
1. <span data-ttu-id="65857-136">Fügen Sie unter dem Auftragsbestätigungsmodul ein Empfehlungsmodul hinzu und konfigurieren Sie es so, dass es die Einstellungen **Neu** und **Bestseller** verwendet.</span><span class="sxs-lookup"><span data-stu-id="65857-136">Below the order confirmation module, add a recommendations module, and configure it so that it uses the **New** and **Best Selling** settings.</span></span>
1. <span data-ttu-id="65857-137">Speichern Sie die Seite, laden Sie es hoch und zeigen Sie eine Vorschau an.</span><span class="sxs-lookup"><span data-stu-id="65857-137">Save and preview the page, check it in, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="65857-138">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="65857-138">Additional resources</span></span>

[<span data-ttu-id="65857-139">Starterkit-Überblick</span><span class="sxs-lookup"><span data-stu-id="65857-139">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="65857-140">Containermodul</span><span class="sxs-lookup"><span data-stu-id="65857-140">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="65857-141">Kauffeldmodul</span><span class="sxs-lookup"><span data-stu-id="65857-141">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="65857-142">Einkaufswagenmodul</span><span class="sxs-lookup"><span data-stu-id="65857-142">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="65857-143">Auschecken-Modul</span><span class="sxs-lookup"><span data-stu-id="65857-143">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="65857-144">Kopfzeilenmodul</span><span class="sxs-lookup"><span data-stu-id="65857-144">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="65857-145">Fußzeilenmodul</span><span class="sxs-lookup"><span data-stu-id="65857-145">Footer module</span></span>](author-footer-module.md)
