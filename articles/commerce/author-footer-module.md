---
title: Fußzeilenmodul
description: In diesem Thema werden Fußzeilenmodule behandelt nd wie sie in Dynamics 365 Commerce erstellt werden.
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
ms.openlocfilehash: f8e0290b5af9d0c1fc9ad0279b0d7f81c9feb2fc
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001146"
---
# <a name="footer-module"></a><span data-ttu-id="59f7e-103">Fußzeilenmodul</span><span class="sxs-lookup"><span data-stu-id="59f7e-103">Footer module</span></span>  


[!include [banner](includes/banner.md)]

<span data-ttu-id="59f7e-104">In diesem Thema werden Fußzeilenmodule behandelt und deren Erstellung in Microsoft Dynamics 365 Commerce beschrieben.</span><span class="sxs-lookup"><span data-stu-id="59f7e-104">This topic covers footer modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="59f7e-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="59f7e-105">Overview</span></span>

<span data-ttu-id="59f7e-106">Das Fußzeilenmodul ist ein spezielle Container, der verwendet wird, um die Module zu hosten, die in der Fußzeile erscheinen.</span><span class="sxs-lookup"><span data-stu-id="59f7e-106">The footer module is a special container that is used to host the modules that appear in the page footer.</span></span> <span data-ttu-id="59f7e-107">Zum Beispiel kann es Verknüpfungen an verschiedene Seiten auf der Site umfassen wie **Kontaktieren Sie uns** und **Speichern Sie Richtlinien**.</span><span class="sxs-lookup"><span data-stu-id="59f7e-107">For example, it can include links to various pages across the site, such as **Contact Us** and **Store Policies** pages.</span></span>

## <a name="footer-module-properties"></a><span data-ttu-id="59f7e-108">Fußzeilenmoduleigenschaften</span><span class="sxs-lookup"><span data-stu-id="59f7e-108">Footer module properties</span></span> 

<span data-ttu-id="59f7e-109">Wie die meisten Container unterstützt ein Fußzeilenmodul die Eigenschaften für die Überschrift und die Breite.</span><span class="sxs-lookup"><span data-stu-id="59f7e-109">Like most containers, a footer module support properties for the heading and the width.</span></span> <span data-ttu-id="59f7e-110">Es unterstützt außerdem das Hinzufügen mehrerer Fußzeilenkategoriemodulen.</span><span class="sxs-lookup"><span data-stu-id="59f7e-110">It also supports the addition of multiple footer category modules.</span></span> <span data-ttu-id="59f7e-111">Jedes Fußzeilenkategoriemodul, das hinzugefügt wird, wird als Spalte im Fußzeilenmodul dargestellt.</span><span class="sxs-lookup"><span data-stu-id="59f7e-111">Each footer category module that is added is rendered as a column in the footer module.</span></span>

## <a name="modules-available-in-a-footer-module"></a><span data-ttu-id="59f7e-112">Module, di in einem Fußzeilenmodul verfügbar sind</span><span class="sxs-lookup"><span data-stu-id="59f7e-112">Modules available in a footer module</span></span>

<span data-ttu-id="59f7e-113">**Fußzeilenartikel** – Ein Fußzeilenartikelmodul kann eine Überschrift, ein Bild und einen Link enthalten.</span><span class="sxs-lookup"><span data-stu-id="59f7e-113">**Footer items** – A footer items module can contain a heading, an image, and a link.</span></span> <span data-ttu-id="59f7e-114">Die Überschrift kann entweder alleine oder mit einem Bild und einem Link zusammen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="59f7e-114">The heading can be used either alone or in combination with an image and a link.</span></span> <span data-ttu-id="59f7e-115">Jeder Link in der Fußzeile kann so konfiguriert werden, damit nur Text (z.B. „kontaktieren Sie uns“ und „Datenschutz“ Links) enthalten ist oder Text und ein Bild hat (beispielsweise, Social Media Links).</span><span class="sxs-lookup"><span data-stu-id="59f7e-115">Every link in the footer can be configured so that it has just text (for example, "Contact Us" and "Privacy" links), or so that it has both text and an image (for example, social media links).</span></span>

