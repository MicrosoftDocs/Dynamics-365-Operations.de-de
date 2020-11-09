---
title: Einkaufswagenmodul
description: Dieses Thema enthält Einkaufsmodule und es wird beschrieben, wie diese den Sitesieten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
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
ms.openlocfilehash: 39026ec56ebf25342410330f2ba3e2e7773dfd6a
ms.sourcegitcommit: 765056b5dc1d0a8c27e56ff2cbd310ad3349ff09
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "4055426"
---
# <a name="cart-module"></a><span data-ttu-id="98ccb-103">Einkaufswagenmodul</span><span class="sxs-lookup"><span data-stu-id="98ccb-103">Cart module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="98ccb-104">Dieses Thema enthält Einkaufsmodule und es wird beschrieben, wie diese den Sitesieten in Microsoft Dynamics 365 Commerce hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="98ccb-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="98ccb-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="98ccb-105">Overview</span></span>

<span data-ttu-id="98ccb-106">Über das Warenkorbmodul werden die Artikel angezeigt, die dem Warenkorb hinzugefügt wurden, bevor der Kunde zur Kasse geht.</span><span class="sxs-lookup"><span data-stu-id="98ccb-106">A cart module shows the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="98ccb-107">Das Modul zeigt eine Bestellzusammenfassung an und der Kunde kann Werbecodes anwenden oder entfernen.</span><span class="sxs-lookup"><span data-stu-id="98ccb-107">The module also shows an order summary and lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="98ccb-108">Das Einkaufskorbmodul unterstützt das Auschecken von angemeldeten Benutzern und von Gästen.</span><span class="sxs-lookup"><span data-stu-id="98ccb-108">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="98ccb-109">Es unterstützt auch eine Verknüpfung **Zurück zum Einkaufen**.</span><span class="sxs-lookup"><span data-stu-id="98ccb-109">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="98ccb-110">Sie können die Route für diesen Link unter **Seiteneinstellungen \> Erweiterungen \> Routen** konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="98ccb-110">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="98ccb-111">Das Warenkorbmodul rendert Daten basierend auf der Warenkorb-ID, einem auf der gesamten Site verfügbaren Browser-Cookie.</span><span class="sxs-lookup"><span data-stu-id="98ccb-111">The cart module renders data based on the cart ID, which is a browser cookie available throughout the site.</span></span> 

<span data-ttu-id="98ccb-112">Das folgende Bild zeigt ein Beispiel einer Warenkorbseite auf der Fabrikam-Site.</span><span class="sxs-lookup"><span data-stu-id="98ccb-112">The following image shows an example of a cart page on the Fabrikam site.</span></span>

![Beispiel eines Einkaufskorbmoduls auf der Fabrikam-Site](./media/cart2.PNG)

<span data-ttu-id="98ccb-114">Das folgende Bild zeigt ein Beispiel einer Warenkorbseite auf der Fabrikam-Site.</span><span class="sxs-lookup"><span data-stu-id="98ccb-114">The following image shows an example of a cart page on the Fabrikam site.</span></span> <span data-ttu-id="98ccb-115">In diesem Beispiel wird eine Bearbeitungsgebühr für eine Position fällig.</span><span class="sxs-lookup"><span data-stu-id="98ccb-115">In this example, there is a handling fee for a line item.</span></span>

![Beispiel eines Einkaufskorbmoduls mit einer Bearbeitungsgebühr für einen Positionsartikel](./media/ecommerce-handling-fee.png)

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="98ccb-117">Einkaufswagenmodul-Eigenschaften und Slots</span><span class="sxs-lookup"><span data-stu-id="98ccb-117">Cart module properties and slots</span></span>

