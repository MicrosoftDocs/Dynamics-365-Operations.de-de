---
title: Einkaufswagenmodul
description: Dieses Thema behandelt Einkaufswagenmodule und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1ec8e89ed82bcdffdc21e62d24ad8c8a7d939cdf
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797862"
---
# <a name="cart-module"></a><span data-ttu-id="0d4a6-103">Einkaufswagenmodul</span><span class="sxs-lookup"><span data-stu-id="0d4a6-103">Cart module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0d4a6-104">Dieses Thema behandelt Einkaufswagenmodule und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="0d4a6-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="0d4a6-105">Über das Warenkorbmodul werden die Artikel angezeigt, die dem Warenkorb hinzugefügt wurden, bevor der Kunde zur Kasse geht.</span><span class="sxs-lookup"><span data-stu-id="0d4a6-105">A cart module shows the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="0d4a6-106">Das Modul zeigt eine Bestellzusammenfassung an und der Kunde kann Werbecodes anwenden oder entfernen.</span><span class="sxs-lookup"><span data-stu-id="0d4a6-106">The module also shows an order summary and lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="0d4a6-107">Das Einkaufskorbmodul unterstützt das Auschecken von angemeldeten Benutzern und von Gästen.</span><span class="sxs-lookup"><span data-stu-id="0d4a6-107">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="0d4a6-108">Es unterstützt auch eine Verknüpfung **Zurück zum Einkaufen**.</span><span class="sxs-lookup"><span data-stu-id="0d4a6-108">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="0d4a6-109">Sie können die Route für diesen Link unter **Seiteneinstellungen \> Erweiterungen \> Routen** konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="0d4a6-109">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="0d4a6-110">Das Warenkorbmodul rendert Daten basierend auf der Warenkorb-ID, einem auf der gesamten Site verfügbaren Browser-Cookie.</span><span class="sxs-lookup"><span data-stu-id="0d4a6-110">The cart module renders data based on the cart ID, which is a browser cookie available throughout the site.</span></span> 

<span data-ttu-id="0d4a6-111">Das folgende Bild zeigt ein Beispiel einer Warenkorbseite auf der Fabrikam-Site.</span><span class="sxs-lookup"><span data-stu-id="0d4a6-111">The following image shows an example of a cart page on the Fabrikam site.</span></span>

![Beispiel eines Einkaufskorbmoduls auf der Fabrikam-Site](./media/cart2.PNG)

<span data-ttu-id="0d4a6-113">Das folgende Bild zeigt ein Beispiel einer Warenkorbseite auf der Fabrikam-Site.</span><span class="sxs-lookup"><span data-stu-id="0d4a6-113">The following image shows an example of a cart page on the Fabrikam site.</span></span> <span data-ttu-id="0d4a6-114">In diesem Beispiel wird eine Bearbeitungsgebühr für eine Position fällig.</span><span class="sxs-lookup"><span data-stu-id="0d4a6-114">In this example, there is a handling fee for a line item.</span></span>

![Beispiel eines Einkaufskorbmoduls mit einer Bearbeitungsgebühr für einen Positionsartikel](./media/ecommerce-handling-fee.png)

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="0d4a6-116">Einkaufswagenmodul-Eigenschaften und Slots</span><span class="sxs-lookup"><span data-stu-id="0d4a6-116">Cart module properties and slots</span></span>

