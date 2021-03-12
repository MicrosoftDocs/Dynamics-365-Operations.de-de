---
title: Fußzeilenmodul
description: In diesem Thema werden Fußzeilenmodule behandelt nd wie sie in Dynamics 365 Commerce erstellt werden.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 038fee32cbf1ed6b4967f440faaf3c0d4fa583f6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4979946"
---
# <a name="footer-module"></a><span data-ttu-id="2f2de-103">Fußzeilenmodul</span><span class="sxs-lookup"><span data-stu-id="2f2de-103">Footer module</span></span>  

[!include [banner](includes/banner.md)]

<span data-ttu-id="2f2de-104">In diesem Thema werden Fußzeilenmodule behandelt und deren Erstellung in Microsoft Dynamics 365 Commerce beschrieben.</span><span class="sxs-lookup"><span data-stu-id="2f2de-104">This topic covers footer modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="2f2de-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="2f2de-105">Overview</span></span>

<span data-ttu-id="2f2de-106">Das Fußzeilenmodul ist ein spezielle Container, der verwendet wird, um die Module zu hosten, die in der Fußzeile erscheinen.</span><span class="sxs-lookup"><span data-stu-id="2f2de-106">The footer module is a special container that is used to host the modules that appear in the page footer.</span></span> <span data-ttu-id="2f2de-107">Zum Beispiel kann es Verknüpfungen an verschiedene Seiten auf der Site umfassen wie **Kontaktieren Sie uns** und **Speichern Sie Richtlinien**.</span><span class="sxs-lookup"><span data-stu-id="2f2de-107">For example, it can include links to various pages across the site, such as **Contact Us** and **Store Policies** pages.</span></span>

<span data-ttu-id="2f2de-108">Das folgende Bild zeigt ein Beispiel eines Fußzeilenmoduls, das auf einer Homepage verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2f2de-108">The following image shows an example of a footer module on a site page.</span></span>

![Beispiel eines Fußzeilenmoduls](./media/ecommerce-footer.PNG)

## <a name="footer-module-properties"></a><span data-ttu-id="2f2de-110">Fußzeilenmoduleigenschaften</span><span class="sxs-lookup"><span data-stu-id="2f2de-110">Footer module properties</span></span> 

<span data-ttu-id="2f2de-111">Wie die meisten Container unterstützt ein Fußzeilenmodul die Eigenschaften für die Überschrift und die Breite.</span><span class="sxs-lookup"><span data-stu-id="2f2de-111">Like most containers, a footer module supports properties for the heading and the width.</span></span> <span data-ttu-id="2f2de-112">Es unterstützt außerdem das Hinzufügen mehrerer Fußzeilenkategoriemodulen.</span><span class="sxs-lookup"><span data-stu-id="2f2de-112">It also supports the addition of multiple footer category modules.</span></span> <span data-ttu-id="2f2de-113">Jedes Fußzeilenkategoriemodul, das hinzugefügt wird, wird als Spalte im Fußzeilenmodul dargestellt.</span><span class="sxs-lookup"><span data-stu-id="2f2de-113">Each footer category module that is added is rendered as a column in the footer module.</span></span>

## <a name="modules-available-in-a-footer-module"></a><span data-ttu-id="2f2de-114">Module, di in einem Fußzeilenmodul verfügbar sind</span><span class="sxs-lookup"><span data-stu-id="2f2de-114">Modules available in a footer module</span></span>

<span data-ttu-id="2f2de-115">**Fußzeilenartikel** – Ein Fußzeilenartikelmodul kann eine Überschrift, ein Bild und einen Link enthalten.</span><span class="sxs-lookup"><span data-stu-id="2f2de-115">**Footer items** – A footer items module can contain a heading, an image, and a link.</span></span> <span data-ttu-id="2f2de-116">Die Überschrift kann entweder alleine oder mit einem Bild und einem Link zusammen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2f2de-116">The heading can be used either alone or in combination with an image and a link.</span></span> <span data-ttu-id="2f2de-117">Jeder Link in der Fußzeile kann so konfiguriert werden, damit nur Text (z.B. „kontaktieren Sie uns“ und „Datenschutz“ Links) enthalten ist oder Text und ein Bild hat (beispielsweise, Social Media Links).</span><span class="sxs-lookup"><span data-stu-id="2f2de-117">Every link in the footer can be configured so that it has just text (for example, "Contact Us" and "Privacy" links), or so that it has both text and an image (for example, social media links).</span></span>

<span data-ttu-id="2f2de-118">**Zurück zum Anfang** – Ein Modul zurück nach oben stellt einen Link für die rasche Navigation zum Seitenanfang bereit.</span><span class="sxs-lookup"><span data-stu-id="2f2de-118">**Back to top** – A back to top module provides a link for quick navigation to the top of the page.</span></span> <span data-ttu-id="2f2de-119">Ein Ziel ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2f2de-119">A destination is required.</span></span> <span data-ttu-id="2f2de-120">Der Standardzielwert ist \#, den Benutzer an den Seitenanfang bringt.</span><span class="sxs-lookup"><span data-stu-id="2f2de-120">The default destination value is \#, which takes the user to the top of the page.</span></span>

## <a name="create-a-footer-module"></a><span data-ttu-id="2f2de-121">Erstellen eines Fußzeilenmoduls</span><span class="sxs-lookup"><span data-stu-id="2f2de-121">Create a footer module</span></span>