<span data-ttu-id="59f7e-116">**Zurück zum Anfang** – Ein Modul zurück nach oben stellt einen Link für die rasche Navigation zum Seitenanfang bereit.</span><span class="sxs-lookup"><span data-stu-id="59f7e-116">**Back to top** – A back to top module provides a link for quick navigation to the top of the page.</span></span> <span data-ttu-id="59f7e-117">Ein Ziel ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="59f7e-117">A destination is required.</span></span> <span data-ttu-id="59f7e-118">Der Standardzielwert ist der #, den Benutzer an den Seitenanfang bring.</span><span class="sxs-lookup"><span data-stu-id="59f7e-118">The default destination value is #, which takes the user to the top of the page.</span></span>

## <a name="author-a-footer-module"></a><span data-ttu-id="59f7e-119">Erstellen eines Fußzeilenmoduls</span><span class="sxs-lookup"><span data-stu-id="59f7e-119">Author a footer module</span></span>

1. <span data-ttu-id="59f7e-120">Im Navigationsbereich wählen Sie **Fragmente** und **Neues Seiten-Fragment** aus.</span><span class="sxs-lookup"><span data-stu-id="59f7e-120">In the navigation pane, select **Fragments**, and then select **New Page Fragment**.</span></span>
1. <span data-ttu-id="59f7e-121">Im Dialogfeld **Neues Seiten-Fragment** wählen Sie das Fußzeilenmodul aus, geben Sie einen Namen für das Seitenfragment ein, und wählen Sie dann **OK**.</span><span class="sxs-lookup"><span data-stu-id="59f7e-121">In the **New Page Fragment** dialog box, select the footer module, enter a name for the page fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="59f7e-122">Wählen Sie im Seitenlayout auf der linken Seite die Ellipsen-Schaltfläche (**...**) für das Fußzeilenmodul und anschließend **Modul hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="59f7e-122">In the outline tree on the left, select the ellipsis button (**...**) for the footer module, and then select **Add Module**.</span></span>
1. <span data-ttu-id="59f7e-123">Im Dialogfeld **Modul hinzufügen** wählen Sie das Fußzeilenkategoriemodul und wählen Sie dann **OK**.</span><span class="sxs-lookup"><span data-stu-id="59f7e-123">In the **Add Module** dialog box, select the footer category module, and then select **OK**.</span></span>
1. <span data-ttu-id="59f7e-124">Wählen Sie im Seitenlayout auf der linken Seite die Ellipsen-Schaltfläche für das Fußzeilenmodul und anschließend **Modul hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="59f7e-124">In the outline tree, select the ellipsis button for the footer category module, and then select **Add Module**.</span></span>
1. <span data-ttu-id="59f7e-125">Im Dialogfeld **Modul hinzufügen** wählen Sie das Fußzeilenelementmodul und wählen Sie dann **OK**.</span><span class="sxs-lookup"><span data-stu-id="59f7e-125">In the **Add Module** dialog box, select the footer item module, and then select **OK**.</span></span>
1. <span data-ttu-id="59f7e-126">In der Gliederungsstruktur wählen Sie das Fußzeilenelementmodul aus.</span><span class="sxs-lookup"><span data-stu-id="59f7e-126">In the outline tree, select the footer item module.</span></span> <span data-ttu-id="59f7e-127">Im Eigenschaftenbereich auf der rechten Seite konfigurieren Sie die Überschrift und verknüpfen Sie Text und Bild nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="59f7e-127">Then, in the properties pane on the right, configure the heading, link and link text, and image as you require.</span></span>
1. <span data-ttu-id="59f7e-128">Um weitere Fußzeilenelemente hinzuzufügen, wiederholen Sie die Schritte 5 bis 7.</span><span class="sxs-lookup"><span data-stu-id="59f7e-128">To add more footer items, repeat steps 5 through 7.</span></span>
1. <span data-ttu-id="59f7e-129">Um einen Link „Zurück zum Anfang“ der Fußzeile hinzuzufügen, wählen Sie die Ellipsen-Schaltfläche für das Fußzeilenmodul und anschließend **Modul hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="59f7e-129">To add a "back to top" link to your footer, select the ellipsis button for the footer category module, and then select **Add Module**.</span></span>
1. <span data-ttu-id="59f7e-130">Im Dialogfeld **Modul hinzufügen** wählen Sie das Modul zurück zum Anfang und wählen dann **OK**.</span><span class="sxs-lookup"><span data-stu-id="59f7e-130">In the **Add Module** dialog box, select the back to top module, and then select **OK**.</span></span>
1. <span data-ttu-id="59f7e-131">In der Gliederungsstruktur wählen Sie das Modul zurück zum Anfang aus.</span><span class="sxs-lookup"><span data-stu-id="59f7e-131">In the outline tree, select the back to top module.</span></span> <span data-ttu-id="59f7e-132">Im Eigenschaftenbereich auf der rechten Seite konfigurieren Sie das Modul zurück zum Anfang, wie Sie es benötigen.</span><span class="sxs-lookup"><span data-stu-id="59f7e-132">Then, in the properties pane on the right, configure the back to top module as you require.</span></span>
1. <span data-ttu-id="59f7e-133">Speichern Sie das Seitenfragment, laden Sie es hoch und veröffentlichen Sie es.</span><span class="sxs-lookup"><span data-stu-id="59f7e-133">Save the page fragment, check it in, and publish it.</span></span>

