---
title: Einkaufswagenmodul
description: Dieses Thema enthält Einkaufsmodule und es wird beschrieben, wie diese den Sitesieten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f21268ed4cffed1d5c789f722796cdf05e965819
ms.sourcegitcommit: 4a981ee4be6d7e6c0e55541535d386bce2565cba
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/27/2020
ms.locfileid: "3621035"
---
# <a name="cart-module"></a><span data-ttu-id="0bf6f-103">Einkaufswagenmodul</span><span class="sxs-lookup"><span data-stu-id="0bf6f-103">Cart module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0bf6f-104">Dieses Thema enthält Einkaufsmodule und es wird beschrieben, wie diese den Sitesieten in Microsoft Dynamics 365 Commerce hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="0bf6f-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="0bf6f-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="0bf6f-105">Overview</span></span>

<span data-ttu-id="0bf6f-106">Über das Warenkorbmodul werden die Artikel angezeigt, die dem Warenkorb hinzugefügt wurden, bevor der Kunde zur Kasse geht.</span><span class="sxs-lookup"><span data-stu-id="0bf6f-106">A cart module shows the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="0bf6f-107">Das Modul zeigt eine Bestellzusammenfassung an und der Kunde kann Werbecodes anwenden oder entfernen.</span><span class="sxs-lookup"><span data-stu-id="0bf6f-107">The module also shows an order summary and lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="0bf6f-108">Das Einkaufskorbmodul unterstützt das Auschecken von angemeldeten Benutzern und von Gästen.</span><span class="sxs-lookup"><span data-stu-id="0bf6f-108">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="0bf6f-109">Es unterstützt auch eine Verknüpfung **Zurück zum Einkaufen**.</span><span class="sxs-lookup"><span data-stu-id="0bf6f-109">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="0bf6f-110">Sie können die Route für diesen Link unter **Seiteneinstellungen \> Erweiterungen \> Routen** konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="0bf6f-110">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="0bf6f-111">Das Warenkorbmodul rendert Daten basierend auf der Warenkorb-ID, einem auf der gesamten Site verfügbaren Browser-Cookie.</span><span class="sxs-lookup"><span data-stu-id="0bf6f-111">The cart module renders data based on the cart ID, which is a browser cookie available throughout the site.</span></span> 

<span data-ttu-id="0bf6f-112">Das folgende Bild zeigt ein Beispiel einer Warenkorbseite auf der Fabrikam-Site.</span><span class="sxs-lookup"><span data-stu-id="0bf6f-112">The following image shows an example of a cart page on the Fabrikam site.</span></span>

![Beispiel eines Warenkorb-Moduls](./media/cart2.PNG)

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="0bf6f-114">Einkaufswagenmodul-Eigenschaften und Slots</span><span class="sxs-lookup"><span data-stu-id="0bf6f-114">Cart module properties and slots</span></span>