1. <span data-ttu-id="2f2de-122">Wechseln Sie zu **Fragmente** und wählen Sie **Neu** aus, um ein neues Fragment zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2f2de-122">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="2f2de-123">Wählen Sie im Dialogfeld **Neues Fragment** das Modul **Container** aus, geben Sie einen Namen für das Fragment ein und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="2f2de-123">In the **New fragment** dialog box, select the **Container** module, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="2f2de-124">Wählen Sie im Slot **Standard-Container** die Ellipsen-Schaltfläche (**...**) und wählen Sie **Modul hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="2f2de-124">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="2f2de-125">Im Dialogfeld **Modul hinzufügen** wählen Sie das **Fußzeilenkategoriemodul** und wählen Sie dann **OK**.</span><span class="sxs-lookup"><span data-stu-id="2f2de-125">In the **Add Module** dialog box, select the **Footer category** module, and then select **OK**.</span></span>
1. <span data-ttu-id="2f2de-126">Wählen Sie im Slot **Fußzeilenkategorie** die Ellipsen-Schaltfläche (**...**) und wählen Sie **Modul hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="2f2de-126">In the **Footer category** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="2f2de-127">Im Dialogfeld **Modul hinzufügen** wählen Sie das **Fußzeilenelement**-Modul und wählen Sie dann **OK**.</span><span class="sxs-lookup"><span data-stu-id="2f2de-127">In the **Add Module** dialog box, select the **Footer item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="2f2de-128">Wählen Sie den Slot **Fußzeilenelement** und wählen Sei dann im Eigenschaftenbereich auf der rechten Seite konfigurieren Sie die Überschrift und verknüpfen Sie Text und Bild nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="2f2de-128">Select the **Footer item** slot, and then, in the properties pane on the right, configure the heading, link and link text, and image as needed.</span></span>
1. <span data-ttu-id="2f2de-129">Um weitere Fußzeilenelemente hinzuzufügen, wiederholen Sie die Schritte 5 bis 7.</span><span class="sxs-lookup"><span data-stu-id="2f2de-129">To add more footer items, repeat steps 5 through 7 for each.</span></span>
1. <span data-ttu-id="2f2de-130">Um einen Link „Zurück zum Anfang“ der Fußzeile hinzuzufügen, wählen Sie die Ellipsen-Schaltfläche (**...**) für die **Fußzeilenkategorie** und anschließend **Modul hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="2f2de-130">To add a "back to top" link to your footer, select the ellipsis (**...**) in the **Footer category** slot, and then select **Add Module**.</span></span>
1. <span data-ttu-id="2f2de-131">Im Dialogfeld **Modul hinzufügen** wählen Sie das Modul **zurück zum Anfang** und wählen dann **OK**.</span><span class="sxs-lookup"><span data-stu-id="2f2de-131">In the **Add Module** dialog box, select the **Back to top** module, and then select **OK**.</span></span>
1. <span data-ttu-id="2f2de-132">Wählen Sie den Slot **Zurück an den Anfang** und wählen Sie dann im Eigenschaftenbereich auf der rechten Seite Konfigurieren Sie den Text und andere Moduleigenschaften nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="2f2de-132">Select the **Back to top** slot, and then, in the properties pane on the right, configure the text and other module properties as needed.</span></span>
1. <span data-ttu-id="2f2de-133">Wählen **Bearbeiten beenden**, um das Fragment einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="2f2de-133">Select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="2f2de-134">Um Sicherzustellen, dass eine Kopfzeile auf jeder Seite angezeigt wird, führen Sie die folgenden Schritte für jede Seitenvorlage aus, die für die Site erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="2f2de-134">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="2f2de-135">Im Slot **Fußzeile** wählen Sie das Modul **Standardseite** und fügen das Fußzeilenfragment hinzu, das Sie erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="2f2de-135">In the **Footer** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="2f2de-136">Wählen **Bearbeiten beenden**, um die Vorlage einzuchecken, und wählen Sie dann **Veröffentlichen**, um sie zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="2f2de-136">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="2f2de-137">Wenn Sie das Fragment der Seitenvorlagen hinzufügen, helfen Sie sicherzustellen, dass die Fußzeile auf jeder Seite angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="2f2de-137">By adding the fragment to page templates, you help guarantee that the footer is rendered on every page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2f2de-138">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="2f2de-138">Additional resources</span></span>

[<span data-ttu-id="2f2de-139">Übersicht über die Modulbibliothek</span><span class="sxs-lookup"><span data-stu-id="2f2de-139">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="2f2de-140">Containermodul</span><span class="sxs-lookup"><span data-stu-id="2f2de-140">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="2f2de-141">Kauffeldmodul</span><span class="sxs-lookup"><span data-stu-id="2f2de-141">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="2f2de-142">Einkaufswagenmodul</span><span class="sxs-lookup"><span data-stu-id="2f2de-142">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="2f2de-143">Auschecken-Modul</span><span class="sxs-lookup"><span data-stu-id="2f2de-143">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="2f2de-144">Auftragsbestätigungsmodul</span><span class="sxs-lookup"><span data-stu-id="2f2de-144">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="2f2de-145">Kopfzeilenmodul</span><span class="sxs-lookup"><span data-stu-id="2f2de-145">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="2f2de-146">Fußzeilenmodul</span><span class="sxs-lookup"><span data-stu-id="2f2de-146">Footer module</span></span>](author-footer-module.md)
