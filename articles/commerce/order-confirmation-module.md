---
title: Auftragsdetailmodul
description: In diesem Thema werden Auftragsdetailmodule behandelt und deren Verwendung in Microsoft Dynamics 365 Commerce beschrieben.
author: anupamar
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: cb09a0b6ce1e48707f96021e9fad0006d9c1c55c
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2020
ms.locfileid: "3026016"
---
# <a name="order-details-module"></a><span data-ttu-id="518bc-103">Auftragsdetailmodul</span><span class="sxs-lookup"><span data-stu-id="518bc-103">Order details module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="518bc-104">In diesem Thema werden Auftragsdetailmodule behandelt und deren Verwendung in Microsoft Dynamics 365 Commerce beschrieben.</span><span class="sxs-lookup"><span data-stu-id="518bc-104">This topic covers order details modules and describes how to use them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="518bc-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="518bc-105">Overview</span></span>

<span data-ttu-id="518bc-106">Nachdem eine Bestellung aufgegeben wurde, kann das Bestelldetailmodul verwendet werden, um die Bestätigungsdetails anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="518bc-106">The order details module is used to show order confirmation details after an order has been placed.</span></span> <span data-ttu-id="518bc-107">Hier werden die Bestellbestätigungs-ID, die Bestellkontaktinformationen und andere Bestelldetails angezeigt, z. B. die gekauften Artikel, die Zahlungsinformationen und die Versandmethode.</span><span class="sxs-lookup"><span data-stu-id="518bc-107">It shows the order confirmation ID, order contact information, and other order details, such as the items that were purchased, payment information, and the shipping method.</span></span>

## <a name="order-confirmation-module-properties"></a><span data-ttu-id="518bc-108">Eigenschaften des Auftragsbestätigungsmoduls</span><span class="sxs-lookup"><span data-stu-id="518bc-108">Order confirmation module properties</span></span>

| <span data-ttu-id="518bc-109">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="518bc-109">Property name</span></span>  | <span data-ttu-id="518bc-110">Werte</span><span class="sxs-lookup"><span data-stu-id="518bc-110">Values</span></span> | <span data-ttu-id="518bc-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="518bc-111">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="518bc-112">Überschrift</span><span class="sxs-lookup"><span data-stu-id="518bc-112">Heading</span></span>        | <span data-ttu-id="518bc-113">Überschriftentext und Überschriftsmarkierung (**H1**, **H2**, **H3**, **H4**, **H5** oder **H6**)</span><span class="sxs-lookup"><span data-stu-id="518bc-113">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="518bc-114">Das Auftragsbestätigungsmodul kann eine Überschrift haben.</span><span class="sxs-lookup"><span data-stu-id="518bc-114">The order confirmation module can have a heading.</span></span> <span data-ttu-id="518bc-115">Standardmäßig wird die **H2** Überschriftsmarkierung für die Überschrift verwendet.</span><span class="sxs-lookup"><span data-stu-id="518bc-115">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="518bc-116">Die Markierung kann jedoch geändert werden, um Zugangsbedingungen zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="518bc-116">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="518bc-117">Kontaktnummer</span><span class="sxs-lookup"><span data-stu-id="518bc-117">Contact number</span></span> | <span data-ttu-id="518bc-118">Text</span><span class="sxs-lookup"><span data-stu-id="518bc-118">Text</span></span> | <span data-ttu-id="518bc-119">Für auftragsbezogene Fragen kann eine Telefonnummer angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="518bc-119">A contact number can be provided for order-related questions.</span></span> |

## <a name="modules-that-can-be-used-on-an-order-details-page"></a><span data-ttu-id="518bc-120">Module, die in einem Modul einer Auftragsdetailseite verwendet werden können</span><span class="sxs-lookup"><span data-stu-id="518bc-120">Modules that can be used on an order details page</span></span>

<span data-ttu-id="518bc-121">Wenn Sie eine Bestelldetailseite erstellen, können Sie zusätzlich zum Bestelldetail-Modul weitere relevante Module hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="518bc-121">When you create an order details page, you can add other relevant modules in addition to the order details module.</span></span> <span data-ttu-id="518bc-122">Im Folgenden finden Sie einige Beispiele hierfür:</span><span class="sxs-lookup"><span data-stu-id="518bc-122">Here are some examples:</span></span>

- <span data-ttu-id="518bc-123">**Empfehlungsmodule** – Das Empfehlungsmodul kann auf der Auftragsbestätigungsseite platziert werden, um dem Kunden andere Produkte vorzuschlagen.</span><span class="sxs-lookup"><span data-stu-id="518bc-123">**Recommendations module** – The recommendations module can be added to the order details page to suggest other products to the customer.</span></span>
- <span data-ttu-id="518bc-124">**Marketing-Module** – Zur Seite mit den Bestelldetails kann ein beliebiges Marketingmodul hinzugefügt werden, um Marketinginhalte anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="518bc-124">**Marketing modules** – Any marketing module can be added to the order details page to show marketing content.</span></span>