| <span data-ttu-id="98ccb-118">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="98ccb-118">Property</span></span> | <span data-ttu-id="98ccb-119">Werte</span><span class="sxs-lookup"><span data-stu-id="98ccb-119">Values</span></span> | <span data-ttu-id="98ccb-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="98ccb-120">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="98ccb-121">Überschrift</span><span class="sxs-lookup"><span data-stu-id="98ccb-121">Heading</span></span> | <span data-ttu-id="98ccb-122">Überschriftentext und eine Überschriftsmarkierung ( **H1** , **H2** , **H3** , **H4** , **H5** oder **H6** )</span><span class="sxs-lookup"><span data-stu-id="98ccb-122">Heading text and a heading tag ( **H1** , **H2** , **H3** , **H4** , **H5** , or **H6** )</span></span> | <span data-ttu-id="98ccb-123">Eine Überschrift für den Einkaufskorb wie "Einkaufstasche" oder "Artikel in Ihrem Korb".</span><span class="sxs-lookup"><span data-stu-id="98ccb-123">A heading for the cart, such as "Shopping bag" or "Items in your cart."</span></span> |
| <span data-ttu-id="98ccb-124">Fehlermeldungen "Nicht vorrätig" anzeigen</span><span class="sxs-lookup"><span data-stu-id="98ccb-124">Show out of stock errors</span></span> | <span data-ttu-id="98ccb-125">**True** oder **False**</span><span class="sxs-lookup"><span data-stu-id="98ccb-125">**True** or **False**</span></span> | <span data-ttu-id="98ccb-126">Wenn diese Eigenschaft **True** ist, zeigt die Warenkorbseite Bestandsfehler an.</span><span class="sxs-lookup"><span data-stu-id="98ccb-126">If this property is set to **True** , the cart page will show stock-related errors.</span></span> <span data-ttu-id="98ccb-127">Wir empfehlen, dass Sie für diese Eigenschaft **True** festlegen, wenn Bestandsprüfungen auf die Website angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="98ccb-127">We recommend that you set this property to **True** if inventory checks are applied on the site.</span></span> |
| <span data-ttu-id="98ccb-128">Versandkosten für Positionsartikel anzeigen</span><span class="sxs-lookup"><span data-stu-id="98ccb-128">Show shipping charges for line items</span></span> | <span data-ttu-id="98ccb-129">**True** oder **False**</span><span class="sxs-lookup"><span data-stu-id="98ccb-129">**True** or **False**</span></span> | <span data-ttu-id="98ccb-130">Wenn diese Eigenschaft **True** ist, enthalten Warenkorbpositionen die Versandkosten, wenn diese Angabe verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="98ccb-130">If this property is set to **True** , cart line items will show the shipping charges, if this information is available.</span></span> <span data-ttu-id="98ccb-131">Diese Funktion wird im Fabrikam-Design nicht unterstützt, da Benutzer den Versand nur im Auschecken-Ablauf auswählen.</span><span class="sxs-lookup"><span data-stu-id="98ccb-131">This feature isn't supported in the Fabrikam theme, because users select shipping only in the checkout flow.</span></span> <span data-ttu-id="98ccb-132">Diese Funktion kann jedoch gegebenenfalls in anderen Workflows aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="98ccb-132">However, this feature can be turned on in other workflows if it's applicable.</span></span> |

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="98ccb-133">Module, die im Einkaufswagenmodul verwendet werden können</span><span class="sxs-lookup"><span data-stu-id="98ccb-133">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="98ccb-134">**Textblock** – Dieses Modul unterstützt benutzerdefinierte Nachrichten im Einkaufswagenmodul.</span><span class="sxs-lookup"><span data-stu-id="98ccb-134">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="98ccb-135">Die Meldungen werden durch das Content Management-System (CMS) gesteuert.</span><span class="sxs-lookup"><span data-stu-id="98ccb-135">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="98ccb-136">Es können beliebige Nachrichten hinzugefügt werden wie „Für Probleme mit der Bestellung, kontaktieren Sie 1-800-Fabrikam.“</span><span class="sxs-lookup"><span data-stu-id="98ccb-136">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="98ccb-137">**Store-Selector** – Dieses Modul wird eine Liste von nahe gelegene Filialen anzeigen, die für eine Abholung zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="98ccb-137">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="98ccb-138">Hier können Benutzer einen Ort eingeben, um nach Geschäften in der Nähe zu suchen.</span><span class="sxs-lookup"><span data-stu-id="98ccb-138">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="98ccb-139">Weitere Informationen zu diesem Modul finden Sie unter [Auswahlmodul speichern](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="98ccb-139">For more information on this module, see [Store selector module](store-selector.md).</span></span>

## <a name="module-properties"></a><span data-ttu-id="98ccb-140">Moduleigenschaften</span><span class="sxs-lookup"><span data-stu-id="98ccb-140">Module properties</span></span>

<span data-ttu-id="98ccb-141">Die folgenden Warenkorbmoduleigenschaften können unter **Site-Einstellungen \> Erweiterungen** konfiguriert werden:</span><span class="sxs-lookup"><span data-stu-id="98ccb-141">The following cart module settings can be configured at **Site Settings \> Extensions** :</span></span>

- <span data-ttu-id="98ccb-142">**Höchstmenge** – Diese Eigenschaft dient zur Angabe der maximalen Anzahl jedes Artikels, die dem Einkaufskorb hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="98ccb-142">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="98ccb-143">Beispielsweise kann ein Einzelhändler festlegen, dass nur 10 eines Produkts als einzelne Transaktion verkauft werden können.</span><span class="sxs-lookup"><span data-stu-id="98ccb-143">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="98ccb-144">**Bestand** – Informationen zum Anwenden von Bestandeinstellungen finden Sie unter [Wenden Sie Bestandeinstellungen an](inventory-settings.md).</span><span class="sxs-lookup"><span data-stu-id="98ccb-144">**Inventory** – For information about how to apply inventory settings, see [Apply inventory settings](inventory-settings.md).</span></span>
- <span data-ttu-id="98ccb-145">**Zurück zum Einkaufen** – Mit dieser Eigenschaft wird die Route für die Verknüpfung **Zurück zum Einkaufen** angegeben.</span><span class="sxs-lookup"><span data-stu-id="98ccb-145">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="98ccb-146">Die Route kann auf Site-Ebene konfiguriert werden, sodass Einzelhändler den Kunden zur Homepage oder zu einer anderen Seite der Site zurückführen können.</span><span class="sxs-lookup"><span data-stu-id="98ccb-146">The route can be configured at the site level, allowing retailers to take the customer back to the home page or any other page on the site.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="98ccb-147">In der Dynamics 365 Commerce Version 10.0.14 und höher werden Artikel im Warenkorb basierend auf den Einstellungen aggregiert, die im Online-Funktionsprofil für den Online-Shop in der Commerce-Zentrale definiert sind.</span><span class="sxs-lookup"><span data-stu-id="98ccb-147">In the Dynamics 365 Commerce 10.0.14 release and later, items in the cart are aggregated based on the settings that are defined in the online functionality profile for the online store in Commerce headquarters.</span></span> <span data-ttu-id="98ccb-148">Weitere Informationen zum Erstellen eines Online-Funktionsprofils und zum Festlegen der für die Aggregation erforderlichen Eigenschaften finden Sie [Erstellen Sie ein Online-Funktionsprofil](online-functionality-profile.md).</span><span class="sxs-lookup"><span data-stu-id="98ccb-148">For more information about how to create an online functionality profile and set the properties that are required for aggregation, see [Create an online functionality profile](online-functionality-profile.md).</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="98ccb-149">Commerce Scale Unit-Interaktion</span><span class="sxs-lookup"><span data-stu-id="98ccb-149">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="98ccb-150">Das Einkaufskorbmoduls ruft Produktinformationen mithilfe der APIs der Commerce-Skalierungseinheit ab.</span><span class="sxs-lookup"><span data-stu-id="98ccb-150">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="98ccb-151">Die Kennung vom Einkaufskorb vom Browsercookie wird verwendet, um die gesamte Produktinformationen der Commerce-Skalierungseinheit abzurufen.</span><span class="sxs-lookup"><span data-stu-id="98ccb-151">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="98ccb-152">Ein Einkaufswagenmodul einer Seite hinzufügen</span><span class="sxs-lookup"><span data-stu-id="98ccb-152">Add a cart module to a page</span></span>

<span data-ttu-id="98ccb-153">Um ein Einkaufswagenmodul einer neuen Seite hinzuzufügen und die erforderlichen Eigenschaften festzulegen, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="98ccb-153">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="98ccb-154">Wechseln Sie zu **Fragmente** und wählen Sie **Neu** aus, um ein neues Fragment zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="98ccb-154">Go to **Fragments** , and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="98ccb-155">Wählen Sie im Dialogfeld **Neues Fragment** das Modul **Einkaufskorb** aus.</span><span class="sxs-lookup"><span data-stu-id="98ccb-155">In the **New fragment** dialog box, select the **Cart** module.</span></span>
1. <span data-ttu-id="98ccb-156">Geben Sie unter **Name des Fragments** den Namen **Einkaufswagenfragment** ein und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="98ccb-156">Under **Fragment name** , enter the name **Cart fragment** , and then select **OK**.</span></span>
1. <span data-ttu-id="98ccb-157">Wählen Sie den Slot **Warenkorb** aus.</span><span class="sxs-lookup"><span data-stu-id="98ccb-157">Select the **Cart** slot.</span></span>
1. <span data-ttu-id="98ccb-158">Wählen Sie im Eigenschaftenbereich rechts das Stiftsymbol aus, geben Sie den Überschriftentext in das Feld ein und wählen Sie dann das Häkchensymbol aus.</span><span class="sxs-lookup"><span data-stu-id="98ccb-158">In the properties pane on the right, select the pencil symbol, enter heading text in the field, and then select the check mark symbol.</span></span>
1. <span data-ttu-id="98ccb-159">Wählen Sie im Slot **Warenkorb** die Ellipsen-Schaltfläche ( **...** ) und wählen Sie **Modul hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="98ccb-159">In the **Cart** slot, select the ellipsis ( **...** ), and then select **Add Module**.</span></span>
1. <span data-ttu-id="98ccb-160">Wählen Sie im Dialogfeld **Modul hinzufügen** das Modul **Auswahl speichern** und dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="98ccb-160">In the **Add Module** dialog box, select the **Store selector** module, and then select **OK**.</span></span>
1. <span data-ttu-id="98ccb-161">Wählen Sie **Speichern** , wählen Sie **Bearbeiten beenden** , um das Fragment einzuchecken, und wählen Sie dann **Veröffentlichen** , um es zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="98ccb-161">Select **Save** , select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="98ccb-162">Wechseln Sie zu **Vorlagen** und wählen Sie **Neu** aus, um eine neue Vorlage zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="98ccb-162">Go to **Templates** , and select **New** to create a new template.</span></span>
1. <span data-ttu-id="98ccb-163">Im Dialogfeld **Neue Vorlage** unter Vorlagenname geben Sie einen Namen für die neue **Vorlage** ein und wählen OK.</span><span class="sxs-lookup"><span data-stu-id="98ccb-163">In the **New Template** dialog box, under **Template name** , enter a name for the template.</span></span>
1. <span data-ttu-id="98ccb-164">Wählen Sie in der Gliederungsstruktur den Slot **Text** , die Ellipsen-Schaltfläche ( **...** ) und dann **Fragment hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="98ccb-164">In the outline tree, select the **Body** slot, select the ellipsis ( **...** ), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="98ccb-165">Wählen Sie im Dialogfeld **Fragment auswählen** das Fragment **Warenkorbfragment** und dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="98ccb-165">In the **Select fragment** dialog box, select the **Cart fragment** fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="98ccb-166">Wählen Sie **Speichern** , wählen Sie **Bearbeiten beenden** , um die Vorlage einzuchecken, und wählen Sie dann **Veröffentlichen** , um es zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="98ccb-166">Select **Save** , select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="98ccb-167">Wechseln Sie zu **Seiten** , und wählen Sie dann **Neu** aus, um eine neue Seite zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="98ccb-167">Go to **Pages** , and select **New** to create a new page.</span></span>
1. <span data-ttu-id="98ccb-168">Im Dialogfeld **Vorlage auswählen** wählen Sie die Vorlage, die Sie zuvor erstellt haben, und geben einen Namen ein und wählen dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="98ccb-168">In the **Choose a template** dialog box, select the template that you created, enter a page name, and then select **OK**.</span></span>
1. <span data-ttu-id="98ccb-169">Wählen **Speichern** und dann **Vorschau** aus, um eine Vorschau der Seite anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="98ccb-169">Select **Save** , and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="98ccb-170">Wählen **Bearbeiten beenden** , um die Seite einzuchecken, und wählen Sie dann **Veröffentlichen** , um sie zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="98ccb-170">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="98ccb-171">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="98ccb-171">Additional resources</span></span>

[<span data-ttu-id="98ccb-172">Modul für Einkaufswagensymbol</span><span class="sxs-lookup"><span data-stu-id="98ccb-172">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="98ccb-173">Auschecken-Modul</span><span class="sxs-lookup"><span data-stu-id="98ccb-173">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="98ccb-174">Zahlungsmodul</span><span class="sxs-lookup"><span data-stu-id="98ccb-174">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="98ccb-175">Versandadressmodul</span><span class="sxs-lookup"><span data-stu-id="98ccb-175">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="98ccb-176">Lieferoptionsmodul</span><span class="sxs-lookup"><span data-stu-id="98ccb-176">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="98ccb-177">Auftragsdetailmodul</span><span class="sxs-lookup"><span data-stu-id="98ccb-177">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="98ccb-178">Geschenkkartenmodul</span><span class="sxs-lookup"><span data-stu-id="98ccb-178">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="98ccb-179">Lagerverfügbarkeit für Retail Channels berechnen</span><span class="sxs-lookup"><span data-stu-id="98ccb-179">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)

[<span data-ttu-id="98ccb-180">Ein Onlinefunktionsprofil erstellen</span><span class="sxs-lookup"><span data-stu-id="98ccb-180">Create an online functionality profile</span></span>](online-functionality-profile.md)