<span data-ttu-id="0bf6f-115">Das Wagenmodul hat eine **Überschrift**-Eigenschaft, die auf Werte wie **Einkaufstasche** und **Artikel im Einkaufskorb** gesetzt werden kann.</span><span class="sxs-lookup"><span data-stu-id="0bf6f-115">The cart module has a **Heading** property that can be set to values such as **Shopping bag** and **Items in your cart**.</span></span> 

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="0bf6f-116">Module, die im Einkaufswagenmodul verwendet werden können</span><span class="sxs-lookup"><span data-stu-id="0bf6f-116">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="0bf6f-117">**Textblock** – Dieses Modul unterstützt benutzerdefinierte Nachrichten im Einkaufswagenmodul.</span><span class="sxs-lookup"><span data-stu-id="0bf6f-117">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="0bf6f-118">Die Meldungen werden durch das Content Management-System (CMS) gesteuert.</span><span class="sxs-lookup"><span data-stu-id="0bf6f-118">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="0bf6f-119">Es können beliebige Nachrichten hinzugefügt werden wie „Für Probleme mit der Bestellung, kontaktieren Sie 1-800-Fabrikam.“</span><span class="sxs-lookup"><span data-stu-id="0bf6f-119">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="0bf6f-120">**Store-Selector** – Dieses Modul wird eine Liste von nahe gelegene Filialen anzeigen, die für eine Abholung zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="0bf6f-120">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="0bf6f-121">Hier können Benutzer einen Ort eingeben, um nach Geschäften in der Nähe zu suchen.</span><span class="sxs-lookup"><span data-stu-id="0bf6f-121">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="0bf6f-122">Weitere Informationen zu diesem Modul finden Sie unter [Auswahlmodul speichern](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="0bf6f-122">For more information on this module, see [Store selector module](store-selector.md).</span></span>

## <a name="module-properties"></a><span data-ttu-id="0bf6f-123">Moduleigenschaften</span><span class="sxs-lookup"><span data-stu-id="0bf6f-123">Module properties</span></span>

<span data-ttu-id="0bf6f-124">Die folgenden Warenkorbmoduleigenschaften können unter **Site-Einstellungen \> Erweiterungen** konfiguriert werden:</span><span class="sxs-lookup"><span data-stu-id="0bf6f-124">The following cart module settings can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="0bf6f-125">**Höchstmenge** – Diese Eigenschaft dient zur Angabe der maximalen Anzahl jedes Artikels, die dem Einkaufskorb hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="0bf6f-125">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="0bf6f-126">Beispielsweise kann ein Einzelhändler festlegen, dass nur 10 eines Produkts als einzelne Transaktion verkauft werden können.</span><span class="sxs-lookup"><span data-stu-id="0bf6f-126">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="0bf6f-127">**Bestand** – Informationen zum Anwenden von Bestandeinstellungen finden Sie unter [Wenden Sie Bestandeinstellungen an](inventory-settings.md).</span><span class="sxs-lookup"><span data-stu-id="0bf6f-127">**Inventory** – For information about how to apply inventory settings, see [Apply inventory settings](inventory-settings.md).</span></span>
- <span data-ttu-id="0bf6f-128">**Zurück zum Einkaufen** – Mit dieser Eigenschaft wird die Route für die Verknüpfung **Zurück zum Einkaufen** angegeben.</span><span class="sxs-lookup"><span data-stu-id="0bf6f-128">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="0bf6f-129">Die Route kann auf Site-Ebene konfiguriert werden, sodass Einzelhändler den Kunden zur Homepage oder zu einer anderen Seite der Site zurückführen können.</span><span class="sxs-lookup"><span data-stu-id="0bf6f-129">The route can be configured at the site level, allowing retailers to take the customer back to the home page or any other page on the site.</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="0bf6f-130">Commerce Scale Unit-Interaktion</span><span class="sxs-lookup"><span data-stu-id="0bf6f-130">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="0bf6f-131">Das Einkaufskorbmoduls ruft Produktinformationen mithilfe der APIs der Commerce-Skalierungseinheit ab.</span><span class="sxs-lookup"><span data-stu-id="0bf6f-131">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="0bf6f-132">Die Kennung vom Einkaufskorb vom Browsercookie wird verwendet, um die gesamte Produktinformationen der Commerce-Skalierungseinheit abzurufen.</span><span class="sxs-lookup"><span data-stu-id="0bf6f-132">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="0bf6f-133">Ein Einkaufswagenmodul einer Seite hinzufügen</span><span class="sxs-lookup"><span data-stu-id="0bf6f-133">Add a cart module to a page</span></span>

<span data-ttu-id="0bf6f-134">Um ein Einkaufswagenmodul einer neuen Seite hinzuzufügen und die erforderlichen Eigenschaften festzulegen, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="0bf6f-134">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="0bf6f-135">Wechseln Sie zu **Seitenfragmente**, und wählen Sie dann **Neu** aus, um das neue Fragment zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0bf6f-135">Go to **Page Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="0bf6f-136">Wählen Sie im Dialogfeld **Neues Seitenfragment** das Modul **Warenkorb**.</span><span class="sxs-lookup"><span data-stu-id="0bf6f-136">In the **New Page Fragment** dialog box, select the **Cart** module.</span></span>
1. <span data-ttu-id="0bf6f-137">Unter **Name des Seitenfragments** geben Sie einen Namen für das **Warenkorb-Fragment** ein und wählen Sie dann **OK**.</span><span class="sxs-lookup"><span data-stu-id="0bf6f-137">Under **Page Fragment Name**, enter the name **Cart fragment**, and then select **OK**.</span></span>
1. <span data-ttu-id="0bf6f-138">Wählen Sie den Slot **Warenkorb** aus.</span><span class="sxs-lookup"><span data-stu-id="0bf6f-138">Select the **Cart** slot.</span></span>
1. <span data-ttu-id="0bf6f-139">Wählen Sie im Eigenschaftenbereich rechts das Stiftsymbol aus, geben Sie den Überschriftentext in das Feld ein und wählen Sie dann das Häkchensymbol aus.</span><span class="sxs-lookup"><span data-stu-id="0bf6f-139">In the properties pane on the right, select the pencil symbol, enter heading text in the field, and then select the check mark symbol.</span></span>
1. <span data-ttu-id="0bf6f-140">Wählen Sie im Slot **Warenkorb** die Ellipsen-Schaltfläche (**...**) und wählen Sie **Modul hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="0bf6f-140">In the **Cart** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="0bf6f-141">Wählen Sie im Dialogfeld **Modul hinzufügen** das Modul **Auswahl speichern** und dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="0bf6f-141">In the **Add Module** dialog box, select the **Store selector** module, and then select **OK**.</span></span>
1. <span data-ttu-id="0bf6f-142">Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um das Fragment einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="0bf6f-142">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="0bf6f-143">Wechseln Sie zu **Vorlagen** und wählen Sie **Neu** aus, um eine neue Vorlage zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0bf6f-143">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="0bf6f-144">Im Dialogfeld **Neue Vorlage** unter Vorlagenname geben Sie einen Namen für die neue **Vorlage** ein und wählen OK.</span><span class="sxs-lookup"><span data-stu-id="0bf6f-144">In the **New Template** dialog box, under **Template name**, enter a name for the template.</span></span>
1. <span data-ttu-id="0bf6f-145">Wählen Sie in der Gliederungsstruktur den Slot **Text**, die Ellipsen-Schaltfläche (**...**) und dann **Fragment hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="0bf6f-145">In the outline tree, select the **Body** slot, select the ellipsis (**...**), and then select **Add Fragment**.</span></span>
1. <span data-ttu-id="0bf6f-146">In dem Dialogfeld **Wählen Sie Seitenfragment** wählen Sie das Fragment **Warenkorbfragment** und wählen **OK**.</span><span class="sxs-lookup"><span data-stu-id="0bf6f-146">In the **Select Page Fragment** dialog box, select the **Cart fragment** fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="0bf6f-147">Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um die Vorlage einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="0bf6f-147">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="0bf6f-148">Wechseln Sie zu **Seiten**, und wählen Sie dann **Neu** aus, um eine neue Seite zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0bf6f-148">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="0bf6f-149">Im Dialogfeld **Vorlage auswählen** wählen Sie die Vorlage, die Sie zuvor erstellt haben, und geben einen Namen ein und wählen dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="0bf6f-149">In the **Choose a template** dialog box, select the template that you created, enter a page name, and then select **OK**.</span></span>
1. <span data-ttu-id="0bf6f-150">Wählen **Speichern** und dann **Vorschau** aus, um eine Vorschau der Seite anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="0bf6f-150">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="0bf6f-151">Wählen **Bearbeiten beenden**, um die Seite einzuchecken, und wählen Sie dann **Veröffentlichen**, um sie zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="0bf6f-151">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0bf6f-152">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="0bf6f-152">Additional resources</span></span>

[<span data-ttu-id="0bf6f-153">Überblick über Starterkit</span><span class="sxs-lookup"><span data-stu-id="0bf6f-153">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="0bf6f-154">Containermodul</span><span class="sxs-lookup"><span data-stu-id="0bf6f-154">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="0bf6f-155">Shopauswahlmodul</span><span class="sxs-lookup"><span data-stu-id="0bf6f-155">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="0bf6f-156">Kauffeldmodul</span><span class="sxs-lookup"><span data-stu-id="0bf6f-156">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="0bf6f-157">Symbol Einkaufswagenmodul</span><span class="sxs-lookup"><span data-stu-id="0bf6f-157">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="0bf6f-158">Auschecken-Modul</span><span class="sxs-lookup"><span data-stu-id="0bf6f-158">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="0bf6f-159">Auftragsbestätigungsmodul</span><span class="sxs-lookup"><span data-stu-id="0bf6f-159">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="0bf6f-160">Kopfzeilenmodul</span><span class="sxs-lookup"><span data-stu-id="0bf6f-160">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="0bf6f-161">Fußzeilenmodul</span><span class="sxs-lookup"><span data-stu-id="0bf6f-161">Footer module</span></span>](author-footer-module.md)

[<span data-ttu-id="0bf6f-162">Lagerverfügbarkeit für Retail Channels berechnen</span><span class="sxs-lookup"><span data-stu-id="0bf6f-162">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)