## <a name="create-an-order-details-page-module"></a><span data-ttu-id="518bc-125">Erstellen eines Moduls für eine Bestelldetailseite</span><span class="sxs-lookup"><span data-stu-id="518bc-125">Create an order details page module</span></span>

1. <span data-ttu-id="518bc-126">Erstellen Sie eine Seitenvorlage, die mit **Auftragdetailvorlage** bezeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="518bc-126">Create a page template that is named **Order details template**.</span></span>
1. <span data-ttu-id="518bc-127">Im **Haupt-** Slot der Standardseite fügen Sie ein Auftragsdetailmodul hinzu.</span><span class="sxs-lookup"><span data-stu-id="518bc-127">In the **Main** slot of the default page, add an order details module.</span></span>
1. <span data-ttu-id="518bc-128">Fügen Sie im Auftragsdetailmodul ein Empfehlungsmodul hinzu.</span><span class="sxs-lookup"><span data-stu-id="518bc-128">In the order details module, add a recommendations module.</span></span>
1. <span data-ttu-id="518bc-129">Vorlage speichern und Vorschau anzeigen.</span><span class="sxs-lookup"><span data-stu-id="518bc-129">Save and preview the template.</span></span> <span data-ttu-id="518bc-130">Das Auftragsdetailmodul soll nicht gerendert werden, da es den Kontext der Auftragsbestätigungsnummer benötigt.</span><span class="sxs-lookup"><span data-stu-id="518bc-130">The order details module won't be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="518bc-131">Beenden Sie die Bearbeitung der Vorlage und veröffentlichen Sie sie.</span><span class="sxs-lookup"><span data-stu-id="518bc-131">Finish editing the template, and publish it.</span></span>
1. <span data-ttu-id="518bc-132">Verwenden Sie die Auftragsdetailvorlage, die Sie soeben erstellt haben, um die Seite zu erstellen, die die Bezeichnung **Auftragsdetail** hat.</span><span class="sxs-lookup"><span data-stu-id="518bc-132">Use the order details template that you just created to create a page that is named **order details page**.</span></span>
1. <span data-ttu-id="518bc-133">Fügen Sie die Standardseite zum Seitenumriss hinzu.</span><span class="sxs-lookup"><span data-stu-id="518bc-133">Add the default page to the page outline.</span></span>
1. <span data-ttu-id="518bc-134">Fügen Sie im **Kopfzeilen**-Slot ein Kopffragment hinzu.</span><span class="sxs-lookup"><span data-stu-id="518bc-134">In the **Header** slot, add a header fragment.</span></span>
1. <span data-ttu-id="518bc-135">Fügen Sie im **Fußzeilen**-Slot ein Fußzeilenfragment hinzu.</span><span class="sxs-lookup"><span data-stu-id="518bc-135">In the **Footer** slot, add a footer fragment.</span></span>
1. <span data-ttu-id="518bc-136">Fügen Sie im **Haupt**-Slot ein Auftragsdetailmodul hinzu.</span><span class="sxs-lookup"><span data-stu-id="518bc-136">In the **Main** slot, add an order details module.</span></span>
1. <span data-ttu-id="518bc-137">Fügen Sie im Eigenschaftenbereich für Auftragsdetailmodule die Überschrift **Auftragsdetail** hinzu.</span><span class="sxs-lookup"><span data-stu-id="518bc-137">In the property pane for the order details module, add the heading **Order details**.</span></span>
1. <span data-ttu-id="518bc-138">Fügen Sie unter dem Auftragsdetailmodul ein Empfehlungsmodul hinzu und konfigurieren Sie es so, dass es die Einstellungen **Neu** und **Bestseller** verwendet.</span><span class="sxs-lookup"><span data-stu-id="518bc-138">Below the order details module, add a recommendations module, and configure it so that it uses the **New** and **Best Selling** settings.</span></span>
1. <span data-ttu-id="518bc-139">Seite speichern und Vorschau anzeigen.</span><span class="sxs-lookup"><span data-stu-id="518bc-139">Save and preview the page.</span></span>
1. <span data-ttu-id="518bc-140">Beenden Sie die Bearbeitung der Seite und veröffentlichen Sie sie.</span><span class="sxs-lookup"><span data-stu-id="518bc-140">Finish editing the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="518bc-141">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="518bc-141">Additional resources</span></span>

[<span data-ttu-id="518bc-142">Starterkit-Übersicht</span><span class="sxs-lookup"><span data-stu-id="518bc-142">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="518bc-143">Containermodul</span><span class="sxs-lookup"><span data-stu-id="518bc-143">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="518bc-144">Kauffeldmodul</span><span class="sxs-lookup"><span data-stu-id="518bc-144">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="518bc-145">Einkaufswagenmodul</span><span class="sxs-lookup"><span data-stu-id="518bc-145">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="518bc-146">Auschecken-Modul</span><span class="sxs-lookup"><span data-stu-id="518bc-146">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="518bc-147">Kopfzeilenmodul</span><span class="sxs-lookup"><span data-stu-id="518bc-147">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="518bc-148">Fußzeilenmodul</span><span class="sxs-lookup"><span data-stu-id="518bc-148">Footer module</span></span>](author-footer-module.md)