| <span data-ttu-id="0d4a6-117">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="0d4a6-117">Property</span></span> | <span data-ttu-id="0d4a6-118">Werte</span><span class="sxs-lookup"><span data-stu-id="0d4a6-118">Values</span></span> | <span data-ttu-id="0d4a6-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0d4a6-119">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="0d4a6-120">Überschrift</span><span class="sxs-lookup"><span data-stu-id="0d4a6-120">Heading</span></span> | <span data-ttu-id="0d4a6-121">Überschriftentext und eine Überschriftsmarkierung (**H1**, **H2**, **H3**, **H4**, **H5** oder **H6**)</span><span class="sxs-lookup"><span data-stu-id="0d4a6-121">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="0d4a6-122">Eine Überschrift für den Einkaufskorb wie "Einkaufstasche" oder "Artikel in Ihrem Korb".</span><span class="sxs-lookup"><span data-stu-id="0d4a6-122">A heading for the cart, such as "Shopping bag" or "Items in your cart."</span></span> |
| <span data-ttu-id="0d4a6-123">Fehlermeldungen "Nicht vorrätig" anzeigen</span><span class="sxs-lookup"><span data-stu-id="0d4a6-123">Show out of stock errors</span></span> | <span data-ttu-id="0d4a6-124">**True** oder **False**</span><span class="sxs-lookup"><span data-stu-id="0d4a6-124">**True** or **False**</span></span> | <span data-ttu-id="0d4a6-125">Wenn diese Eigenschaft **True** ist, zeigt die Warenkorbseite Bestandsfehler an.</span><span class="sxs-lookup"><span data-stu-id="0d4a6-125">If this property is set to **True**, the cart page will show stock-related errors.</span></span> <span data-ttu-id="0d4a6-126">Wir empfehlen, dass Sie für diese Eigenschaft **True** festlegen, wenn Bestandsprüfungen auf die Website angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="0d4a6-126">We recommend that you set this property to **True** if inventory checks are applied on the site.</span></span> |
| <span data-ttu-id="0d4a6-127">Versandkosten für Positionsartikel anzeigen</span><span class="sxs-lookup"><span data-stu-id="0d4a6-127">Show shipping charges for line items</span></span> | <span data-ttu-id="0d4a6-128">**True** oder **False**</span><span class="sxs-lookup"><span data-stu-id="0d4a6-128">**True** or **False**</span></span> | <span data-ttu-id="0d4a6-129">Wenn diese Eigenschaft **True** ist, enthalten Warenkorbpositionen die Versandkosten, wenn diese Angabe verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="0d4a6-129">If this property is set to **True**, cart line items will show the shipping charges, if this information is available.</span></span> <span data-ttu-id="0d4a6-130">Diese Funktion wird im Fabrikam-Design nicht unterstützt, da Benutzer den Versand nur im Auschecken-Ablauf auswählen.</span><span class="sxs-lookup"><span data-stu-id="0d4a6-130">This feature isn't supported in the Fabrikam theme, because users select shipping only in the checkout flow.</span></span> <span data-ttu-id="0d4a6-131">Diese Funktion kann jedoch gegebenenfalls in anderen Workflows aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="0d4a6-131">However, this feature can be turned on in other workflows if it's applicable.</span></span> |
| <span data-ttu-id="0d4a6-132">Verfügbare verkaufsfördernde Maßnahmen anzeigen</span><span class="sxs-lookup"><span data-stu-id="0d4a6-132">Show available promotions</span></span>| <span data-ttu-id="0d4a6-133">**True** oder **False**</span><span class="sxs-lookup"><span data-stu-id="0d4a6-133">**True** or **False**</span></span> | <span data-ttu-id="0d4a6-134">Wenn diese Eigenschaft auf **True** gesetzt ist, zeigt der Warenkorb verfügbare Werbeaktionen basierend auf den Artikeln im Warenkorb an.</span><span class="sxs-lookup"><span data-stu-id="0d4a6-134">If this property is set to **True**, the cart shows available promotions, based on items in the cart.</span></span> <span data-ttu-id="0d4a6-135">Diese Funktion ist nur in Dynamics 365 Commerce, Release 10.0.16 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0d4a6-135">This capability is available in the Dynamics 365 Commerce 10.0.16 release.</span></span> |

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="0d4a6-136">Module, die im Einkaufswagenmodul verwendet werden können</span><span class="sxs-lookup"><span data-stu-id="0d4a6-136">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="0d4a6-137">**Textblock** – Dieses Modul unterstützt benutzerdefinierte Nachrichten im Einkaufswagenmodul.</span><span class="sxs-lookup"><span data-stu-id="0d4a6-137">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="0d4a6-138">Die Meldungen werden durch das Content Management-System (CMS) gesteuert.</span><span class="sxs-lookup"><span data-stu-id="0d4a6-138">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="0d4a6-139">Es können beliebige Nachrichten hinzugefügt werden wie „Für Probleme mit der Bestellung, kontaktieren Sie 1-800-Fabrikam.“</span><span class="sxs-lookup"><span data-stu-id="0d4a6-139">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="0d4a6-140">**Store-Selector** – Dieses Modul wird eine Liste von nahe gelegene Filialen anzeigen, die für eine Abholung zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="0d4a6-140">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="0d4a6-141">Hier können Benutzer einen Ort eingeben, um nach Geschäften in der Nähe zu suchen.</span><span class="sxs-lookup"><span data-stu-id="0d4a6-141">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="0d4a6-142">Weitere Informationen zu diesem Modul finden Sie unter [Auswahlmodul speichern](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="0d4a6-142">For more information on this module, see [Store selector module](store-selector.md).</span></span>

## <a name="module-properties"></a><span data-ttu-id="0d4a6-143">Moduleigenschaften</span><span class="sxs-lookup"><span data-stu-id="0d4a6-143">Module properties</span></span>

<span data-ttu-id="0d4a6-144">Die folgenden Warenkorbmoduleigenschaften können unter **Site-Einstellungen \> Erweiterungen** konfiguriert werden:</span><span class="sxs-lookup"><span data-stu-id="0d4a6-144">The following cart module settings can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="0d4a6-145">**Höchstmenge** – Diese Eigenschaft dient zur Angabe der maximalen Anzahl jedes Artikels, die dem Einkaufskorb hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="0d4a6-145">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="0d4a6-146">Beispielsweise kann ein Einzelhändler festlegen, dass nur 10 eines Produkts als einzelne Transaktion verkauft werden können.</span><span class="sxs-lookup"><span data-stu-id="0d4a6-146">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="0d4a6-147">**Bestand** – Informationen zum Anwenden von Bestandeinstellungen finden Sie unter [Wenden Sie Bestandeinstellungen an](inventory-settings.md).</span><span class="sxs-lookup"><span data-stu-id="0d4a6-147">**Inventory** – For information about how to apply inventory settings, see [Apply inventory settings](inventory-settings.md).</span></span>
- <span data-ttu-id="0d4a6-148">**Zurück zum Einkaufen** – Mit dieser Eigenschaft wird die Route für die Verknüpfung **Zurück zum Einkaufen** angegeben.</span><span class="sxs-lookup"><span data-stu-id="0d4a6-148">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="0d4a6-149">Die Route kann auf Site-Ebene konfiguriert werden, sodass Einzelhändler den Kunden zur Homepage oder zu einer anderen Seite der Site zurückführen können.</span><span class="sxs-lookup"><span data-stu-id="0d4a6-149">The route can be configured at the site level, allowing retailers to take the customer back to the home page or any other page on the site.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0d4a6-150">In der Dynamics 365 Commerce Version 10.0.14 und höher werden Artikel im Warenkorb basierend auf den Einstellungen aggregiert, die im Online-Funktionsprofil für den Online-Shop in der Commerce-Zentrale definiert sind.</span><span class="sxs-lookup"><span data-stu-id="0d4a6-150">In the Dynamics 365 Commerce 10.0.14 release and later, items in the cart are aggregated based on the settings that are defined in the online functionality profile for the online store in Commerce headquarters.</span></span> <span data-ttu-id="0d4a6-151">Weitere Informationen zum Erstellen eines Online-Funktionsprofils und zum Festlegen der für die Aggregation erforderlichen Eigenschaften finden Sie [Erstellen Sie ein Online-Funktionsprofil](online-functionality-profile.md).</span><span class="sxs-lookup"><span data-stu-id="0d4a6-151">For more information about how to create an online functionality profile and set the properties that are required for aggregation, see [Create an online functionality profile](online-functionality-profile.md).</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="0d4a6-152">Commerce Scale Unit-Interaktion</span><span class="sxs-lookup"><span data-stu-id="0d4a6-152">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="0d4a6-153">Das Einkaufskorbmoduls ruft Produktinformationen mithilfe der APIs der Commerce-Skalierungseinheit ab.</span><span class="sxs-lookup"><span data-stu-id="0d4a6-153">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="0d4a6-154">Die Kennung vom Einkaufskorb vom Browsercookie wird verwendet, um die gesamte Produktinformationen der Commerce-Skalierungseinheit abzurufen.</span><span class="sxs-lookup"><span data-stu-id="0d4a6-154">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="0d4a6-155">Ein Einkaufswagenmodul einer Seite hinzufügen</span><span class="sxs-lookup"><span data-stu-id="0d4a6-155">Add a cart module to a page</span></span>

<span data-ttu-id="0d4a6-156">Um ein Einkaufswagenmodul einer neuen Seite hinzuzufügen und die erforderlichen Eigenschaften festzulegen, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="0d4a6-156">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="0d4a6-157">Wechseln Sie zu **Fragmente** und wählen Sie **Neu** aus, um ein neues Fragment zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0d4a6-157">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="0d4a6-158">Wählen Sie im Dialogfeld **Neues Fragment** das Modul **Einkaufskorb** aus.</span><span class="sxs-lookup"><span data-stu-id="0d4a6-158">In the **New fragment** dialog box, select the **Cart** module.</span></span>
1. <span data-ttu-id="0d4a6-159">Geben Sie unter **Name des Fragments** den Namen **Einkaufswagenfragment** ein und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="0d4a6-159">Under **Fragment name**, enter the name **Cart fragment**, and then select **OK**.</span></span>
1. <span data-ttu-id="0d4a6-160">Wählen Sie den Slot **Warenkorb** aus.</span><span class="sxs-lookup"><span data-stu-id="0d4a6-160">Select the **Cart** slot.</span></span>
1. <span data-ttu-id="0d4a6-161">Wählen Sie im Eigenschaftenbereich rechts das Stiftsymbol aus, geben Sie den Überschriftentext in das Feld ein und wählen Sie dann das Häkchensymbol aus.</span><span class="sxs-lookup"><span data-stu-id="0d4a6-161">In the properties pane on the right, select the pencil symbol, enter heading text in the field, and then select the check mark symbol.</span></span>
1. <span data-ttu-id="0d4a6-162">Wählen Sie im Slot **Warenkorb** die Ellipsen-Schaltfläche (**...**) und wählen Sie **Modul hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="0d4a6-162">In the **Cart** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="0d4a6-163">Wählen Sie im Dialogfeld **Modul hinzufügen** das Modul **Auswahl speichern** und dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="0d4a6-163">In the **Add Module** dialog box, select the **Store selector** module, and then select **OK**.</span></span>
1. <span data-ttu-id="0d4a6-164">Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um das Fragment einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="0d4a6-164">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="0d4a6-165">Wechseln Sie zu **Vorlagen** und wählen Sie **Neu** aus, um eine neue Vorlage zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0d4a6-165">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="0d4a6-166">Im Dialogfeld **Neue Vorlage** unter Vorlagenname geben Sie einen Namen für die neue **Vorlage** ein und wählen OK.</span><span class="sxs-lookup"><span data-stu-id="0d4a6-166">In the **New Template** dialog box, under **Template name**, enter a name for the template.</span></span>
1. <span data-ttu-id="0d4a6-167">Wählen Sie in der Gliederungsstruktur den Slot **Text**, die Ellipsen-Schaltfläche (**...**) und dann **Fragment hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="0d4a6-167">In the outline tree, select the **Body** slot, select the ellipsis (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="0d4a6-168">Wählen Sie im Dialogfeld **Fragment auswählen** das Fragment **Warenkorbfragment** und dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="0d4a6-168">In the **Select fragment** dialog box, select the **Cart fragment** fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="0d4a6-169">Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um die Vorlage einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="0d4a6-169">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="0d4a6-170">Wechseln Sie zu **Seiten**, und wählen Sie dann **Neu** aus, um eine neue Seite zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0d4a6-170">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="0d4a6-171">Im Dialogfeld **Vorlage auswählen** wählen Sie die Vorlage, die Sie zuvor erstellt haben, und geben einen Namen ein und wählen dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="0d4a6-171">In the **Choose a template** dialog box, select the template that you created, enter a page name, and then select **OK**.</span></span>
1. <span data-ttu-id="0d4a6-172">Wählen **Speichern** und dann **Vorschau** aus, um eine Vorschau der Seite anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="0d4a6-172">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="0d4a6-173">Wählen **Bearbeiten beenden**, um die Seite einzuchecken, und wählen Sie dann **Veröffentlichen**, um sie zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="0d4a6-173">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0d4a6-174">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="0d4a6-174">Additional resources</span></span>

[<span data-ttu-id="0d4a6-175">Modul für Einkaufswagensymbol</span><span class="sxs-lookup"><span data-stu-id="0d4a6-175">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="0d4a6-176">Auschecken-Modul</span><span class="sxs-lookup"><span data-stu-id="0d4a6-176">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="0d4a6-177">Zahlungsmodul</span><span class="sxs-lookup"><span data-stu-id="0d4a6-177">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="0d4a6-178">Versandadressenmodul</span><span class="sxs-lookup"><span data-stu-id="0d4a6-178">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="0d4a6-179">Lieferoptionenmodul</span><span class="sxs-lookup"><span data-stu-id="0d4a6-179">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="0d4a6-180">Abholinformationsmodul</span><span class="sxs-lookup"><span data-stu-id="0d4a6-180">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="0d4a6-181">Auftragsdetailmodul</span><span class="sxs-lookup"><span data-stu-id="0d4a6-181">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="0d4a6-182">Geschenkkartenmodul</span><span class="sxs-lookup"><span data-stu-id="0d4a6-182">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="0d4a6-183">Lagerverfügbarkeit für Retail Channels berechnen</span><span class="sxs-lookup"><span data-stu-id="0d4a6-183">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)

[<span data-ttu-id="0d4a6-184">Ein Onlinefunktionsprofil erstellen</span><span class="sxs-lookup"><span data-stu-id="0d4a6-184">Create an online functionality profile</span></span>](online-functionality-profile.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]