<span data-ttu-id="59f7e-134">Auf jeder Seitenvorlage, die für den Standort erstellt wurde, folgen Sie diesen Schritten.</span><span class="sxs-lookup"><span data-stu-id="59f7e-134">On every page template that has been created for the site, follow these steps.</span></span>

1. <span data-ttu-id="59f7e-135">Im **Haupt-** Slot der Standardseite im Fußzeilenmodul fügen Sie das Fußzeilenfragment hinzu, das Sie erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="59f7e-135">In the **Main** slot of the default page, in the footer module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="59f7e-136">Speichern Sie die Vorlage, laden Sie sie hoch und veröffentlichen Sie sie.</span><span class="sxs-lookup"><span data-stu-id="59f7e-136">Save the template, check it in, and publish it.</span></span>

<span data-ttu-id="59f7e-137">Wenn Sie das Seitenfragment der Seitenvorlagen hinzufügen, helfen Sie sicherzustellen, dass die Fußzeile auf jeder Seite angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="59f7e-137">By adding the page fragment to page templates, you help guarantee that the footer is rendered on every page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="59f7e-138">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="59f7e-138">Additional resources</span></span>

[<span data-ttu-id="59f7e-139">Starterkit-Überblick</span><span class="sxs-lookup"><span data-stu-id="59f7e-139">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="59f7e-140">Containermodul</span><span class="sxs-lookup"><span data-stu-id="59f7e-140">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="59f7e-141">Kauffeldmodul</span><span class="sxs-lookup"><span data-stu-id="59f7e-141">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="59f7e-142">Einkaufswagenmodul</span><span class="sxs-lookup"><span data-stu-id="59f7e-142">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="59f7e-143">Auschecken-Modul</span><span class="sxs-lookup"><span data-stu-id="59f7e-143">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="59f7e-144">Auftragsbestätigungsmodul</span><span class="sxs-lookup"><span data-stu-id="59f7e-144">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="59f7e-145">Kopfzeilenmodul</span><span class="sxs-lookup"><span data-stu-id="59f7e-145">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="59f7e-146">Fußzeilenmodul</span><span class="sxs-lookup"><span data-stu-id="59f7e-146">Footer module</span></span>](author-footer-module.md)
